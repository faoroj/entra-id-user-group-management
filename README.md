# Microsoft Entra ID — User & Group Management

## Overview
This repository demonstrates hands-on identity and access administration using Microsoft Entra ID (Azure AD).  
Scope includes user and group management, group-based licensing, and ticket-style troubleshooting scenarios.

## Skills Demonstrated
- User lifecycle management (create, update, disable, restore)
- Security group design and membership testing
- Group-based licensing assignment and validation
- Access verification and common troubleshooting workflows
- Documentation in an IT ticket format (INC-style)

## Lab Environment
- Microsoft Entra ID (Microsoft 365 Developer tenant or test tenant)
- Admin portal: Entra Admin Center
- Test accounts: standard users + admin account
- Optional: Microsoft 365 apps / test SaaS app for access checks

## Project Walkthrough
1. Lab setup: [`docs/00-lab-setup.md`](docs/00-lab-setup.md)
2. User management: [`docs/01-user-management.md`](docs/01-user-management.md)
3. Group management: [`docs/02-group-management.md`](docs/02-group-management.md)
4. Group-based licensing: [`docs/03-group-based-licensing.md`](docs/03-group-based-licensing.md)
5. Access tests: [`docs/04-access-tests.md`](docs/04-access-tests.md)
6. Troubleshooting tickets: [`docs/05-troubleshooting-tickets.md`](docs/05-troubleshooting-tickets.md)

## Ticket Index
- INC-001: User can’t access app (missing group membership) — [`tickets/INC-001-user-cant-access-app.md`](tickets/INC-001-user-cant-access-app.md)
- INC-002: License not applying to user — [`tickets/INC-002-license-not-applying.md`](tickets/INC-002-license-not-applying.md)
- INC-003: Group membership change delay / sync expectation — [`tickets/INC-003-group-membership-delay.md`](tickets/INC-003-group-membership-delay.md)
- INC-004: User disabled / sign-in failure — [`tickets/INC-004-user-disabled-login-failure.md`](tickets/INC-004-user-disabled-login-failure.md)

## Notes
- All user names are test accounts.
- Screenshots are stored under `/evidence/screenshots/`.
  
---

## Repository Structure
```text
entra-id-user-group-management/
├─ README.md
├─ docs/
│  ├─ environment-setup.md
│  ├─ user-management.md
│  ├─ group-management.md
│  ├─ group-based-licensing.md
│  ├─ access-validation.md
│  └─ troubleshooting-overview.md
├─ tickets/
│  ├─ ticket-01-user-cant-access-app.md
│  ├─ ticket-02-license-not-applying.md
│  ├─ ticket-03-group-membership-delay.md
│  └─ ticket-04-user-disabled-sign-in-failure.md
├─ screenshots/
│  ├─ environment/
│  ├─ users/
│  ├─ groups/
│  ├─ licensing/
│  ├─ access-tests/
│  └─ tickets/
│     ├─ ticket-01/
│     ├─ ticket-02/
│     ├─ ticket-03/
│     └─ ticket-04/
└─ templates/
   └─ ticket-template.md

