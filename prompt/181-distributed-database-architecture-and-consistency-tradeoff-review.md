# 181. Distributed Database Architecture and Consistency Tradeoff Review

## Current prompt — Distributed database replication design

```text
Design the distribution and replication layer for this database workload.

Start with the application invariants: which reads must observe a completed write, which operations may tolerate staleness, what data loss window is acceptable, and what must happen when the network partitions. Do not use CAP as a slogan; state the actual behaviour the caller will observe.

System context
- Workload and data: [entities, read/write mix, critical invariants, access patterns]
- Scale and geography: [traffic, regions, latency targets, growth]
- Existing state: [single database, primary/replica, sharded cluster, distributed SQL, other]
- Failure and recovery requirements: [node/AZ/region loss, RPO, RTO, maintenance window]
- Constraints: [team skills, managed/self-hosted, cost, residency, migration limits]

Design the system in this order:

1. Data placement
Choose the partition boundary and key. Explain how the choice avoids hot partitions, cross-partition transactions, and expensive reshuffles when capacity changes. State which data should deliberately remain co-located.

2. Replica and write topology
Choose a leader/follower, multi-leader, leaderless quorum, or distributed-consensus model only where it fits. Specify replica placement across failure domains, synchronous versus asynchronous acknowledgement, and the resulting durability and write-latency tradeoff.

3. Read contract
Show which reads go to the writer, a local replica, or a quorum. Cover read-your-writes, monotonic reads, stale analytics reads, and the behaviour during replica lag.

4. Failure path
Walk through a leader, network, or regional failure: detection, quorum decision, fencing of the old writer, promotion, traffic rerouting, treatment of lagging replicas, and recovery after the partition heals. Name the split-brain guard explicitly.

5. Operational proof
Provide the small set of signals and drills that prove the design works: replication lag, quorum health, partition skew, leader-election/failover time, stale-read rate, recovery time, and one failure exercise that must be rehearsed before production.

Use a compact topology diagram and a tradeoff table. Do not invent throughput, inter-region latency, RPO/RTO, or vendor guarantees. If a requirement conflicts with the chosen consistency model, identify the conflict rather than hiding it.
```

**Source model:** Adapted from [Leader/Follower Replication — HLD Fundamentals](https://ikshitij.com/learn/fundamentals/replication-leader-follower/), accessed 2026-07-18. The prompt's distributed-database scope was expanded from the source's replication design exercise; wording was rewritten for this catalog.

## Original version — preserved

```text
You are a senior distributed systems and database architecture advisor supporting an engineering lead, platform owner, CTO, infrastructure team, or data platform team.

Your task is to review a distributed database design, migration, or scaling situation and produce a structured, decision-grade assessment.

INPUTS
- Workload context: [application type, transaction profile, read/write mix, latency targets, global vs regional usage, growth rate]
- Current architecture: [single-node database, sharded database, distributed SQL, replicated cluster, multi-region topology, hybrid estate]
- Data distribution model: [partitioning strategy, shard key, range vs hash vs directory routing, replication model, leader/follower layout]
- Consistency and availability needs: [strong consistency, bounded staleness, eventual consistency, failover expectations, tolerated downtime]
- Query and transaction patterns: [point reads, range scans, joins, cross-partition queries, write hotspots, multi-row transactions, analytics overlap]
- Operational context: [managed vs self-hosted, cloud layout, observability, backup/restore model, incident history, team skill]
- Current pain points: [hot partitions, cross-region latency, failover risk, replication lag, rebalancing pain, write contention, cost growth, other]
- Constraints: [compliance, residency, migration risk, budget, uptime obligations, vendor lock-in concerns]
- Evidence available: [top queries, topology diagram, traffic distribution, partition stats, failover metrics, incident timelines, latency percentiles]
- Known assumptions: [optional]

DELIVERABLE
Create a structured report with the following sections.

1. Executive summary
- State whether the current distributed database posture is appropriate, strained, fragile, or over-engineered.
- Summarize the main architecture problem in one sentence.
- Identify the top 3 decision drivers.

2. Distribution and partitioning diagnosis
- Explain how data is currently partitioned or should be partitioned.
- Assess whether the shard or partition strategy matches real workload distribution.
- Identify likely hot shard, skew, routing, or resharding risks.
- Distinguish scaling problems caused by partition choice from those caused by query design.

3. Replication and failover review
- Assess the replication model and likely recovery behavior.
- Explain where replication improves resilience and where it adds latency or coordination cost.
- Identify likely failover weaknesses, lag risks, read-staleness issues, or replica pressure.
- Distinguish resilience posture from performance posture.

4. Consistency, availability, and partition-tolerance tradeoffs
- Evaluate whether the chosen system behavior matches the application's real correctness needs.
- Explain the practical tradeoffs among consistency, availability, and partition tolerance.
- Identify where strong consistency is necessary and where looser guarantees may be acceptable.
- Say directly if the architecture is promising impossible guarantees.

5. Query and transaction behavior review
- Assess how the architecture handles point reads, range queries, distributed joins, cross-partition transactions, and write-heavy paths.
- Identify where network round trips, consensus, or cross-partition coordination are likely driving latency.
- Explain whether the workload is a good fit for distributed SQL, manual sharding, or another model.
- Distinguish one-off slow paths from structural distributed-system cost.

6. Operational complexity and observability assessment
- Evaluate the burden of routing, balancing, re-sharding, backups, incident response, and capacity planning.
- Identify where the team may be underestimating operational overhead.
- Assess whether current telemetry is sufficient to detect skew, lag, failover drift, or saturation early.
- Note where managed services reduce burden and where they do not remove architectural responsibility.

7. Option comparison and tradeoffs
Compare at least 3 realistic options, such as:
- keep the current system and tune partitioning
- move from manual sharding to a native distributed database
- stay on a single-node or primary-replica architecture longer
- adopt distributed SQL for strong consistency workloads
- accept eventual consistency for selected paths
- separate operational workloads by region or domain

For each option, compare:
- scalability fit
- correctness fit
- latency impact
- failover posture
- operational complexity
- migration risk
- cost

8. Risk register
Build a risk table with columns:
- risk
- category
- likelihood low, medium, or high
- impact low, medium, or high
- early warning signal
- mitigation

Include at least:
- hot partition risk
- consistency tradeoff risk
- replication or lag risk
- failover risk
- re-sharding or migration risk
- observability or operational overload risk

9. Recommended actions
Provide:
- 3 immediate actions for the next 30 days
- 3 structural actions for the next 90 days
- 3 metrics or signals that should be monitored

For each action, explain:
- why it matters
- expected effect on latency, resilience, or correctness
- what must be validated first

10. Questions that must be resolved
List the highest-leverage follow-up questions.
Focus on questions that would materially change the architecture recommendation.

11. Final recommendation
End with:
- overall verdict
- the single most important distribution or consistency correction
- the biggest hidden distributed-systems risk
- what still needs verification before migration, repartitioning, or rollout

RESPONSE RULES
- Be practical, skeptical, and workload-first.
- Explicitly separate:
  - Confirmed
  - Assumptions
  - Needs verification
- Do not assume horizontal scale is automatically worth the coordination cost.
- Do not assume replication alone solves failover or global latency problems.
- If shard-key or partition evidence is missing, say confidence is limited.
- If the system needs strong correctness guarantees, evaluate consistency requirements directly rather than hand-waving with CAP slogans.
- Prefer decision-useful architecture reasoning over distributed-systems jargon.

OUTPUT FORMAT
Use Markdown with:
- clear headings
- one compact option-comparison table
- one risk table
- concise bullet points
- a short final recommendation block

Now review this case:
[PASTE CASE HERE]
```
