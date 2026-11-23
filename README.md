# Mbongwe Brandon Egbe

**Full-stack engineer in Dubai, UAE.** I build and run backends for payments, fleets and finance: TypeScript, Node.js, NestJS, PostgreSQL, Python, GCP and AWS. Open to full-stack and backend roles (onsite, hybrid or remote).

[Portfolio](https://mbongwe-brandon-egbe.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/mbongwe-brandon-egbe/) · [Email](mailto:mbongweegbe@gmail.com) · GCP Associate Cloud Engineer

---

## Projects

### AutoPartner Gabon: fleet, rent-to-own and GPS tracking platform
**Live:** [autopartner-admin.vercel.app](https://autopartner-admin.vercel.app) · Code private, walkthrough on request

Runs a vehicle rental business in Libreville: rent-to-own contracts, payments, GPS tracking of the fleet, tracker rental to outside clients, and a spare-parts shop.

- **Own tracking server:** GT06 trackers report to a self-hosted Traccar server on AWS. A signed webhook stores each position with speed, ignition, satellites, battery and GSM signal.
- **Live fleet map:** every vehicle on one map with heading, state and its duration ("parked 2 h"), the last 30 minutes of trail, route replay and stop detection.
- **Safe remote immobilization:** engine cut-off is sent only while the vehicle is parked. It counts as done only when the tracker acknowledges it, and every command is audit-logged.
- **Late-payment enforcement:** daily, weekly and monthly payment schedules. Overdue contracts escalate automatically, and the car is released automatically once payment arrives.
- **Tracker rental:** client accounts that only see their own vehicles, monthly invoices, and automatic suspension when unpaid.
- **Parts shop:** public catalogue, cart and orders, stock reserved on confirmation, and a discount for tracking clients.

`TypeScript` `Express` `Prisma` `PostgreSQL` `Next.js` `React Query` `Leaflet` `Traccar` `AWS` `Render` `Vercel`

### NannyLink: global nanny marketplace
**Live:** [joinnannylink.com](https://joinnannylink.com) · Code private, walkthrough on request

Families pay once to unlock a vetted nanny's contact details or to book concierge matching. I designed, built and launched it solo.

- **Postgres Row Level Security:** private contact data reaches only families who paid, were matched, or were granted access by an admin.
- **Stripe and PayPal behind one checkout API:** signed webhooks, fulfillment that is safe to repeat, duplicate-checkout prevention, and correct amounts in zero-, two- and three-decimal currencies.
- **Automated tests:** end-to-end and security suites run against a local Supabase stack in GitHub Actions on every PR.
- **Email notifications:** status emails via database triggers and an Edge Function, with a deduplicated retry queue on `pg_cron`.

`TypeScript` `React` `TanStack Start` `Supabase` `PostgreSQL` `Stripe` `PayPal` `Cloudflare Workers` `GitHub Actions`

### ReceiptVault: VAT-ready receipts for UAE businesses
**Code:** [pentashi/Receipt-vault](https://github.com/pentashi/Receipt-vault)

Staff photograph receipts. ReceiptVault reads the supplier, TRN, 5% VAT and total, flags receipts whose VAT can't be recovered, and gives the accountant a CSV for the quarterly VAT 201 return.

- **Receipt scanning:** Google Cloud Document AI extracts the fields, and foreign-currency totals are converted to AED.
- **Company workspaces:** owner, accountant and staff roles, so one accountant can manage many client companies.
- **VAT quarter view:** VAT 201 box 9 figures and a pre-filing checklist. It also explains why VAT was excluded (missing TRN, entertainment, rejected).

`Python` `Flask` `SQLAlchemy` `PostgreSQL` `React` `TypeScript` `Document AI` `Cloud Storage` `Cloud Run` `Docker`

### CEMAC Accounting Backend (client project)
**Code:** [pentashi/cemac-accounting-backend](https://github.com/pentashi/cemac-accounting-backend)

A modular accounting API for CEMAC/OHADA markets, covering invoices, partners, accounting entries, reporting and audit logs.

- **Auth:** JWT with role-based access, plus OTP codes stored in Redis (in-memory fallback).
- **Audit and data exchange:** audit logging across all modules, and PDF, Excel and CSV export/import.

`NestJS` `TypeORM` `PostgreSQL` `Redis` `Swagger` `Jest`

---

## Experience

**Independent Software Consultant**, AMSIT & AMSI Group · Jul 2024 – present · Remote (China · Cameroon · Gabon)
Backend software for logistics, fleet management and accounting clients, including AutoPartner, CEMAC Accounting and CargoLink (NestJS and Socket.IO shipment tracking API).

**Software Engineering Intern**, ENEO Cameroon · Jul – Sep 2022
Internal recruitment platform: frontend unit tests, system testing and code reviews.

**Education:** BTech Software Engineering, Institut Universitaire de la Côte (2021 – 2024) · **Certification:** Google Cloud Associate Cloud Engineer

## Stack

**Backend:** TypeScript, Node.js, NestJS, Express, Python (Flask), Prisma, TypeORM, SQLAlchemy, PostgreSQL, Redis
**Frontend:** React, Next.js, TanStack, Tailwind CSS
**Cloud:** GCP (Cloud Run, Cloud Build, Document AI, Cloud Storage), AWS, Supabase, Vercel, Render, Docker, GitHub Actions
**Integrations:** Stripe, PayPal, Traccar/GT06 GPS trackers
