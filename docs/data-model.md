# Conceptual Data Model

## Scope

This document presents a conceptual data model for the public showcase repository. It is not the private production schema and should not be interpreted as a direct database export, table map, or migration reference.

## Modeling Principles

- Represent business entities at a high level
- Show relationships needed to explain operations
- Preserve finance and account logic conceptually
- Avoid exact production table names, column names, or internal implementation details

## Core Entities

| Entity | Purpose |
|---|---|
| Customer | Represents the person or account receiving meal service |
| Menu | Defines the service-day offering and available meal options |
| Order | Captures a meal request tied to a customer and service date |
| Payment | Records money received or acknowledged for account settlement |
| Ledger Transaction | Represents a finance event such as a charge, payment, adjustment, or expense |
| Purchase / Expense | Tracks business spending related to operations |
| Admin User | Represents a privileged operational or administrative actor |
| Dispatch View | Represents an operational projection of orders for preparation and handoff |

## Supporting Concepts

Additional supporting concepts are often needed even in a simplified model:

- Service date
- Order status
- Payment status
- Customer balance
- Role or permission scope
- Menu components or item selections
- Operational notes or exceptions

## Conceptual Relationships

| From | Relationship | To |
|---|---|---|
| Customer | places | Order |
| Menu | is used to validate | Order |
| Order | may generate | Ledger Transaction |
| Payment | may generate | Ledger Transaction |
| Purchase / Expense | may generate | Ledger Transaction |
| Ledger Transaction | contributes to | Customer balance or business reporting |
| Admin User | manages | Menu, Order, Finance, and Reporting workflows |
| Dispatch View | summarizes | Order data for kitchen and delivery operations |

## Example Conceptual Flow

```text
Customer
  -> Order
  -> Order charge ledger event
  -> Customer balance update

Payment
  -> Payment ledger event
  -> Customer balance update

Purchase / Expense
  -> Expense ledger event
  -> Admin finance reporting
```

## Ledger and Accounting Logic

At a conceptual level, the finance layer is event-based rather than purely status-based.

- Orders can create charge events.
- Payments can create settlement events.
- Adjustments can correct account state without mutating historical records silently.
- Purchases and expenses can feed operational finance reporting.
- Customer balance is best treated as a computed or traceable result of ledger activity, not just a manual field overwrite.

This approach improves auditability and makes downstream reporting more reliable.

## Entity Notes

### Customer

Represents the party whose service usage and account state need to be tracked over time. In a real system, this may be linked to institution, group, route, or operational classification, but those details are intentionally generalized here.

### Order

Represents a service-day request. Important conceptual fields include the service date, selected option, status, and association with the customer and menu context.

### Menu

Represents the set of orderable options for a specific date or service window. It acts as the business context for valid order capture.

### Payment

Represents funds received or confirmed for account settlement. It should remain traceable and associated with related finance reporting.

### Ledger Transaction

Represents the canonical finance event used to explain charges, payments, adjustments, or expenses. This entity is especially useful when discussing balance visibility and reporting maturity.

### Purchase / Expense

Represents internal operational spending that may need categorization, reconciliation, and reporting, even if it does not map directly to customer accounts.

### Admin User

Represents operators with privileged access to configuration, oversight, review, and exception handling.

### Dispatch View

Represents a derived operational view rather than a single stored business fact. It exists to help kitchen and dispatch teams act on the order set for a given service period.

## Privacy and Exposure Boundary

This document intentionally avoids:

- Exact production schema names
- Real identifiers or primary key conventions
- Sensitive attributes
- Customer or institution data examples
- Private finance record structures
- Migration or export-level details

The purpose is to explain the product and system design, not to reveal the private implementation.
