# User Access Review (UAR) Tracker

**Live Demo:** [uar-tracker.chrisolowolafe.workers.dev](https://uar-tracker.chrisolowolafe.workers.dev)  
**Built by:** [Chris Olowo, PMP®](https://chris-olowo-grc-portfolio.pages.dev) — GRC Analyst & Risk Practitioner

---

## Overview

A fully interactive, browser-based User Access Review (UAR) tracker that manages quarterly access certification cycles, enforces Role-Based Access Control (RBAC) governance, and identifies Segregation of Duties (SoD) conflicts — all mapped to ISO 27001:2022, NIST CSF 2.0, and SOC 2 Trust Service Criteria.

---

## Features

### Access Reviews (UAR)
- Add users with department, role, and last access date
- Automated **risk scoring** — Critical / High / Medium / Low based on:
  - Privileged role detection
  - Days inactive (90+ day threshold)
  - Contractor status
  - Revocation flag
- **UAR Decision workflow** — Certify / Pending / Needs Review / Revoke
- **SoD conflict flag** on any user whose role creates a conflict
- Filter by status, search by name/dept/role
- Edit modal with reviewer notes
- Delete individual users or clear all

### Segregation of Duties (SoD) Matrix
- Full **11x11 role conflict matrix** visualizing incompatible role combinations
- Three states: Conflict (✗), Caution (⚠), Acceptable (✓)
- **Active conflicts panel** — lists current users whose roles violate SoD
- ISO 27001, NIST, and SOC 2 control references per conflict

### Report
- Quarterly UAR summary report with completion percentage
- Full user detail table with risk ratings and decisions
- Applicable controls reference block
- Print to PDF / Export CSV

### Sample Data
- One-click demo data loader with 10 realistic users across departments
- Pre-configured to demonstrate SoD conflicts, inactive accounts, and revocation scenarios

---

## SoD Conflict Rules

| Role | Conflicts With |
|---|---|
| Accounts Payable | Accounts Receivable, Finance Manager, Payroll Manager, Manager/Approver |
| Accounts Receivable | Accounts Payable, Finance Manager, Payroll Manager |
| Payroll Manager | Accounts Payable, Accounts Receivable, HR Manager, Finance Manager |
| Finance Manager | Accounts Payable, Accounts Receivable, Payroll Manager, Auditor |
| System Administrator | Auditor, Developer |
| Database Administrator | Auditor, Developer |
| Developer | System Administrator, Database Administrator, Auditor |
| Auditor | Finance Manager, Sys Admin, DB Admin, Developer, Payroll Manager |
| HR Manager | Payroll Manager |
| Manager / Approver | Accounts Payable |

---

## Framework Coverage

| Framework | Controls |
|---|---|
| ISO 27001:2022 | A.5.15, A.5.16, A.6.5, A.8.2 |
| NIST CSF 2.0 | PR.AC-01, PR.AC-04, PR.AC-05 |
| SOC 2 Type II | CC6.2, CC6.3 |

---

## Security Architecture

All security headers enforced server-side via Cloudflare `_headers`:

| Header | Value |
|---|---|
| `X-Frame-Options` | `DENY` |
| `X-Content-Type-Options` | `nosniff` |
| `Referrer-Policy` | `strict-origin-when-cross-origin` |
| `Strict-Transport-Security` | `max-age=63072000; includeSubDomains; preload` |
| `Content-Security-Policy` | Strict allowlist |
| `Permissions-Policy` | Geolocation, microphone, camera, payment denied |

Additional controls:
- HTTPS enforcement via JavaScript
- GitHub Pages → Cloudflare Pages canonical redirect
- Chart.js loaded with SRI integrity hash
- Chart.js safety stub IIFE
- All user input HTML-escaped (XSS prevention)
- `localStorage` wrapped in try/catch
- `prefers-reduced-motion` respected
- No cookies, no tracking, no analytics
- All data stored exclusively in `localStorage`

---

## Repository Structure

```
user-access-review-tracker/
├── index.html    ← Full application
├── _headers      ← Cloudflare security headers
└── README.md     ← This file
```

---

## Running Locally

```bash
git clone https://github.com/chrisolowolafe-sys/user-access-review-tracker.git
cd user-access-review-tracker
open index.html
```

---

## Part of the GRC Portfolio

| Project | Status |
|---|---|
| [ShomriTech GRC Platform](https://chris-olowo-grc-portfolio.pages.dev/grc-platform) | ✅ Live |
| [Vendor Risk Assessment Tool](https://vendor-risk-assessment-tool.chrisolowolafe.workers.dev) | ✅ Live |
| **User Access Review (UAR) Tracker** *(this repo)* | ✅ Live |
| SOC 2 Evidence Tracker | Coming soon |
| NIST AI RMF Gap Assessment | Coming soon |

---

## Author

**Chris Olowo, PMP®**  
GRC Analyst & Risk Practitioner · Calgary, Canada  
ISO 27001 Lead Auditor · NIST CSF 2.0 · GRC · PrivacyOps · ISO 42001

[Portfolio](https://chris-olowo-grc-portfolio.pages.dev) · [LinkedIn](https://www.linkedin.com/in/chris-o-742316135)

---

*For demonstration and educational purposes only. Not a certified compliance platform or legal service.*
