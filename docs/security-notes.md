# Security Notes

## Purpose

This document explains the security posture and sanitization principles for the public Menu To Go portfolio repository. It describes what must remain excluded and what security concerns matter in the private operational system.

## Public Repository Sanitization Principles

The public repository is intentionally limited to documentation, conceptual diagrams, and non-sensitive portfolio material.

It must not include:

- Secrets, API keys, or tokens
- Production credentials or authentication material
- Private deployment URLs or environment values
- Customer records or personal data
- Operational exports or database dumps
- Exact internal schema details that are not needed for portfolio explanation
- Internal-only assets, screenshots with real data, or confidential documents

## No Secrets, No Credentials, No Production Data

The most important public-repo rule is simple: no live operational material should ever be committed.

That includes:

- Frontend environment values with real endpoints
- Service-role credentials
- Admin-only access artifacts
- Production SQL exports
- Screenshots containing real names, phone numbers, balances, or order history

If sample data is ever added, it should be intentionally fake, minimal, and clearly marked as demo-only.

## Supabase and RLS Considerations

A Supabase/PostgreSQL implementation introduces several important security considerations:

- Separate unprivileged client access from privileged backend or admin actions
- Use Row Level Security to constrain which records a role can read or change
- Review policies with the same rigor as application code
- Avoid assuming frontend role checks are sufficient
- Ensure finance and admin workflows have tighter access boundaries than general operations

In a system like this, RLS is not only a database feature but a core part of the application trust model.

## Access Control Considerations

Operational systems with multiple personas need more than simple authenticated access.

Important concepts include:

- Role-aware screen access
- Scoped permissions for admin workflows
- Restricted finance visibility
- Separation between operational data entry and sensitive oversight functions
- Audit-friendly handling of privileged actions

A public showcase should communicate that access control is part of the system design even when the policies themselves remain private.

## Backup and Disaster Recovery Considerations

Even a modest operations platform should plan for:

- Reliable database backups
- Recovery testing
- Controlled restoration procedures
- Documentation for service continuity
- Clear ownership of production recovery steps

The public repository should discuss these practices conceptually without exposing provider details, backup schedules, or recovery credentials.

## Auditability Considerations

Operational and finance workflows become safer when the system favors traceable events over silent overwrites.

Auditability benefits from:

- Ledger-style finance events
- Clear user attribution for admin actions
- Timestamped state transitions
- Reviewable reporting inputs
- Exception tracking for unusual changes

This is especially important where customer balances, payments, expenses, or administrative overrides are involved.

## Security Roadmap

Reasonable future security improvements could include:

- Stronger review of RLS policies and role boundaries
- More explicit audit logging for sensitive workflows
- Better separation of privileged automation from user-facing actions
- Periodic repository sanitization checks
- Safer demo-data generation and screenshot workflows
- Monitoring and alerting for suspicious finance or admin activity

## Public Repository Position

This repository is safe for public sharing only insofar as it remains a sanitized, documentation-first technical portfolio. The private production application should continue to enforce its own operational security, access control, backup, and data governance practices outside this repository.
