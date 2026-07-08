# Demo Flow

## Purpose

This walkthrough is designed for a public-facing demo of the Menu To Go concept. It explains how to narrate the product without requiring access to production data or private source code.

## Personas

| Persona | Primary interest |
|---|---|
| Admin | Configuration, oversight, access control, reporting |
| Kitchen / Dispatch | Preparation readiness and consolidated order views |
| Finance / Admin | Balance updates, ledger activity, expenses, reporting |
| Customer / Operator | Order registration, account context, service-day execution |

## Suggested Demo Walkthrough

### 1. Configure Daily Menu and Order Context

Start by explaining that each service day needs a valid operating context:

- The menu must be defined for the day
- Available options must be clear before order capture begins
- Operators need a stable service-date frame to reduce mistakes

This establishes the business rule that order entry depends on an active menu context.

### 2. Register an Order

Move to the order-entry perspective:

- An operator selects or identifies the customer
- The order is registered against the active menu
- Status and account context can be reviewed at the point of entry
- The workflow aims to reduce fragmented order intake and manual consolidation

This is the moment to emphasize operational clarity over generic e-commerce behavior.

### 3. Prepare the Kitchen and Dispatch View

Next, explain how transactional order data becomes an operational view:

- Orders for the service window are consolidated
- Kitchen staff need a preparation-oriented projection
- Dispatch or packing teams need a handoff-ready view
- The system reduces copy/paste coordination and improves service readiness

This helps stakeholders understand why the product supports both data entry and operational execution.

### 4. Update the Financial Ledger and Customer Balance

Then shift to finance logic:

- Orders can create charge-side ledger events
- Payments can create settlement-side ledger events
- Expenses may feed internal finance reporting
- Customer balance is interpreted from finance activity rather than only from a manual status label

This is an important differentiator because it shows a more mature operations model.

### 5. Review Dashboard and Admin Reports

Show how leadership or administrators would use the system:

- Review service-day activity
- Check exceptions, pending balances, or unusual finance patterns
- Monitor operational completion
- Use summarized views instead of reconstructing the day manually

The key message is that reporting is part of the operating system, not an afterthought.

### 6. Identify Automation Opportunities

Close the demo with forward-looking but credible opportunities:

- Daily operational summaries
- Exception and anomaly alerts
- Customer balance reminders
- Ticket generation for unresolved issues
- Structured messaging intake for future order capture support

Frame these as natural extensions of the system design rather than as marketing claims.

## Demo Guidance

For public presentations:

- Use conceptual language
- Avoid showing real data
- Avoid implying that the repository is the production application
- Focus on architecture, workflow design, and operational maturity
- Use the diagrams and docs to support the narrative
