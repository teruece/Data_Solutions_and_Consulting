## Enterprise Data Model Modernisation — Maximus UK


Led Enterprise Data Model Modernisation at Maximus UK — designed and implemented production-grade dimensional models, automated data quality and semantic layers, and reduced reporting discrepancies while enabling AI-ready datasets for cross-functional analytics.

## Project description

The Enterprise Data Model Modernisation at Maximus UK was a strategic programme to replace fragmented, inconsistent reporting datasets with a single, scalable, production-grade analytical data model. The objective was to create a reusable, documented set of dimensional models and production SQL views that power leadership reporting, product analytics, operational dashboards, and are AI/ML-ready. The programme focused on improving data quality, reducing engineer/analyst rework, shortening time-to-insight, and enabling governed self-service analytics across HR, service delivery and operations teams.

## Core objectives

• Build a single source of truth (SSOT) for enterprise KPIs and events.

• Replace ad-hoc tables and Excel-driven joins with well-documented star-schema models.

• Operationalise data quality checks and lineage to improve trust.

• Produce production-ready views (BigQuery / cloud warehouse) and a semantic layer consumable by Power BI.

• Prepare datasets for downstream AI/ML experiments (consistent keys, timestamps, completeness).


## Project scope

Included data domains:

• Workforce & people events (hires, leavers, role changes)

• Operational events (case events, outcomes, SLA timestamps)

• Product / service usage metrics

• Financial/contract metrics required for enterprise reporting


Excluded: one-off legacy systems put on an archival cadence unless critical for KPI traceability.

## Phased step-by-step approach

PHASE 0 — Mobilise & Governance (Kickoff)

• Stakeholder alignment: Convene product leads, data engineering, BI owners and senior sponsors; define business outcomes and success metrics.

• Define governance: Identify data owners, stewards, and SLAs; agree acceptance criteria for model promotion to “production.”

• Deliverables: Project charter, stakeholder RACI, success KPIs (accuracy, freshness, adoption targets).


PHASE 1 — Discovery & Current State Assessment

• Inventory datasets: Catalogue existing raw sources, ETL jobs, SQL views, dashboards and downstream consumers.

• Map reporting pain points: Interview analysts and stakeholders to capture mismatched definitions and manual work.

• Profiling and lineage: Run data profiling (row counts, null rates, cardinality) and capture lineage for critical fields.

• Deliverables: Data catalogue export, profiling report, pain-point register, prioritized domain list.

PHASE 2 — Requirement & KPI Definition

• Workshop KPIs: Facilitate working sessions to standardise KPI definitions (e.g., Active Cases, Time-to-Resolution, Attrition). Convert ambiguous definitions into precise, testable logic (filters, denominators, windows).

• Define analytical use cases: Reporting, ad-hoc analysis, experimentation, ML training sets.

• Deliverables: KPI specification doc, metric glossary, sample queries showing expected results.


PHASE 3 — Conceptual & Logical Modelling

• Conceptual model: Map entity relationships (users, cases, interactions, contracts). Confirm grain for facts (e.g., event-level or daily aggregate).

• Logical design: Design star schema per domain — fact tables (events), dimension tables (user, time, org). Include surrogate keys and slowly changing dimension (SCD) strategies.

• Validation: Review with product managers and data engineers for feasibility and performance considerations.

• Deliverables: ER diagrams, model rationale document, grain definitions.


PHASE 4 — Physical Design & Implementation Planning

• Physical model: Translate logical models into physical tables/views for the target warehouse (BigQuery recommended). Add partitioning/clustering strategy.

• Transformation architecture: Define transformation approach — dbt models / SQL views / orchestrator (Airflow/Composer). 

• Data contracts: Agree required fields, types, cardinality and freshness.

• Deliverables: Physical schema scripts, dbt model plan, materialisation spec, data contract docs.


PHASE 5 — Build & Test

• Development: Implement staging queries (cleaning, canonicalisation), then build fact and dimension models as tested SQL/dbt models.

• Data quality tests: Add automated tests (row counts, freshness, uniqueness, null thresholds, referential integrity). Implement in CI pipelines.

• Performance tuning: Add partitioning, clustering, and pre-aggregations where needed.

• Unit & integration tests: Validate KPI outputs with known examples and reconcile against legacy reports.

• Deliverables: dbt project (or equivalent), SQL views, automated tests, test run logs.


PHASE 6 — Semantic Layer & Visualisation Layer

• Semantic layer: Create a governed semantic layer (views or LookML/Power BI semantic models) exposing approved metrics and dimensions.

• Dashboard migration: Rebuild or refactor existing Power BI dashboards to consume the semantic layer, standardise visuals and incorporate drill-downs for product and leadership use. Ensure row-level security where required.

• Deliverables: Semantic model, updated dashboards, dashboard runbooks.


PHASE 7 — Release, Training & Adoption

• Staged rollout: Release to a pilot group, collect feedback and iterate. Move to wider rollout after sign-off.

• Training: Run hands-on sessions for analysts, PMs and stakeholders on the new model, KPIs, and how to query the semantic layer. Provide quick-start guides and query examples.

• Deliverables: Training slides, cheat-sheets, FAQ, adoption metrics dashboard.


PHASE 8 — Operate & Continuous Improvement

• Monitoring & alerting: Monitor data freshness, test failures, and query performance; route incidents to owners.

• Governance cadence: Quarterly reviews for new KPIs, model changes and data quality thresholds.

• Iteration: Incorporate new product events and feedback; promote changes via a controlled release process.

• Deliverables: Operational runbook, monitoring dashboards, cadence schedule.


## Key artifacts 

• KPI glossary: precise calculation for each KPI (SQL pseudo-code).

• dbt model hierarchy: staging → marts → semantic_views.

• SQL view for a fact table (showing grain, joins, window functions).

• Data quality test suite (uniqueness of user_id per period, null thresholds, etc.).

• ER diagrams and partitioning strategy notes.

• Dashboard before/after screenshots and adoption metrics.


## Roles & responsibilities (example)

• Senior Data Analyst: Lead model design, KPI definitions, validation, stakeholder liaison, semantic layer design, and dashboard refactor.

• Data Engineers: Implement and optimise pipelines, set up orchestration, handle infra and performance.

• BI Developer/Analyst: Dashboard development and UX.

• Product Manager / Business Owner: Define business requirements, accept KPIs.

• Data Governance / Compliance: Approve data contracts and retention policies.


## Success metricss

• Accuracy: Reduction in KPI reconciliation issues vs legacy reports (target: 90%+ reconciliation within tolerance).

• Freshness: Time from event ingestion to availability in marts (target SLA e.g., <2 hours for near-real-time domains).

• Adoption: Percentage of leadership dashboards using semantic layer (target: 80% within 3 months).

• Efficiency: Reduction in ad-hoc analyst time spent reconciling (measure via stakeholder survey).

• Quality: Number of data incidents per quarter (target: reduce by X%).


## Common risks & mitigations

• Ambiguous KPI definitions → mitigate with workshops and sign-off gates.

• Performance issues at scale → mitigate by prototyping partitions and query explain plans early.

• Source system changes → mitigate via schema-change alerts and data contracts.

• Adoption resistance → mitigate with change champions, training, and providing “easy wins” dashboards.



