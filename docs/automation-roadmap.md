# Automation Roadmap

## Purpose

This roadmap outlines credible automation directions for Menu To Go without overstating current implementation. It focuses on operational leverage, auditability, and service reliability.

## AI-Assisted Operational Reporting

One of the clearest automation opportunities is turning operational data into readable daily summaries.

Examples of useful outputs:

- Service-day order summary
- Pending or unusual balance overview
- Payment and expense exception digest
- End-of-day admin narrative for follow-up actions

The value is not only speed, but also consistency in how the operation is reviewed.

## Ticket and Incident Workflow

Operational issues often become easier to manage when they are converted into trackable work items.

Potential ticket triggers include:

- Missing payment confirmation
- Dispatch mismatch
- Repeated order correction
- Expense record inconsistency
- Access or role-related incidents

This creates a bridge between transactional operations and service management discipline.

## Automated Customer Balance Summaries

Customer account communication can become more structured through scheduled or event-based summaries.

Potential uses:

- Periodic balance snapshots
- Reminder workflows for unresolved balances
- Operator-facing account review notes
- Internal finance queues for follow-up

Any implementation should respect privacy controls and role-aware access boundaries.

## Anomaly Detection for Payments, Orders, and Expenses

The platform is a good candidate for rules-based and AI-assisted anomaly detection.

Conceptual checks could include:

- Orders without expected finance events
- Payments that do not reconcile cleanly
- Unusual expense patterns
- Duplicate or conflicting service-day entries
- Sudden shifts in order composition that merit review

These checks do not require exaggerated AI claims; they can begin with strong operational rules and evolve over time.

## WhatsApp or Messaging Ingestion as a Future Workflow

Message-based intake is a natural future direction for recurring meal operations.

Conceptually, the workflow could:

- Ingest structured or semi-structured messages
- Extract customer, date, and order intent
- Flag ambiguities for operator review
- Convert validated requests into operational records

The public portfolio should present this as a future workflow concept rather than as a claim about the current repository contents.

## SLA and Service Operations Alignment

As the platform matures, automation should align with simple service operations expectations:

- Daily readiness checks
- Timely review of unresolved tickets
- Response expectations for finance and dispatch issues
- Clear ownership for exceptions and escalations

This helps position the platform as an operational system rather than only a CRUD interface.

## Agentic Workflow Possibilities

An agentic layer could support coordination across documentation, reporting, and exception handling.

Relevant ecosystem directions may include:

- ChatGPT for summaries, drafting, and operator copilots
- Claude for synthesis, policy review, or workflow narration
- Codex, OpenCode, or Antigravity for implementation support and repository operations
- MCP-based tooling for safer access to structured systems
- OpenRouter for model-routing experiments where appropriate
- Local models for privacy-sensitive or offline analysis workflows
- Automation tools for scheduled reports, message parsing, and incident orchestration

These are best framed as enabling tools in a broader operations architecture, not as product claims by themselves.

## Suggested Rollout Approach

| Phase | Focus |
|---|---|
| Phase 1 | Rules-based summaries, alerts, and recurring admin digests |
| Phase 2 | Ticketing workflows and finance/account follow-up automation |
| Phase 3 | Messaging ingestion and exception classification |
| Phase 4 | Agentic orchestration across reporting, review, and operational triage |

## Portfolio Position

This roadmap shows that the platform can evolve into a more automated operating system while remaining grounded in practical workflows, security boundaries, and auditable business logic.
