# User Access Review (UAR) Tracker

**Live Demo:** [user-access-review-tracker.pages.dev](https://user-access-review-tracker.pages.dev)  
**Built by:** [Chris Olowo, PMP®](https://chris-olowo-grc-portfolio.pages.dev) — GRC Analyst & Risk Practitioner

---

## Overview

A fully interactive, browser-based User Access Review (UAR) tracker that manages quarterly access certification cycles, enforces Role-Based Access Control (RBAC) governance, and identifies Segregation of Duties (SoD) conflicts — all mapped to ISO 27001:2022, NIST CSF 2.0, and SOC 2 Trust Service Criteria.

---

## Features

### Access Reviews (UAR)
- Add users with department, role, and last access date
- Automated **risk scoring** — Critical / High / Medium / Low
- **UAR Decision workflow** — Certify / Pending / Needs Review / Revoke
- **SoD conflict flag** on any user whose role creates a conflict
- Filter by status, search by name/dept/role
- Edit modal with reviewer notes

### Segregation of Duties (SoD) Matrix
- Full **11×11 role conflict matrix**
- Three states: Conflict (✗), Caution (⚠), Acceptable (✓)
- **Active conflicts panel** — lists current users with SoD violations

### Report
- Quarterly UAR summary with completion percentage
- Full user detail table with risk ratings and decisions
- Print to PDF / Export CSV

---

## Framework Coverage

| Framework | Controls |
|---|---|
| ISO 27001:2022 | A.5.15, A.5.16, A.6.5, A.8.2 |
| NIST CSF 2.0 | PR.AC-01, PR.AC-04, PR.AC-05 |
| SOC 2 Type II | CC6.2, CC6.3 |

---

## Security Architecture

All security headers enforced server-side via Cloudflare `_headers`. Additional: HTTPS enforcement, GitHub Pages redirect, Chart.js SRI, safety stub, XSS prevention, localStorage try/catch, prefers-reduced-motion, no tracking.

---

## Repository Structure

```
user-access-review-tracker/
├── index.html    ← Full application
├── _headers      ← Cloudflare security headers
└── README.md     ← This file
```

---

## Complete GRC Portfolio

| Project | Live URL |
|---|---|
| 🏠 ShomriTech GRC Platform | [chris-olowo-grc-portfolio.pages.dev](https://chris-olowo-grc-portfolio.pages.dev) |
| 1️⃣ Vendor Risk Assessment Tool | [vendor-risk-assessment-tool.pages.dev](https://vendor-risk-assessment-tool.pages.dev) |
| 2️⃣ **User Access Review Tracker** *(this repo)* | [user-access-review-tracker.pages.dev](https://user-access-review-tracker.pages.dev) |
| 3️⃣ SOC 2 Evidence Tracker | [soc2-evidence-tracker.pages.dev](https://soc2-evidence-tracker.pages.dev) |
| 4️⃣ NIST AI RMF Gap Assessment | [nist-ai-rmf-assessment.pages.dev](https://nist-ai-rmf-assessment.pages.dev) |
| 5️⃣ Security Questionnaire Library | [security-questionnaire-library.pages.dev](https://security-questionnaire-library.pages.dev) |

---

## Author

**Chris Olowo, PMP®**  
GRC Analyst & Risk Practitioner · Calgary, Canada  
ISO 27001 Lead Auditor · NIST CSF 2.0 · ISO 42001 · GRC · PrivacyOps · PMP®

*Pro bono ISO 42001 AI governance consulting provided to non-profit organizations in Calgary.*

[Portfolio](https://chris-olowo-grc-portfolio.pages.dev) · [LinkedIn](https://www.linkedin.com/in/chris-o-742316135) · [GitHub](https://github.com/chrisolowolafe-sys)

---

*For demonstration and educational purposes only. Not a certified compliance platform or legal service.*
