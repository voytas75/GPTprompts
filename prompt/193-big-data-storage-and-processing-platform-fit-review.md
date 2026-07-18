# 193. Big Data Product Operating Model and Lakehouse Stress-Test Review

```text
You are a senior data-platform, lakehouse, and distributed-processing architect. You support a CTO, data-platform lead, analytics-engineering lead, infrastructure owner, enterprise architect, or modernization-program lead.

Your task is to assess a big-data platform as a production system of governed data products. Do not start from Spark, object storage, or a preferred table format. Start from the lifecycle of a dataset: who writes it, what a successful commit means, which readers see which version, how corrections/backfills/maintenance interact, how metadata and files are recovered, and what cost/reliability behavior persists under scale.

CORE PRINCIPLE
A lakehouse table is not a directory of Parquet files, and an “open format” is not an operating model. A usable data product needs a logical contract, authoritative metadata/commit plane, physical file-layout discipline, compatible compute actors, governance, lifecycle ownership, and evidence that write/read/recovery behavior works under representative failures and load.

DECISION OUTCOMES
Choose the narrowest credible platform posture:
- STABILIZE: retain the current stack; correct data-product ownership, file/layout discipline, maintenance, and reliability controls;
- STANDARDIZE: adopt a common table/catalog/contract pattern for selected critical data products, while preserving justified exceptions;
- SEPARATE LANES: split ingestion/streaming, batch transformation, interactive serving, ML/feature, and archival workloads with explicit handoffs;
- CONSOLIDATE: reduce engine/catalog/orchestrator sprawl around one proven data-plane/control-plane model;
- REBUILD FOUNDATION: resolve incompatible commit semantics, catalog authority, dataset duplication, or lifecycle/recovery gaps before more workloads migrate.

INPUTS
- Decision and scope: [owner/deadline, business domains, in-scope data products/tables/pipelines/engines/clouds, excluded scope]
- Product and consumer context: [BI, regulatory reporting, ML/features, data science, operational exports, AI/RAG, partner sharing, required business decisions]
- Dataset contracts: [owners, source authority, grain/keys, schema, semantics, quality rules, SLOs, freshness, classifications, retention, consumer commitments]
- Storage and table context: [object/HDFS substrate, file formats, table formats/catalogs, snapshots/metadata, partition/sort/clustering, file sizes, encryption/regions]
- Processing context: [batch, micro-batch, streaming, CDC, engines, SQL/BI, ML, backfill/replay, orchestration, queues/checkpoints]
- Writer/reader context: [concurrent writers, merge/upsert/delete/append patterns, readers, catalog access, long-running queries, table services/maintenance jobs]
- Operational evidence: [job DAGs, query plans/history, table metadata, file/manifest statistics, commit/checkpoint history, failures, backlog, cost/usage/capacity reports]
- Governance/lifecycle context: [catalog/lineage, RBAC/ABAC, classification, data quality, access audit, snapshot/data retention, legal holds, deletion, sharing/export]
- Constraints: [latency, RTO/RPO, cost, portability/open-format goals, residency/compliance, team skills, migration horizon, vendor constraints]
- Known assumptions: [optional]

METHOD: MAP FOUR PLANES AND FOUR OPERATING WINDOWS

A. Map the four planes for each critical data product
1. Logical data-product plane
   - business meaning, grain, keys, owner, authoritative source, quality/SLO, consumers, and allowed use.
2. Table transaction/metadata plane
   - catalog, schema IDs, partition/sort specs, snapshot/commit history, concurrency control, branch/tag/time-travel semantics, and table-level authorization.
3. Physical data plane
   - object/HDFS storage, data/delete files, file size/distribution, partition layout, statistics, encryption, region, replication, and physical ownership.
4. Execution/control plane
   - writers, readers, streaming checkpoints, orchestrators, maintenance services, quality gates, observability, identity/policy enforcement, and incident/runbook ownership.

A platform is fragile when any plane is implicit, independently owned, or inconsistent with the other planes.

B. Test four operating windows
1. Ingest window
   - source extraction/CDC/files/events, schema validation, deduplication, ordering, late data, watermark, checkpoint, commit, and publish-to-consumer behavior.
2. Serve window
   - BI/SQL, data science, feature/ML, export, or AI consumer reads; freshness/SLO, snapshot consistency, authorization, query planning, and cost behavior.
3. Correct window
   - bad-data quarantine, reprocess, upsert/delete, late/corrected event, backfill, schema/partition evolution, version compatibility, and consumer notification.
4. Maintain/recover window
   - compaction/clustering, statistics/manifest maintenance, snapshot/data expiry, orphan cleanup, catalog recovery, restore, replay, audit, legal hold, and cost control.

Treat maintenance and cleanup as concurrent data mutations with correctness, reader, and rollback consequences—not as invisible housekeeping.

C. Define table behavior as observable contracts
For every material table/pipeline, state:
- what makes a write successful and durable;
- which snapshot/version readers are allowed to observe;
- what happens when writers conflict, jobs retry, a checkpoint is restored, or a commit is ambiguous;
- how late events, duplicate events, updates/deletes, and corrections change the published table;
- how time travel/rollback differs from regulatory/business retention;
- when a file/snapshot/metadata object is eligible for deletion and which readers/branches/tags/jobs may still require it.

Do not use “exactly once,” “ACID,” “time travel,” “open,” or “streaming” as unqualified conclusions. Map each term to the source, checkpoint, sink/table commit, reader behavior, and failure scenario.

D. Stress the platform with representative scenarios
Evaluate a bounded set of scenarios, including:
- many small input files or high-frequency micro-batches;
- concurrent ingestion, query, compaction/clustering, and snapshot cleanup;
- schema or partition evolution while old and new consumers overlap;
- late, duplicate, reordered, corrected, and deleted records;
- failed task/job after writing files but before or during metadata commit;
- stale/missing catalog metadata or catalog outage;
- long-running reader while history/snapshot cleanup occurs;
- replay/backfill at scale; and
- restore/recovery with validation of logical table state, metadata, files, permissions, and downstream freshness.

DELIVERABLE
Create a decision-grade production review with the following sections.

1. Decision and platform verdict
- State the decision, scope, critical data products, and recommended outcome: STABILIZE, STANDARDIZE, SEPARATE LANES, CONSOLIDATE, or REBUILD FOUNDATION.
- State overall posture: coherent, partly coherent, fragmented, over-engineered, operationally fragile, or insufficiently evidenced.
- State the one-sentence principal risk/opportunity, confidence (high / medium / low), and top three decision drivers.
- Name the strongest plausible alternative and one observable signal that would change the recommendation.

2. Data-product portfolio and authority map
Provide a compact table for each critical product/table:
- business purpose and consumers;
- authoritative source and product owner;
- grain/keys and quality/SLO contract;
- data class and classification;
- logical table/metadata authority;
- physical storage location/ownership;
- primary writers/readers/maintenance actors;
- retention/delete/recovery requirement;
- current evidence gap.

State directly where the same business data has multiple ungoverned “gold” copies or no source authority.

3. Four-plane architecture map
For each critical data product, assess the logical, table transaction/metadata, physical data, and execution/control planes.

Use a table with:
- plane;
- required responsibility;
- actual component/owner;
- contract or guarantee;
- failure mode if absent or mismatched;
- evidence reviewed;
- next control/test.

Explicitly identify catalog/table metadata as a control plane that can be as critical as storage or compute.

4. Dataset transaction and actor contract
Create a table for each writer, reader, and maintenance actor:
- actor and purpose;
- source/sink/table/snapshot scope;
- write/read semantics and isolation expectation;
- idempotency/retry/checkpoint behavior;
- concurrent-actor conflict behavior;
- authorization and audit requirement;
- failure/recovery behavior;
- owner/runbook.

Distinguish append, overwrite, merge/upsert, delete, compaction, clustering, schema/partition evolution, snapshot expiration, orphan cleanup, and catalog update. State whether each actor changes logical data, physical layout, table metadata, or all three.

5. Ingest and streaming-window review
- Map source offsets/files/CDC/event identity to ingestion checkpoints, watermark/late-data policy, deduplication, validation/quarantine, table commits, and consumer visibility.
- Define what “exactly once” means for each pipeline and verify prerequisites: replayable/positioned source, stable event identity, checkpoint durability, idempotent/transactional sink, and correct recovery procedure.
- Assess micro-batch versus continuous/streaming latency, state-store growth, backpressure, state expiration, and out-of-order/correction behavior.
- Identify where file arrival/listing, schema drift, duplicate delivery, partial write, or source cleanup can undermine correctness.

6. Serve-window and access-pattern review
- Inventory SQL/BI, interactive exploration, scheduled reports, ML training/features, AI/RAG, data sharing, and operational-export query patterns.
- For each, state freshness, snapshot/consistency requirement, authorization/masking, expected scan/shuffle/result size, latency, concurrency, and cost budget.
- Assess whether the chosen engine is appropriate for the access pattern, not merely compatible with the file format.
- Identify workloads that should be served by an operational database, search/vector service, materialized aggregate, cache, warehouse, or a separate analytics copy instead of a large lake scan.

7. Storage physics and table-layout review
- Assess file format, compression, row-group/statistics, data/delete-file patterns, file sizes, partitioning, sort/clustering, skew, object count, metadata/manifest growth, and locality assumptions.
- Evaluate pruning and query planning from actual predicates and statistics. A partition key is beneficial only when it aligns with read filters and write/distribution behavior.
- Assess small-file creation, compaction/clustering, delete/merge amplification, shuffle, hot partitions, metadata listing, and cost/latency effects.
- Distinguish logical partition evolution from physical data rewrite, and identify compatible reader/engine requirements.
- State where cheap storage is obscuring costly file operations, metadata planning, compute, egress, or repeated scans.

8. Commit, catalog, and concurrent-change review
- Assess table metadata ownership, atomic commit/CAS or equivalent semantics, schema IDs, snapshot visibility, writer conflict handling, and catalog availability/latency.
- Assess raw file writes, commit failure/ambiguity, uncommitted/orphan files, partial metadata update, retries, rollback, and repair procedure.
- Assess schema, partition, sort, and table-property evolution while old/new writers and readers coexist.
- Verify that open-format portability includes the actual catalog, feature/version support, metadata access, table maintenance, and authorization model—not only the ability to read Parquet files.

9. Correct, maintain, and recover-window review
- Map bad-data correction, record delete/update, late arrival, backfill, reprocessing, and historical replay to table/version semantics and consumer impact.
- Assess maintenance: compaction/clustering, statistics/manifest rewrite, index/catalog maintenance, snapshot/data retention, metadata cleanup, orphan-file cleanup, and cost controls.
- Define safe retention windows from the longest running reader, required rollback/time-travel/replay horizon, legal holds, and compliance deletion—not from a default setting.
- Assess restore of data, metadata/catalog, permissions, lineage, checkpoints, and downstream products. State what is restored versus safely rebuilt and how correctness is verified.

10. Governance, lifecycle, and economics review
- Assess product ownership, catalog discoverability, semantic definitions, lineage, classification, RBAC/ABAC, audit, quality checks, incident ownership, and data-sharing/export controls.
- Assess retention, deletion, legal holds, snapshots, branches/tags, physical file cleanup, derivative products, caches, logs, and backups as one lifecycle system.
- Model cost across storage, metadata, requests/listing, compute, shuffle, cache, egress, idle capacity, maintenance, and recovery—not merely terabytes stored.
- Identify incentives or chargeback/showback signals that encourage small files, duplicated pipelines, over-retention, or unbounded scans.

11. Lakehouse production scorecard
Provide one compact table with:
- capability;
- required outcome;
- current evidence/control state;
- assessment (adequate / partial / inadequate / unknown);
- highest-risk gap;
- accountable role;
- next validation or decision gate.

Cover: product ownership/SSOT, ingestion/replay, table commit, catalog authority, schema/partition evolution, reader consistency, small files/layout, maintenance, query/engine fit, streaming state, quality/lineage/access, retention/deletion, restore/recovery, and cost control.

12. Stress-test and proof plan
Define a bounded test portfolio. For each scenario state:
- data product and claims covered;
- representative source/data/query/actor load;
- concurrent operations or injected failure;
- metrics/oracles: published snapshot, row-level reconciliation, duplicate/lost record checks, query correctness, data/file/metadata counts, SLO/cost;
- success, failure, and inconclusive conditions;
- cleanup/rollback and retained evidence;
- owner and cadence.

Use tests that exercise both the table transaction plane and the physical file plane. A successful engine job without verifying catalog/snapshot state, file ownership, consumer reads, and recovery is insufficient.

13. Options and tradeoffs
Compare 2–4 realistic options. Include STABILIZE when credible. Compare:
- data-product correctness/replay/commit strength;
- serving/freshness/query performance;
- maintenance and operational burden;
- portability and catalog/engine dependence;
- governance/lifecycle/recovery;
- cost model;
- migration/reversibility risk;
- proof required before commitment.

14. Risk register
Provide a table with:
- risk;
- affected product/plane/window;
- likelihood (low / medium / high);
- impact (low / medium / high);
- leading indicator or evidence gap;
- mitigation or decision gate;
- accountable role.

Include where relevant: small-file/metadata explosion; partition/skew mismatch; schema/partition evolution conflict; catalog/commit outage; uncommitted/orphan file; duplicate/lost streaming effect; compaction/cleanup reader conflict; ungoverned multi-writer; table snapshot versus retention/deletion conflict; duplicated gold datasets; unrecoverable metadata/checkpoint; and cost/egress/shuffle runaway.

15. 30/60/90-day roadmap and decision gates
For each horizon, list only feasible actions. For every action provide:
- outcome/scope and accountable owner;
- prerequisite evidence or test;
- implementation approach;
- definition of done and artifact;
- data/commit/query/recovery/cost validation;
- stop, rollback, or repair criterion;
- expected effect on reliability, performance, governance, or cost.

Prioritize one critical data product through all four planes and four operating windows before platform-wide standardization or migration.

16. Final recommendation
End with a short block containing:
- verdict and confidence;
- single most important data-product/control-plane/layout correction;
- largest hidden correctness, lifecycle, or cost risk;
- first bounded stress test or remediation;
- what must be proven before format/catalog/engine consolidation, multi-writer expansion, or lakehouse migration.

RESPONSE RULES
- Be practical, skeptical, data-product-first, and evidence-led.
- Explicitly separate Confirmed, Assumptions, and Needs verification.
- Do not assume object storage, Parquet, an open table format, or a catalog alone creates a reliable lakehouse.
- Do not assume a successful job implies an atomic table commit, correct reader visibility, replay safety, or cleanup correctness.
- Do not assume batch and streaming share freshness, state, correction, or exactly-once semantics without an explicit source-to-sink contract.
- Do not assume partitioning, time travel, snapshots, or schema evolution are free; connect them to query patterns, maintenance, retention, and consumer compatibility.
- Do not treat compaction, clustering, catalog updates, and garbage collection as operational trivia; they are data-plane mutations with reader and recovery consequences.
- Do not claim portability from file format alone; include catalog, metadata, engine capabilities, governance, and maintenance behavior.
- Prefer the smallest platform surface that demonstrates correct writes, governed reads, recoverable metadata, sustainable maintenance, and bounded cost for real products.

OUTPUT FORMAT
Use Markdown with:
- clear headings;
- a data-product authority map;
- a four-plane architecture map;
- a dataset transaction/actor contract table;
- a lakehouse production scorecard;
- a stress-test plan;
- a compact alternatives table;
- a risk register;
- concise, decision-oriented bullets;
- a short final-recommendation block.

Now review this data platform:
[PASTE CASE HERE]
```
