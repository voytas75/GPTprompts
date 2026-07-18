# 180. Data Warehouse and BI Pipeline Review

## Current prompt — Modern data warehouse architecture

```text
You are a senior data architect. Design a modern analytics platform that turns the supplied sources into trustworthy, self-service business insight.

Context
- Data sources: [databases, SaaS tools, APIs, files, event streams]
- Analytics users: [executives, analysts, operations, data scientists, external users]
- Current state: [existing warehouse/lake, BI tools, pipelines, pain points]
- Priority decisions or use cases: [questions, dashboards, operational actions]
- Data volume and freshness: [size, change rate, batch/near-real-time expectations]
- Budget and team constraints: [skills, platform limits, cost ceiling, compliance]

Produce a technical design that is specific to this context.

1. Explain the recommended platform approach and the one credible alternative. Compare total operating cost, team fit, performance needs, and migration risk; do not select a product by popularity alone.

2. Describe the data path from source to consumption:
- raw or landing layer: ingestion, history, schema change handling, lineage;
- cleaned or conformed layer: validation, deduplication, keys, and shared business entities;
- business-ready layer: dimensional models, aggregates, governed metrics, and performance strategy.

3. Define the pipeline operating model:
- batch, CDC, streaming, or mixed ingestion by source;
- transformation layout and materialization choices;
- idempotency, retries, backfills, failure recovery, and deployment workflow.

4. Design trust into the platform:
- tests and reconciliation at the right layers;
- freshness and anomaly signals;
- data contracts or change controls;
- the owner and response path when a metric becomes unreliable.

5. Design the semantic and BI layer:
- core metric definitions and their owners;
- how analysts, dashboards, and applications reach the same business meaning;
- access control, sensitive-data handling, and the boundaries of self-service.

6. End with a phased implementation sequence. State what to build first, what evidence must be available before the next phase, and which expensive capability should be deliberately deferred.

Use concrete diagrams in text or Markdown tables when useful. Do not invent data volumes, tool capabilities, costs, or compliance obligations. If a design choice depends on an unknown, state the decision criterion rather than pretending it is settled.
```

**Source model:** Adapted from [Modern Data Warehouse Architecture Design — AIOpenLibrary](https://aiopenlibrary.com/prompts/data-warehouse-architecture-modern-stack), accessed 2026-07-18. The category fit and structural approach were adopted; wording was rewritten for this catalog.

## Original version — preserved

```text
You are a senior analytics architecture advisor supporting a data lead, BI owner, analytics engineer, CIO, COO, or transformation team.

Your task is to review a data warehouse, BI, or analytics pipeline situation and produce a structured, decision-grade assessment.

INPUTS
- Business context: [industry, scale, major functions, reporting cadence, executive decision needs]
- Source landscape: [ERP, CRM, product data, finance systems, operational databases, files, APIs, event streams]
- Warehouse and pipeline context: [platform, ETL/ELT model, orchestration, staging, modeling layer, refresh cadence, semantic layer]
- Reporting context: [dashboards, KPI definitions, self-service BI, executive reporting, ad hoc analysis, OLAP/reporting tools]
- Data quality and governance context: [ownership, lineage, definitions, reconciliation issues, access controls, metadata, catalog]
- Current pain points: [slow refresh, broken pipelines, conflicting metrics, poor trust, rising cost, weak adoption, data latency, rework]
- Constraints: [budget, compliance, migration limits, cloud preference, team skill, tool sprawl, change fatigue]
- Evidence available: [data model examples, pipeline DAGs, incident history, refresh timings, cost metrics, sample dashboards, SLAs]
- Known assumptions: [optional]

DELIVERABLE
Create a structured report with the following sections.

1. Executive summary
- State whether the warehouse and BI posture is reliable, fragile, fragmented, or scaling poorly.
- Summarize the main analytics delivery problem in one sentence.
- Identify the top 3 decision drivers.

2. Source-to-insight architecture diagnosis
- Explain how data moves from source systems into warehouse tables and BI outputs.
- Identify where data is extracted, transformed, validated, enriched, and exposed.
- Highlight likely bottlenecks, handoff failures, or hidden manual steps.
- Distinguish architecture problems from process discipline problems.

3. Data warehouse fit assessment
- Evaluate whether the warehouse is structured appropriately for analytics, reporting, and historical analysis.
- Assess whether warehouse design choices support trusted BI and repeatable decision-making.
- Identify where the warehouse is being misused as an operational database, raw dump, or reporting patch layer.
- Note if a lakehouse, mart, or revised modeling approach may be more suitable.

4. ETL/ELT and data pipeline review
- Assess pipeline reliability, transformation quality, lineage, and recoverability.
- Identify risks in staging, scheduling, dependency management, schema drift, and data freshness.
- Explain whether ETL or ELT choices appear aligned with scale, governance, and maintainability.
- Highlight where data integration debt is creating recurring operational friction.

5. BI and decision-support review
- Evaluate whether dashboards, OLAP/reporting layers, and self-service tools support real decisions.
- Identify conflicting metrics, semantic inconsistency, weak KPI definitions, or overproduction of dashboards.
- Distinguish visibility problems from actionability problems.
- Say directly if the BI layer provides reports but not reliable decision support.

6. Data quality, trust, and governance assessment
- Assess ownership, metric definitions, lineage, reconciliation, access control, and auditability.
- Identify which trust issues are local and which are systemic.
- Explain where weak metadata, cataloging, or stewardship is undermining BI adoption.
- Distinguish technical data defects from governance defects.

7. Option comparison and tradeoffs
Compare at least 3 realistic options, such as:
- stabilize the current warehouse and pipeline
- redesign transformations and semantic layer
- split operational reporting from analytical reporting
- introduce marts or domain-oriented models
- modernize toward ELT/lakehouse patterns
- reduce tool sprawl and centralize KPI ownership

For each option, compare:
- delivery speed
- trust and consistency
- maintainability
- scalability
- cost
- migration risk
- team burden

8. Risk register
Build a risk table with columns:
- risk
- category
- likelihood low, medium, or high
- impact low, medium, or high
- early warning signal
- mitigation

Include at least:
- pipeline reliability risk
- conflicting KPI risk
- data freshness risk
- lineage/governance risk
- cost growth risk
- adoption/trust risk

9. Recommended actions
Provide:
- 3 immediate actions for the next 30 days
- 3 structural actions for the next 90 days
- 3 metrics or signals that should be monitored

For each action, explain:
- why it matters
- expected effect on trust, latency, reliability, or cost
- what must be validated first

10. Questions that must be resolved
List the highest-leverage follow-up questions.
Focus on questions that would materially change the architecture or operating model recommendation.

11. Final recommendation
End with:
- overall verdict
- the single most important warehouse/pipeline correction
- the biggest hidden analytics risk
- what still needs verification before redesign, migration, or tool consolidation

RESPONSE RULES
- Be practical, skeptical, and decision-oriented.
- Explicitly separate:
  - Confirmed
  - Assumptions
  - Needs verification
- Do not assume a warehouse automatically creates trustworthy BI.
- Do not treat more dashboards as the same thing as better analytics.
- If KPI definitions differ across teams, say there is no true single source of truth.
- If evidence on freshness, lineage, or reconciliation is missing, say confidence is limited.
- Prefer source-to-decision reasoning over tool-centric descriptions.

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
