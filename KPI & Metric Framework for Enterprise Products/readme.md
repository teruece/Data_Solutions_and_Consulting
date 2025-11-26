## KPI & Metric Framework for Enterprise Products — Maximus UK


Delivered an enterprise KPI & Metric Framework, standardising definitions across Maximus UK, eliminating conflicting reports, and enabling trusted, production-ready metrics powering leadership dashboards, operational decision-making and AI-readiness across core business domains.

## Project Description

The KPI & Metric Framework initiative at Maximus UK was designed to eliminate inconsistent metric definitions, improve reporting accuracy, and create a standardised, governed set of enterprise-wide KPIs. These KPIs underpin operational dashboards, product analytics, performance reporting, and strategic decision-making across People, Operations, Contract Performance, and Digital Products.

The programme established a unified methodology for defining, calculating, governing, and publishing KPIs—replacing spreadsheets, inconsistent SQL logic, and domain-specific interpretations. By building a single approved metric glossary, validated SQL logic, and a robust semantic layer, the framework enabled trustworthy reporting, scalable analytics, and readiness for advanced forecasting and AI/ML initiatives.

## Core Objectives

• Standardise KPI definitions across all business units and product teams.

• Translate business concepts into precise, production-ready metric logic.

• Create a Single Source of Truth (SSOT) for all metrics used in dashboards and reporting.

• Align stakeholders (Product, Operations, HR, Finance) around consistent measurement.

• Reduce manual interpretation and conflicting reports by embedding governance and documentation.

• Build SQL-based metric views and a semantic layer consumable by Power BI and BI tools.

• Ensure KPI logic is AI-ready — complete, reproducible and historically consistent.


## Scope

Included KPI domains:
• People Analytics (Attrition, Hiring Velocity, Absence, Tenure)
• Operational Performance (Case Volumes, SLA Compliance, Time-to-Outcome)
• Service/Product Metrics (Digital adoption, User engagement, Process throughput)
• Contract & Financial KPIs (Performance thresholds, Payment triggers)

Excluded: Tactical, non-standardised operational metrics used only temporarily for local processes.

## Phased Step-By-Step Approach

PHASE 0 — Foundation & Governance Setup

• Identify KPI owners, data stewards and approval governance.

• Agree the purpose, scope, retention rules and change-control process.

• Define acceptance criteria for a KPI to be approved (accuracy, reproducibility, data quality).

• Deliverables: Governance charter, RACI, prioritised KPI backlog.


PHASE 1 — Discovery & Current-State Assessment

• Catalogue existing KPI definitions across departments, dashboards and SQL logic.

• Identify conflicting calculations, missing documentation and manual workarounds.

• Profile underlying datasets: completeness, timing, granularity issues impacting metric reliability.

• Map downstream consumers (BI dashboards, operational tools, leadership reports).

• Deliverables: Discovery log, duplicate/variant KPIs list, current-state lineage map.


PHASE 2 — Business Definition & Alignment Workshops

• Run workshops with business leads to clarify meaning, use cases and intended decision value.

• Define business logic: inclusion/exclusion rules, grain, filters, windows, time periods.

• Create draft KPI definitions with diagrams, examples and edge-case handling.

• Resolve disagreements through structured comparison and example reconciliation.

• Deliverables: KPI definition sheets, business logic documentation, approval notes.


PHASE 3 — Technical Specification & SQL Logic Development

• Convert definitions into technical specifications:


* Required tables

* Required joins
  
* Date/period logic
  
* Window/aggregation logic
  
* Denominator/numerator rules
  
  • Develop validated SQL for each KPI in the warehouse (BigQuery or equivalent).

  • Create reference tables (date dimension, status mapping, events).
  
  • Perform reconciliation with historic reports; ensure results match within tolerance.
  
  • Deliverables: Technical spec pack, SQL scripts, reconciliation results.
  

PHASE 4 — Metric Modelling & Semantic Layer Build

• Build metric-level views (dbt models or SQL views) for production use.

• Apply naming standards, metadata tags and lineage mapping.

• Add automated tests:

* Non-negative values
  
* Freshness checks
  
* Null thresholds
  
* Consistency across periods
  
  • Publish metrics to a semantic layer for Power BI / Looker consumption.

  • Deliverables: Metric marts, semantic layer dataset, automated tests.


PHASE 5 — Dashboard Integration & Uplift

• Refactor Power BI dashboards to use the new KPI semantic model.

• Add drill-downs and slice-by dimensions (team, region, cohort, time).

• Ensure role-based access is applied.

• Validate results with stakeholders before replacing legacy dashboards.

• Deliverables: Updated dashboards, validation evidence, user acceptance sign-off.


PHASE 6 — Training, Documentation & Rollout

• Create documentation: definitions, logic, query examples, change control.

• Run training sessions for analysts, PMs, operations leads and leadership teams.

• Provide cheat sheets for correct interpretation and usage.

• Deliverables: Glossary, user guides, training decks, KPI catalogue.


PHASE 7 — Ongoing Governance & Continuous Improvement

• Monthly governance meetings to review new KPI requests and proposed changes.

• Monitor data quality metrics and escalate issues to data owners.

• Incorporate new product or process changes into KPIs.

• Maintain version control to track revisions and prevent metric drift.

• Deliverables: KPI change log, quality dashboard, version-controlled glossary.






