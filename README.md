# Samaj Kallyan Blood Bank — V1 UI Prototype

A responsive React + Vite frontend starter with the organization logo, guest/user flows, donor search, blood request form, admin dashboard preview, and planned finance/committee/report sections.

## Run
Requires Node.js 20+.
```bash
npm install
npm run dev
```
Build with `npm run build`.

## Important
This is a UI prototype. It uses illustrative sample records and browser-only demo state. Login is not real authentication, and no database is connected yet. Do not use it for real patient or donor data until Supabase authentication, row-level security, role checks, consent handling, and testing are implemented.

## Planned delivery
1. Finish UI and flows.
2. Implement secure Supabase schema and RLS.
3. Add Guest, User, Admin, Super Admin roles enforced by backend.
4. Connect donor and request workflows.
5. Add finance, committee, reports, audit logs and notifications.
6. Test privacy/security and deploy.
7. Package Android using Capacitor and GitHub Actions.

Never commit service-role keys or secrets.