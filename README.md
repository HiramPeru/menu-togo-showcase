# Almuerzo To Go — Menu & Order Operations Showcase

A private operational web application designed to manage daily lunch menus, customers, orders, payment status, and dispatch reporting for school and office meal delivery operations.

> This repository is a public showcase. It does not contain production source code, credentials, customer records, student data, phone numbers, private deployment URLs, or operational databases.

## 1. Product Overview

**Almuerzo To Go** centralizes the daily workflow of a lunch delivery operation that would otherwise depend on WhatsApp messages, spreadsheets, manual consolidation, and fragmented records.

The system helps operators manage:

- Institutions or companies.
- Locations or branches.
- Diners / customers.
- Daily menus.
- Food components.
- Daily orders.
- Payment status.
- Operational status.
- Historical order review.
- Print-ready kitchen and dispatch views.

## 2. Business Problem

Food delivery operations for schools and offices usually face recurring issues:

| Problem | Operational Impact |
|---|---|
| Orders arrive through multiple WhatsApp conversations | High risk of omissions and duplicate records |
| Customer information lives in spreadsheets | Manual updates, low traceability, weak reporting |
| Menus change daily | Operators must constantly validate available options |
| Payment tracking is separated from order tracking | Increased reconciliation effort |
| Kitchen and dispatch teams need consolidated views | Manual copy/paste and printing errors |
| Historical records are difficult to audit | Poor visibility into demand, volume, and recurring customers |

## 3. Solution Summary

The application provides a structured operating panel for the full daily meal order cycle:

```text
Customer Master Data
        ↓
Daily Menu Configuration
        ↓
Daily Order Registration
        ↓
Payment / Order Status Tracking
        ↓
Kitchen & Dispatch View
        ↓
Historical Review
```

## 4. Core Modules

### 4.1 CRM

Manages the master records used by the operation:

- Institutions / companies.
- Locations / branches.
- Diners / customers.
- Subscription status.
- Classroom, department, or group references when applicable.

### 4.2 Food Components

Maintains a reusable catalog of meal components:

- Main protein.
- Side dish.
- Base.
- Starter.
- Dessert.
- Beverage.

This avoids typing the same dishes repeatedly and reduces naming inconsistencies.

### 4.3 Daily Menu

Defines which components are available for a specific service date.

Operators can configure the menu before receiving or registering orders.

### 4.4 Daily Orders

Registers each order linked to:

- Service date.
- Diner / customer.
- Selected menu components.
- Payment status.
- Operational order status.

### 4.5 Print / Dispatch View

Provides a consolidated view for kitchen preparation, packing, and delivery review.

### 4.6 History

Allows review of past orders and supports operational auditing.

### 4.7 Admin

Handles user activation and access roles.

## 5. Access Model

The private application uses authenticated access and role-based permissions.

| Role | Scope |
|---|---|
| Admin | Full access, user activation, structural management |
| Operator | Daily operation, order registration, menu handling, CRM usage |

New accounts require administrative activation before accessing the system.

## 6. Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React, TypeScript, Vite |
| UI | Custom CSS |
| Backend / Database | Supabase PostgreSQL |
| Authentication | Supabase Auth |
| Authorization | Role-based access and Row Level Security |
| Deployment | Private cloud deployment |

## 7. Security & Privacy Position

This showcase intentionally excludes:

- Production source code.
- Environment files.
- API keys.
- Supabase project URLs.
- Supabase anonymous or service-role keys.
- Private deployment URLs.
- Customer names.
- Student names.
- Phone numbers.
- Institution-specific operational datasets.
- Local development paths.
- Internal workspace paths.
- Screenshots containing real operational data.

## 8. Data Model — Conceptual View

```text
Institution
    └── Location
            └── Diner / Customer
                    └── Daily Order
                            ├── Menu Date
                            ├── Selected Components
                            ├── Payment Status
                            └── Operational Status
```

## 9. Operational Status Examples

### Payment Status

- Pending
- Paid
- Exempted
- Cancelled

### Order Status

- Registered
- Prepared
- Delivered
- Cancelled

## 10. Product Roadmap

Planned improvements include:

- Daily dashboard with order volume and payment status.
- Excel / PDF export.
- WhatsApp-assisted order intake.
- Costing and margin module.
- Demand forecasting by weekday and institution type.
- Automated payment reminders.
- Role-specific dashboards.
- Kitchen production summaries.
- Mobile-first operator experience.
- Audit trail for sensitive changes.

## 11. Portfolio Relevance

This project demonstrates applied experience in:

- Business process digitization.
- Small-business operations automation.
- CRM-style data modeling.
- Food service workflow design.
- Role-based access design.
- React / TypeScript frontend architecture.
- Supabase-backed application development.
- Operational UX for non-technical users.
- AI-assisted software iteration and refactoring.

## 12. Repository Scope

This repository is only a public-facing portfolio showcase.  
The production codebase remains private.
