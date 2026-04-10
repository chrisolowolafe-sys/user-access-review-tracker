# Vendor Security Risk Assessment Tool

**Live Demo:** [vendor-risk-assessment-tool.pages.dev](https://vendor-risk-assessment-tool.pages.dev)  
**Built by:** [Chris Olowo, PMP®](https://chris-olowo-grc-portfolio.pages.dev) — GRC Analyst & Risk Practitioner

---

## Overview

A fully interactive, browser-based third-party vendor security risk assessment tool that evaluates supplier security posture across **6 domains** and **29 weighted questions**, mapped to ISO 27001:2022 controls, NIST CSF 2.0 functions, SOC 2 Trust Service Criteria, GDPR Article 28, and PIPEDA.

Generates a **risk-rated report** (Critical / High / Medium / Low) with domain breakdowns, detailed findings, recommended risk treatments, and control references. All data is stored locally in the browser — nothing leaves your device.

---

## Features

- **6 Security Assessment Domains** — Data Security, Access Controls, Incident Response, Business Continuity, Compliance & Regulatory, Third-Party Sub-processors
- **29 Weighted Questions** — each mapped to specific framework controls
- **Automated Risk Scoring Engine** — weighted scoring with risk thresholds
- **Risk Rating** — Critical / High / Medium / Low with narrative summary
- **Domain Breakdown** — per-domain risk scores with visual progress bars
- **Detailed Findings Table** — every answer with framework control references
- **Recommended Risk Treatments** — prioritized gap list with severity ratings
- **Assessment History** — saved to localStorage, loadable and deletable
- **Export to JSON** — full assessment data export
- **Print / Save PDF** — print-optimized layout
- **Light / Dark Mode** — persisted via localStorage
- **Fully Responsive** — works on desktop and mobile

---

## Framework Coverage

| Framework | Controls Referenced |
|---|---|
| ISO 27001:2022 | A.5.1, A.5.12, A.5.15, A.5.19, A.5.20, A.5.26, A.5.27, A.5.29, A.5.30, A.5.34, A.5.36, A.6.3, A.6.5, A.8.2, A.8.5, A.8.8, A.8.10, A.8.13, A.8.14, A.8.15, A.8.24, A.8.30 |
| NIST CSF 2.0 | GV.OC-05, ID.AM-05, ID.RA-01, ID.RA-05, ID.SC-02, ID.SC-03, ID.SC-04, PR.AC-01, PR.AC-04, PR.AC-05, PR.AC-07, PR.AT-01, PR.DS-01, PR.DS-02, PR.DS-03, PR.DS-04, PR.DS-06, RS.AN-02, RS.RP-01, RC.RP-01 |
| SOC 2 Type II | CC1.3, CC1.4, CC6.1, CC6.2, CC6.3, CC6.5, CC6.7, CC7.1, CC7.3, CC7.4, CC9.2, A1.1, A1.2, A1.3 |
| GDPR | Art. 25, Art. 28, Art. 28(2), Art. 33 |
| PIPEDA | Principle 4, Breach Notification Regulations |

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

Additional: HTTPS enforcement, GitHub Pages redirect, Chart.js SRI, safety stub, XSS prevention, localStorage try/catch, prefers-reduced-motion, no tracking.

---

## Repository Structure

```
vendor-risk-assessment-tool/
├── index.html      ← Full application
├── _headers        ← Cloudflare security headers
└── README.md       ← This file
```

---

## Complete GRC Portfolio

| Project | Live URL |
|---|---|
| 🏠 ShomriTech GRC Platform | [chris-olowo-grc-portfolio.pages.dev](https://chris-olowo-grc-portfolio.pages.dev) |
| 1️⃣ **Vendor Risk Assessment Tool** *(this repo)* | [vendor-risk-assessment-tool.pages.dev](https://vendor-risk-assessment-tool.pages.dev) |
| 2️⃣ User Access Review Tracker | [user-access-review-tracker.pages.dev](https://user-access-review-tracker.pages.dev) |
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
