# Menu To Go

Public technical portfolio repository for a meal-ordering and operations platform focused on daily menu management, customer orders, kitchen dispatch, balance tracking, finance workflows, and administrative control.

> This is a sanitized public showcase repository. It does not include production source code, credentials, private deployment details, customer data, personal data, database exports, or internal-only assets.

## Executive Summary

Menu To Go represents the architecture and operating model of a service platform used to coordinate recurring meal operations. The product consolidates daily menu setup, order registration, kitchen-facing preparation flows, customer balance visibility, finance controls, and administrative reporting into a single operational system.

This repository is designed to communicate technical judgment, product structure, delivery maturity, and future automation potential without publishing the private production implementation.

## Business Problem

Meal operations for schools, offices, and similar recurring service environments often rely on a patchwork of messages, spreadsheets, ad hoc validations, and manual reconciliation. That operating model creates predictable friction:

| Operational challenge | Typical consequence |
|---|---|
| Orders arrive through multiple channels | Missed requests, duplication, and slower consolidation |
| Daily menu options change frequently | Manual validation and avoidable data-entry mistakes |
| Kitchen and dispatch teams need a single source of truth | Rework in preparation, packing, and handoff |
| Customer balances and payments are tracked separately | Weak reconciliation and reduced financial visibility |
| Admin reporting is assembled manually | Low auditability and delayed decision-making |

## Solution Overview

The platform is organized around a practical operational loop:

1. Configure the menu and service-day context.
2. Register and validate customer orders.
3. Prepare kitchen and dispatch-ready operational views.
4. Reflect charges, payments, and expenses in a finance ledger model.
5. Review dashboards, account state, and operational reporting.
6. Surface automation opportunities for follow-up, anomaly detection, and summaries.

## Functional Modules

| Module | Purpose |
|---|---|
| Daily Ordering | Supports service-day setup, order intake, and operational validation |
| Menu Management | Defines the menu context and available options for each service date |
| Kitchen and Dispatch | Produces consolidated preparation and delivery-oriented views |
| Customer Accounts | Tracks customer balance state and account history conceptually |
| Finance Ledger | Captures payments, charges, expenses, and reporting inputs |
| CRM and Admin Control | Manages customer records, operator workflows, and administrative visibility |
| Reporting and Oversight | Summarizes order activity, finance status, and operational exceptions |

## Technical Architecture Summary

The private system context behind this showcase uses a React/Vite frontend and a Supabase/PostgreSQL backend with role-aware access, database-side controls, and operational workflows across orders, customer balances, finance records, and reporting.

At a conceptual level:

- The frontend provides operator-facing workflows for daily execution.
- Supabase services support authentication, application data, and secured queries.
- PostgreSQL stores operational and finance entities.
- Row Level Security and role-aware access policies help constrain visibility.
- Reporting and automation layers can extend the system without exposing core transactional data publicly.

See [Architecture](./docs/architecture.md) and [System Diagram](./diagrams/system-architecture.mmd).

## Repository Scope and Sanitization Notice

This repository intentionally excludes:

- Production application source code
- Secrets, tokens, API keys, or credentials
- Private environment values or deployment endpoints
- Customer records, phone numbers, addresses, or personal data
- Database dumps, exact production schema, or internal migrations
- Internal-only assets, client-specific files, or confidential reports

The goal is to present system thinking and delivery quality, not to mirror the private implementation.

## Selected Workflows

The showcase centers on the workflows that matter most in daily operations:

- Menu configuration for a service day
- Order registration and validation
- Kitchen preparation and dispatch coordination
- Customer balance updates through ledger-aware events
- Admin review of activity, exceptions, and reporting
- Identification of automation opportunities for summaries, alerts, and intake support

## Technology Stack

| Layer | Technology / Direction |
|---|---|
| Frontend | React, TypeScript, Vite |
| Data platform | Supabase, PostgreSQL |
| Auth and access | Supabase Auth, role-aware access, Row Level Security |
| Operations model | Order management, dispatch views, customer account tracking, finance ledger |
| Reporting direction | Admin dashboards, operational summaries, exception review |
| Automation direction | AI-assisted reporting, anomaly detection, messaging intake, agentic workflows |

## Intended Operational Value

The architecture targets the following operational benefits. These are design goals, not measured outcomes established by this public repository:

- Better traceability from order intake to dispatch
- Cleaner visibility into account state and finance events
- Reduced dependence on manual reconciliation
- Stronger separation between operator workflows and administrative controls
- A foundation for future automation and service operations tooling

## My Role / Contribution

I maintain the public architecture and operational workflow narrative for this project: meal-ordering scope, ledger-aware finance flows, access boundaries, and a sanitized automation roadmap. The public [delivery scope](docs/delivery-scope.md) and [architecture](docs/architecture.md) are the reviewable contribution here; this repository does not establish authorship of every part of the private implementation.

## Evidence / Outcomes

- [Operational workflow](diagrams/operational-workflow.mmd) makes the order-to-dispatch sequence reviewable.
- [Conceptual data model](docs/data-model.md) and [finance ledger flow](diagrams/finance-ledger-flow.mmd) explain the account and finance model.
- [Security notes](docs/security-notes.md) document access and public-data boundaries.

These are qualitative documentation artifacts, not measured adoption, efficiency gains, or independently verified production results. Automation remains a [roadmap](docs/automation-roadmap.md).

## Documentation Index

### Core Docs

- [Architecture](./docs/architecture.md)
- [Conceptual Data Model](./docs/data-model.md)
- [Security Notes](./docs/security-notes.md)
- [Delivery Scope](./docs/delivery-scope.md)
- [Demo Flow](./docs/demo-flow.md)
- [Automation Roadmap](./docs/automation-roadmap.md)

### Diagrams

- [System Architecture Mermaid Source](./diagrams/system-architecture.mmd)
- [Operational Workflow Mermaid Source](./diagrams/operational-workflow.mmd)
- [Finance Ledger Flow Mermaid Source](./diagrams/finance-ledger-flow.mmd)

## Public Portfolio Positioning

This repository is intended for technical portfolio review, architecture discussion, delivery scoping, and product/operations walkthroughs. It is not a public release of the private production application.
