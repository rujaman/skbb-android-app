# SKBB Master Plan

## Roles
- Guest: public information, approved donor search, submit blood request.
- Registered User/Donor: manage own profile, donor registration/consent, track own requests.
- Admin: review requests, manage donor records, notices and operations.
- Super Admin: user roles, access policy, organization settings, audit review.

## Modules
1. Public home, organization info and notices
2. Donor directory and consent-aware availability
3. Blood requests and matching workflow
4. Committee and member management
5. Finance: contributions, donations, income, expenses, balances
6. Reports and exports
7. Role management, audit logs, settings and backups
8. Notifications and Android packaging

## Proposed data entities
profiles, donors, blood_requests, donor_matches, committee_members, fund_transactions, notices, audit_logs.

## Security requirements
- Row-level security on private tables.
- Never expose patient contact details or donor phone numbers to anonymous visitors.
- Backend/database enforces role permissions; hiding UI controls is not security.
- Service-role keys stay server-side.
- Collect minimum necessary personal information and record consent.

## Demo data
All numbers and donor/request records in V1 are illustrative. Replace them with database queries before public launch.