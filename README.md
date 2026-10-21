# SecureCheck

**An ISMS readiness assessment tool for German SMEs — scored against ISO/IEC 27001, NIS2 and BSI IT-Grundschutz.**

SecureCheck answers a question that is otherwise expensive for a small company to answer: *how far are we from being able to demonstrate an information security management system?*

It runs a 30-question structured assessment, scores the responses separately against three frameworks, and returns a readiness profile with per-question remediation guidance and an exportable report.

**[▶ Live demo](https://akhilraju24.github.io/securecheck/)**

> Dissertation project (COM7014), MSc Cybersecurity, Arden University — completed October 2026.

---

## Why this exists

German SMEs are increasingly in scope for obligations they are not resourced to assess:

- **NIS2** widened the set of in-scope entities well beyond traditional critical infrastructure, pulling in mid-size firms that have never run a formal security programme. Penalties reach €10 million or 2% of global turnover.
- **ISO/IEC 27001** certification is increasingly a contractual precondition from customers and partners.
- **BSI IT-Grundschutz** is the reference methodology in the German market, but its depth makes a first self-assessment hard to approach.

A consultancy-led gap assessment is the usual route and is out of reach for many SMEs. SecureCheck is a free first pass: enough structure to know where you stand and what to fix first.

---

## What it does

- **30 assessment questions** across the three frameworks, presented one at a time with progress tracking
- **Three-state responses** — implemented, partially implemented, or absent — rather than binary yes/no, so partial maturity is captured
- **Per-framework scoring**, so an organisation can see that it is strong on ISO 27001 governance but weak on NIS2 incident reporting
- **Weighted overall readiness score** with a three-tier verdict: Strong (≥75%), Developing (≥45%), At Risk (below)
- **Radar chart** comparing readiness across frameworks at a glance
- **Targeted remediation guidance** for every question answered "no" or "partial" — specific next actions, not generic advice
- **Exportable report** for sharing with management
- **Runs entirely in the browser.** No backend, no account, no data transmitted. For a tool asking a company to disclose its security weaknesses, this is a design requirement, not a convenience.

---

## Framework coverage

| Framework | Questions | Coverage |
|---|---|---|
| **ISO/IEC 27001** | 15 | Governance, risk management, people, asset management, access control, operations, incidents, supply chain, cryptography, physical security, compliance |
| **NIS2** | 10 | Risk management measures under Article 21(a)–(j), each question citing its specific sub-article |
| **BSI IT-Grundschutz** | 5 | Baseline analysis, Compendium module adoption, protection-requirement classification, IT-Sicherheitsbeauftragter, Sicherheitskonzept |

The overall score weights each framework by its question count (15 : 10 : 5).

---

## Scoring model

Each response carries a score: implemented = 2, partial = 1, absent = 0. Per-framework readiness is the percentage of available points achieved; the overall score is the weighted mean across frameworks.

```
framework score = (Σ response points / (questions × 2)) × 100
overall         = (ISO × 15 + NIS2 × 10 + BSI × 5) / 30
```

Thresholds at 75% and 45% separate the three readiness tiers. The rationale for the weighting and thresholds is in [`docs/methodology.md`](docs/methodology.md).

---

## Screenshots

<!-- TODO: open index.html, screenshot these three, save into assets/, then uncomment:
     1. the landing page
     2. a question mid-assessment
     3. the results screen with radar chart and remediation list -->

| Landing | Assessment | Results |
|---|---|---|
| _add screenshot_ | _add screenshot_ | _add screenshot_ |

---

## Running it

No build step, no dependencies to install. Either:

```bash
git clone https://github.com/Akhilraju24/securecheck.git
cd securecheck
open index.html          # macOS — or just double-click the file
```

or open the [live demo](https://akhilraju24.github.io/securecheck/).

**Built with:** vanilla HTML, CSS and JavaScript in a single file, with [Chart.js](https://www.chartjs.org/) for the radar and trend charts. Deliberately dependency-light so it runs from a file, a USB stick, or an internal network with no install.

---

## Project structure

```
securecheck/
├── index.html            # the complete application
├── docs/
│   ├── methodology.md    # assessment model, scoring, limitations
│   └── control-mapping.md# framework requirements behind each question
├── assets/               # screenshots
└── README.md
```

---

## Scope and limitations

SecureCheck is a **readiness assessment, not a certification audit**. It produces an indicative gap profile to inform planning. It does not substitute for a formal audit by an accredited body, and a strong result is not evidence of compliance.

Responses are self-reported and unverified. The question set covers the control areas most material to SMEs rather than every clause of each framework — in particular, the BSI IT-Grundschutz section is a high-level screen, not a full Compendium analysis.

---

## Author

**Akhil Raju** — MSc Cybersecurity, Arden University (Berlin)
[LinkedIn](https://www.linkedin.com/in/akhilraju24/)

## License

MIT — see [LICENSE](LICENSE).
