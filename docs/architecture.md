# Architecture

## Purpose

This document describes the public, conceptual architecture of Menu To Go. It is intentionally abstracted to explain the technical shape of the system without disclosing private code, exact infrastructure identifiers, or internal implementation details.

## High-Level Architecture

Menu To Go is best understood as an operations platform with a web application layer, a secured data platform, and a reporting/automation extension layer.

```text
Personas
  -> React/Vite application
  -> Auth, data access, and service workflows
  -> PostgreSQL-backed operational records
  -> Reporting and automation extensions
```

The system supports multiple operational perspectives rather than a single generic user journey. Admin, operations, kitchen/dispatch, and finance users all interact with different views over the same service workflow.

## Frontend Layer

The frontend is a React/Vite application oriented around fast operational execution.

Primary concerns include:

- Daily menu configuration
- Order registration and validation
- Kitchen and dispatch visibility
- Customer account and balance review
- Finance and admin workflows
- Role-aware navigation and screen access

The frontend is expected to prioritize:

- Fast data entry for repetitive daily work
- Clear service-day context
- Low-friction review of status changes
- Views that can support printing or dispatch-oriented use cases

## Backend and Data Layer

The conceptual backend uses Supabase and PostgreSQL as the application data platform.

Responsibilities include:

- Authentication and user identity
- Access control and role-aware authorization
- Storage of operational entities such as orders, menus, customer records, and ledger events
- Query support for dashboards and reporting
- Secure data access patterns using Row Level Security and scoped permissions

The data layer should be treated as both the transaction system for operations and the source of truth for reporting inputs.

## Operational Modules

The architecture aligns around a set of business modules rather than around purely technical domains.

| Module | Architectural role |
|---|---|
| CRM / Customer Records | Maintains customer and account context used across operations |
| Menu Management | Defines service-day offerings and orderable options |
| Order Operations | Captures daily requests and tracks fulfillment state |
| Kitchen / Dispatch | Presents consolidated preparation and handoff views |
| Customer Balance | Connects order activity, payments, and account state |
| Finance Ledger | Records payments, charges, expenses, and reporting events |
| Admin and Reporting | Supports review, oversight, and role-aware operational control |

## Integration Points

The public repository does not include live integrations, but the conceptual design suggests several extension points:

- Payment capture or reconciliation workflows
- Messaging intake for structured order registration
- Admin dashboard reporting
- Automation or ticketing systems for follow-up actions
- Export or reporting surfaces for finance and service operations

These integrations should be designed around strong access boundaries and event traceability rather than direct, uncontrolled data movement.

## Deployment Considerations

For a private production implementation, deployment concerns would typically include:

- Environment-based configuration
- Separation of public frontend configuration from privileged backend secrets
- Controlled database access
- RLS policy validation
- Backup and recovery readiness
- Monitoring for operational errors, data drift, and access issues

The public portfolio repository deliberately omits deployment endpoints, project identifiers, and environment configuration values.

## Suggested Future Architecture

A future-state evolution could add clearer separation between transaction workflows and asynchronous operational intelligence.

Potential directions:

- Event-oriented ledger and reporting pipelines
- Scheduled jobs for daily summaries and anomaly checks
- Ticketing flows for operational exceptions
- Messaging ingestion services for structured order capture
- AI-assisted narrative summaries for operations and finance review
- Dedicated service boundaries for reporting and automation workloads

This future architecture can remain compatible with a React frontend and a Supabase/PostgreSQL core, while introducing a more explicit orchestration layer for background work.

## Mermaid Diagram Reference

The architecture diagram for this document is available here:

- [System Architecture Diagram](../diagrams/system-architecture.mmd)

Use the diagram together with this document to explain the relationship between user roles, application workflows, security controls, and automation opportunities.
