# Architecture Overview

## 1. Architecture Type

The private application follows a single-page application architecture.

```text
Browser Client
     ↓
React + TypeScript Frontend
     ↓
Supabase Client
     ↓
Supabase Auth + PostgreSQL + RLS
```

## 2. Frontend Responsibilities

The frontend handles:

- Authentication screens.
- Role-aware navigation.
- CRM operations.
- Daily menu setup.
- Daily order registration.
- Print / dispatch views.
- Historical reporting views.

## 3. Backend Responsibilities

The backend layer, implemented with Supabase, handles:

- Authentication.
- User profile mapping.
- Role-based access.
- Relational data storage.
- Row Level Security.
- Operational queries.

## 4. Security Design Principles

The private system is designed around the following principles:

- No credentials hardcoded in source code.
- Environment-based configuration.
- Role-based access.
- Restricted access to administrative functions.
- Database-level Row Level Security.
- Manual activation of new users.
- Separation between public showcase and private production code.

## 5. Data Privacy Boundary

The public showcase does not expose:

- Live endpoints.
- Real user records.
- Student information.
- Customer phone numbers.
- Production credentials.
- Internal local paths.
- Operational exports.
