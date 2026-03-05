# PocketApp Admin Console

An interactive, high-fidelity UI prototype of the internal admin dashboard for **PocketApp** (by Piggyvest). Built to support design validation, stakeholder reviews, and frontend development handoff.

🔗 **[View Live Demo → pmd-admin-prototype.netlify.app](https://pmd-admin-prototype.netlify.app)**

---

## What This Is

This is a single-file HTML prototype of the PocketApp Admin Console — the internal tool used by PocketApp's Operations, Compliance, Finance, and Customer Support teams to manage merchants, review KYC applications, monitor transactions, resolve disputes, and run settlements.

It is **not** a production application. There is no backend, no authentication, and no real data. It is a design prototype intended to communicate product intent, test information architecture, and serve as a reference for engineering implementation.

---

## Why It Was Built

PocketApp is scaling its merchant payment infrastructure in Nigeria. As the merchant base grows, the internal team needed a clearer picture of what the admin tooling should look like before a single line of production code was written.

This prototype was built to:

- **Validate the admin workflow** with internal stakeholders across Operations, Compliance, and CS before committing to engineering effort
- **Explore role-based access control** — different team roles see different actions and data
- **Define the KYC review flow** in detail, including approval, rejection, and return-to-merchant states
- **Communicate design intent** to the engineering team during the build phase
- **Share progress with non-technical stakeholders** via a live URL without requiring a dev environment

---

## Screens & Features

The prototype covers 11 screens navigable via a left sidebar and a prototype nav bar at the top:

| Screen | Description |
|---|---|
| **Overview** | Live dashboard with KPI cards (active merchants, pending KYC, open disputes, today's volume), an activity feed, a My Tasks strip, and role-adaptive widgets |
| **Business List** | Searchable, filterable merchant table with status pills and bulk actions |
| **Business Profile** | Full merchant detail view: info, KYC status, wallet balances, transaction history, risk score, notes, and audit trail |
| **KYC Queue** | List of pending KYC applications with age, risk flags, and quick-action buttons |
| **KYC Detail** | Full KYC review screen with document viewer, director verification, risk assessment, and approve/reject/return modals |
| **Transactions** | Filtered transaction table across all merchants |
| **Transaction Detail** | Individual transaction view with metadata, audit trail, and admin actions (flag, reverse, raise dispute) |
| **Disputes** | Dispute queue with SLA tracking, priority indicators, and assignment |
| **Dispute Detail** | Case management view with merchant and customer claim panels, resolution options, and case activity log |
| **Settlements** | Settlement run tracking with force-settle capability and on-hold management |
| **Settings** | Admin profile, team/roles management, 2FA, and active session control |

---

## Role-Based Access Control

The prototype includes a live role switcher that demonstrates how the UI adapts for five internal roles:

- **Super Admin** — full access to all screens and actions
- **Compliance** — KYC review, business profiles, risk tools
- **Finance & Ops** — settlements, transactions, disputes
- **CS (Customer Support)** — dispute management, transaction lookup
- **Product** — read-only access across all sections

Switching roles dynamically updates sidebar visibility, action availability, KPI cards, and widget content.

---

## Tech Stack

- Pure HTML, CSS, and vanilla JavaScript — no frameworks, no build step
- Single self-contained file (`index.html`)
- Google Fonts (Plus Jakarta Sans)
- Deployed via Netlify (drag and drop)

---

## Project Context

This admin console is part of a broader suite of PocketApp prototypes:

| Prototype | URL | Purpose |
|---|---|---|
| Merchant Dashboard | [pmd-prototype.netlify.app](https://pmd-prototype.netlify.app) | Merchant-facing payments dashboard |
| **Admin Console** | [pmd-admin-prototype.netlify.app](https://pmd-admin-prototype.netlify.app) | Internal admin tooling (this repo) |
| Onboarding Flow | [pmd-onboarding-prototype.netlify.app](https://pmd-onboarding-prototype.netlify.app) | Sign-up, KYC submission, and auth flows |

---

## Status

This is a **v3 prototype**. It is actively used for stakeholder reviews and engineering planning. It is not in production.
