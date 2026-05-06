# Financial Reporting & Consolidation

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An open-source, AI-native platform for multi-entity financial consolidation, IFRS/GAAP reporting, and intercompany elimination.

Financial Reporting & Consolidation is a candidate open-source project targeting the group close, multi-currency consolidation, and statutory reporting workflows currently dominated by expensive, closed-source enterprise platforms. It is aimed at mid-market controllers, IPO-bound CFOs, and private equity portfolio finance teams who need IFRS 10 / ASC 810 compliance without a 9–18 month enterprise EPM rollout.

---

## Why Financial Reporting & Consolidation?

- The financial consolidation market is entirely proprietary: no open-source platform exists at any level of maturity, leaving controllers to choose between spreadsheets and six-figure enterprise contracts.
- Tier-1 incumbents such as OneStream and CCH Tagetik typically start at $150K+/yr and require 9–18 month implementations, effectively excluding companies with 10–100 entities.
- Mid-market tools such as Prophix and Vena trade depth for accessibility, lacking the multi-GAAP statutory rigor that IFRS 10 and ASC 810 demand for complex group structures.
- Workiva dominates external reporting and XBRL but is not a full consolidation platform — intercompany elimination and ownership management remain limited.
- Private equity portfolio controllers managing 10–50 portfolio companies across different GAAP frameworks need rapid entity spin-up and tear-down that current tools handle poorly.

---

## Key Features

### Consolidation Engine

- Multi-entity consolidation with configurable entity hierarchy and alternate hierarchies for management vs. statutory reporting
- Multi-currency translation supporting current rate, historical rate, and average rate methods by account type, with automated CTA (Cumulative Translation Adjustment) posting
- Intercompany matching and elimination with dispute resolution workflow and elimination journal posting at the first common parent
- Minority interest and non-controlling interest calculation per IFRS 10 and ASC 810
- Parallel GAAP support: simultaneous IFRS and US GAAP consolidation from a single source of actuals

### Close Management & Audit

- Close management with task assignment, entity-level status tracking, owner assignment, and deadline escalation
- Account reconciliation integrated with the close task workflow
- Full audit trail: every data change, journal entry, and approval logged with user, timestamp, and rationale
- Data quality validation rules on imported actuals to catch errors before they propagate to consolidated statements

### Reporting Outputs

- Consolidated financial statements: P&L, balance sheet, cash flow (direct and indirect method), statement of changes in equity
- Management reporting pack generation with configurable templates
- Narrative reporting with data-linked cells that update automatically when actuals change
- XBRL/iXBRL tagging and SEC submission formatting for public company filers (backlog)
- ESG/CSRD data consolidation aligned to ESRS taxonomy (backlog)

### Integration & Extensibility

- REST API for custom data integration pipelines
- Pre-built ERP connectors for NetSuite, QuickBooks, and SAP at minimum
- Ownership management for complex structures including step acquisitions, equity method investments, and mid-period ownership changes

---

## AI-Native Advantage

AI-native architecture targets the workflows that consume the most controller time today. Automated intercompany elimination uses ML to match IC invoices and payments across entities, propose elimination journal entries with explainable reasoning, and post them on controller approval — replacing manual mapping tables. Continuous close anomaly detection flags mismatches, missing accruals, and out-of-pattern variances in real time throughout the month rather than at period end. Natural-language report generation drafts IFRS-compliant MD&A and variance commentary from structured financial data, and a multi-GAAP bridge assistant proposes and tracks IFRS-to-GAAP adjustment entries with per-difference rationale — a workflow no existing tool handles natively.

---

## Tech Stack & Deployment

The project is designed to align with public accounting standards (IFRS 10, ASC 810, IAS 21) and the open XBRL / iXBRL standards governed by XBRL International under royalty-free licence. Expected deployment is an open-source core suitable for self-hosting, paired with a hosted SaaS tier targeting mid-market and PE-backed companies that cannot justify tier-1 EPM contracts. Integration is via REST API and pre-built ERP connectors (NetSuite, QuickBooks, SAP minimum), with additional connectors for Oracle, Workday, Dynamics, and DATEV/Sage common in European environments.

---

## Market Context

The financial close software market was approximately USD $4.5B in 2026, projected to reach USD $18.5B by 2034 at an 8.1% CAGR (GlobeNewswire, 2026); the financial consolidation segment alone was USD $3.56B in 2026, projected to USD $7.77B by 2035 at 9% CAGR (Business Research Insights). Incumbent pricing ranges from ~$25K/yr (Vena) and ~$30K/yr (Prophix, Workiva) at the mid-market entry point to $300K–$500K+/yr for OneStream enterprise deployments. Primary buyers are group controllers and CFOs at 1,000+ employee enterprises, finance directors at mid-market companies with 50–500 entities, IPO-bound CFOs needing SEC-grade XBRL filing, and private equity portfolio controllers.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
