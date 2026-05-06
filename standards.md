# Standards & API Reference

> Project: Financial Reporting & Consolidation · Generated: 2026-05-06

## Industry Standards & Specifications

### Accounting & Consolidation Standards

**IFRS 10 — Consolidated Financial Statements**
- Official URL: https://www.ifrs.org/issued-standards/list-of-standards/ifrs-10-consolidated-financial-statements/
- Defines the single control-based model for determining which entities must be consolidated into group financial statements. Governs the elimination of intragroup balances, intercompany transactions, and non-controlling interest calculations. Any software implementing group consolidation must comply with IFRS 10 logic for control assessment, ownership management, and elimination hierarchies.

**IAS 21 — The Effects of Changes in Foreign Exchange Rates**
- Official URL: https://www.ifrs.org/issued-standards/list-of-standards/ias-21-the-effects-of-changes-in-foreign-exchange-rates/
- Prescribes how to include foreign currency transactions and foreign operations in the financial statements of an entity and how to translate financial statements into a presentation currency. Governs current rate, historical rate, and average rate translation methods, as well as the treatment of Cumulative Translation Adjustments (CTA). Amended in November 2025 to address translation from non-hyperinflationary to hyperinflationary presentation currencies.

**IAS 27 — Separate Financial Statements**
- Official URL: https://www.ifrs.org/issued-standards/list-of-standards/ias-27-separate-financial-statements/
- Governs the accounting and disclosure requirements for investments in subsidiaries, joint ventures, and associates when an entity prepares separate (statutory) financial statements alongside consolidated statements. Relevant for platforms supporting parallel statutory and group reporting.

**IFRS 3 — Business Combinations**
- Official URL: https://www.ifrs.org/issued-standards/list-of-standards/ifrs-3-business-combinations/
- Defines the acquisition method for recording business combinations, goodwill recognition, and fair value allocation of acquired assets and liabilities. Relevant for consolidation software that must handle first-time consolidation, step acquisitions, and mid-period ownership changes.

**IFRS 18 — Presentation and Disclosure in Financial Statements** (effective 2027, early application permitted)
- Official URL: https://www.ifrs.org/issued-standards/list-of-standards/ifrs-18-presentation-and-disclosure-in-financial-statements/
- Replaces IAS 1; introduces new income statement categories and restructures the statement of profit or loss. The 2025 IFRS Accounting Taxonomy already incorporates IFRS 18 elements. Consolidation platforms must plan for IFRS 18-compliant financial statement templates by 2027.

**US GAAP ASC 810 — Consolidation**
- Official URL: https://dart.deloitte.com/USDART/home/publications/roadmap/consolidation
- FASB standard for US entities. Applies a two-model approach: the Voting Interest Entity (VIE) model and the Variable Interest Entity model. Differs from IFRS 10's single control model. FASB issued ASU 2025-03 in 2025 to address accounting acquirer determinations in VIE transactions. Platforms supporting dual-GAAP consolidation must implement both models in parallel.

**US GAAP ASC 830 — Foreign Currency Matters**
- Official URL: https://fasb.org/ (Accounting Standards Codification, Topic 830)
- US GAAP equivalent of IAS 21. Governs functional currency determination, remeasurement, and translation for US GAAP reporting entities. Relevant for multi-GAAP platforms supporting simultaneous IFRS and US GAAP consolidation.

---

### Digital Reporting & Tagging Standards

**XBRL (eXtensible Business Reporting Language)**
- Official URL: https://www.xbrl.org/
- Open, royalty-free standard governed by XBRL International for machine-readable business reporting. Forms the foundation of SEC EDGAR mandatory filings for US public companies and ESEF filings for EU-listed companies. The XBRL International License Agreement permits royalty-free implementation.

**Inline XBRL (iXBRL)**
- Official URL: https://www.xbrl.org/guidance/ixml-for-inline-xbrl/
- Embeds XBRL tags within human-readable XHTML documents, enabling a single file to be both human-readable and machine-processable. Required by the SEC for all US public company filers (mandatory from 2020 onwards) and by ESMA for ESEF filings by EU-listed issuers.

**IFRS Accounting Taxonomy 2025**
- Official URL: https://www.ifrs.org/issued-standards/ifrs-taxonomy/ and https://xbrl.ifrs.org/taxonomy/2025-03-27/
- Published March 2025; incorporates disclosure requirements for IFRS 18 and IFRS 19 (not yet effective). The reference taxonomy for iXBRL tagging of IFRS-based consolidated financial statements worldwide, including ESEF (EU) and SEC IFRS filers (non-US companies filing with the SEC). Mandatory to reference in any IFRS-based XBRL implementation.

**SEC EDGAR XBRL Taxonomies (US GAAP 2026 / IFRS 2025)**
- Official URL: https://www.sec.gov/newsroom/whats-new/2603-2026-xbrl-taxonomies-update and https://xbrl.sec.gov/
- The SEC adopts annual XBRL taxonomy updates (2026 taxonomy effective for filings from January 2026). The US GAAP Financial Reporting Taxonomy and SEC Reporting Taxonomy are the authoritative tagging reference for US public company filers. EDGAR XBRL Guide (April 2026): https://www.sec.gov/files/edgar/filer-information/specifications/xbrl-guide.pdf

**ESEF — European Single Electronic Format**
- Official URL: https://www.esma.europa.eu/issuer-disclosure/electronic-reporting
- ESMA regulatory technical standard (ESEF RTS) mandating that all companies listed on EU regulated markets file Annual Financial Reports in iXBRL-tagged XHTML format. Mandatory from 2020 (primary statements) and 2022 (block tagging of notes). The ESEF taxonomy extends the IFRS Accounting Taxonomy. A platform targeting EU-listed companies must produce ESEF-compliant iXBRL output.

---

### Sustainability & ESG Reporting Standards

**ESRS (European Sustainability Reporting Standards) + CSRD**
- Official URL: https://finance.ec.europa.eu/capital-markets-union-and-financial-markets/company-reporting-and-auditing/company-reporting/corporate-sustainability-reporting_en and https://www.efrag.org/en/sustainability-reporting/esrs-workstreams/digital-reporting-with-xbrl
- The CSRD determines who must report sustainability data; ESRS specifies what must be reported. Applies from 2024 (large listed companies >500 employees) and 2025 (all other large companies); Wave 2 scope (companies >1,000 FTE and €450M turnover) delayed to 2027 under the 2025 Omnibus simplification package. The ESRS XBRL taxonomy was published in the EU Official Journal (December 2023) and will integrate with the ESEF taxonomy for the 2025 reporting year. A consolidation platform must support ESG data collection at entity level and roll up to group-level disclosures alongside financial consolidation.

---

### Financial Messaging & Data Exchange Standards

**ISO 20022 — Financial Services Messaging Standard**
- Official URL: https://www.iso20022.org/ and https://www.swift.com/standards/iso-20022
- Global standard for electronic data interchange between financial institutions; supports XML and JSON syntaxes. Covers payment initiation (pain), clearing and settlement (pacs), and cash management (camt) message categories. Relevant for intercompany payment reconciliation within a consolidation platform, particularly for matching intercompany cash flows across entities that settle via SWIFT or local payment rails.

**FDX API v6.4 — Financial Data Exchange**
- Official URL: https://financialdataexchange.org/
- Open, royalty-free, non-profit standard for consumer and business financial data sharing; recognized by the CFPB as the US open banking standard (January 2025). Version 6.4 (Spring 2025) includes 24 new RFCs and extended coverage of investment, tax, and insurance data. Relevant for sourcing actuals data from banks and financial institutions into a consolidation platform.

---

### Security & Compliance Standards

**OAuth 2.0 (RFC 6749) and OpenID Connect**
- Official URL: https://oauth.net/2/ and https://openid.net/connect/
- OAuth 2.0 is the de-facto standard for API authorization in financial SaaS platforms. OpenID Connect (OIDC) adds the authentication layer. All major consolidation platforms (OneStream, Oracle FCCS, CCH Tagetik) use OAuth 2.0 / OIDC for API access and external identity provider federation (Microsoft Entra ID / Azure AD, Okta, PingFederate). A new platform must implement OAuth 2.0 with PKCE for API clients and OIDC for SSO federation.

**SAML 2.0**
- Official URL: https://www.oasis-open.org/standard/saml/
- Widely used in enterprise finance for single sign-on (SSO) federation with corporate identity providers. Many enterprise buyers require SAML 2.0 SSO as a procurement requirement for financial applications subject to SOX access controls.

**SOX (Sarbanes-Oxley Act, 2002) — Sections 302 and 404**
- Not an API standard but a US legal compliance requirement for public companies. Section 404 mandates documented internal controls over financial reporting (ICFR), including immutable audit trails, access controls, and segregation of duties. Any platform targeting US public companies must implement SOX-aligned controls: immutable change logs, role-based access with approval workflows, and evidence retention.

**GDPR (EU) 2016/679 and EU Data Act (effective September 2025)**
- Official URL: https://gdpr.eu/ and https://digital-strategy.ec.europa.eu/en/policies/data-act
- GDPR requires EU personal data to remain within approved jurisdictions; financial consolidation platforms processing employee or customer data from EU subsidiaries must comply. The EU Data Act (September 2025) additionally mandates data portability in machine-readable formats and prohibits switching charges after January 2027, directly affecting vendor lock-in practices in consolidation SaaS.

**BCBS 239 — Principles for Effective Risk Data Aggregation and Reporting**
- Official URL: https://www.bis.org/bcbs/publ/d559.htm
- Basel Committee standard governing risk data aggregation for Global Systemically Important Banks (G-SIBs). Requires accurate, timely, consolidated financial data with full audit lineage from source to report. Relevant for consolidation platforms targeting banking-sector clients; data lineage from source ERP to consolidated output is a BCBS 239 requirement.

---

## Similar Products — Developer Documentation & APIs

### OneStream

- **Description:** Unified EPM platform delivering financial close, consolidation, planning, and reporting on a single data model without module separation. Gartner Magic Quadrant Leader (4× consecutive).
- **API Documentation:** https://documentation.onestream.com/docs/Content/REST%20API/REST%20API%20Overview.html
- **REST API Guide (PDF):** https://documentation.onestream.com/docs/Content/PDFs/REST_API_Implementation_Guide.pdf
- **API Overview Guide:** https://documentation.onestream.com/docs/Content/PDFs/API_Overview_Guide.pdf
- **Authentication:** OAuth 2.0 / OIDC (Microsoft Entra ID, Okta, PingFederate) for hosted environments; Personal Access Tokens (PATs) for OneStream-hosted environments using native or SAML 2.0 authentication
- **Standards:** REST/JSON; no public OpenAPI specification confirmed

### Oracle Fusion Cloud EPM — Financial Consolidation and Close (FCCS)

- **Description:** Oracle's cloud EPM suite module for multi-entity, multi-GAAP, multi-currency consolidation. Deeply integrated with Oracle ERP Cloud and Oracle EBS.
- **API Documentation:** https://docs.oracle.com/en/cloud/saas/enterprise-performance-management-common/prest/toc.htm
- **Integration Guide:** https://docs.oracle.com/en/cloud/saas/enterprise-performance-management-common/intgr/fccs_get_started_topicmap.html
- **Full REST API Reference (PDF):** https://docs.oracle.com/en/cloud/saas/enterprise-performance-management-common/prest/GUID-185E11F9-8420-414A-B2EA-9098767FC24F.pdf
- **What's New (May 2025):** https://docs.oracle.com/en/cloud/saas/readiness/epm/2025/epm-may25/25may-epm-wn-f38449.htm
- **Authentication:** OAuth 2.0 and basic authentication
- **Standards:** REST/JSON; EPM Automate CLI for scripted operations

### CCH Tagetik (Wolters Kluwer)

- **Description:** End-to-end financial close and consolidation platform with deep multi-GAAP, multi-currency, and statutory reporting capabilities. Particularly strong for European statutory reporting across 50+ country packs.
- **Integration Overview:** https://www.wolterskluwer.com/en/solutions/cch-tagetik/technology-integrations
- **Developer/Training Resources:** https://www.academy.registration.tagetik.com/ (Tagetik Academy — "Data Integration with RESTful API" course)
- **Power Query Connector (Microsoft):** https://learn.microsoft.com/en-us/power-query/connectors/wolters-kluwer-cch-tagetik
- **Authentication:** OAuth 2.0 client credentials (preferred) and basic authentication
- **Standards:** OData (Open Data Protocol) for data exposure; REST API for data consumption (available from Service Pack 23); SCIM for user provisioning; Swagger/OData documentation available via Tagetik Academy

### SAP Financial Consolidation / Group Reporting (S/4HANA)

- **Description:** S/4HANA-embedded consolidation module with parallel GAAP/IFRS ledgers and real-time journal entries. Available as part of SAP S/4HANA or standalone.
- **API Hub:** https://api.sap.com/package/S4HANAOPAPI/odata (SAP Business Accelerator Hub — OData V2 APIs)
- **OData V4 APIs:** https://api.sap.com/products/SAPS4HANACloud/apis/ODATAV4
- **Developer Guide:** https://www.apideck.com/blog/guide-to-sap-4-hana-rest-and-soap-api
- **Authentication:** OAuth 2.0 via SAP BTP Identity Authentication Service; SAML 2.0 for SSO
- **Standards:** OData V2 and OData V4 (REST-compliant); SOAP for legacy integration

### Workiva

- **Description:** Cloud reporting platform focused on SEC/regulatory filing, XBRL/iXBRL tagging, narrative reporting, SOX programme management, and ESG/CSRD reporting. Dominant for US public company external filings.
- **Developer Portal:** https://developers.workiva.com/
- **API Reference (2026-01-01 version):** https://developers.workiva.com/2026-01-01/overview.html
- **Authentication Guide:** https://developers.workiva.com/workiva-admin/reference/admin-authentication
- **Authentication:** OAuth 2.0 — exchange clientID/clientSecret for a bearer token (10-minute expiry); token endpoint via POST to OAuth2/token
- **Standards:** REST/JSON; OpenAPI specification provided (no public SDK — generate from OpenAPI spec); supports Documents, Spreadsheets, Presentations, Graph, and Tasks via API

### LucaNet

- **Description:** Group consolidation and financial planning platform for mid-market and larger firms; strong IFRS and European local GAAP compliance (German HGB, Swiss, Austrian).
- **Documentation Portal:** https://support.lucanet.com/en/documentation.html
- **Integration Overview:** https://www.lucanet.com/en/platform/technology/data-integration/
- **Connectors Library:** https://www.lucanet.com/en/platform/integrations/ (250+ out-of-the-box connectors)
- **Authentication:** Not publicly detailed; enterprise SSO and REST API credentials likely available to licensed customers
- **Standards:** REST API with third-party connector support (including SharePoint REST API integration documented by partners)

### Prophix

- **Description:** Mid-market EPM covering financial consolidation, budgeting, and reporting. Targets companies with 5–100 entities; faster implementation (6–12 weeks) than tier-1 tools.
- **API Documentation:** https://apitracker.io/a/prophix (third-party tracker; official docs require customer login)
- **Integrations Overview:** https://www.prophix.com/integrations/ (400+ connected systems)
- **Standards:** REST API; supports NetSuite, Dynamics, SAP, Oracle, QuickBooks connectors
- **Authentication:** Not publicly detailed; OAuth 2.0 assumed for SaaS integrations

### HighRadius Financial Close Management

- **Description:** AI-powered financial close and account reconciliation platform. Gartner Magic Quadrant Challenger (2025). Focuses on reconciliation automation, journal entry management, and close task management rather than full consolidation.
- **Product Page:** https://www.highradius.com/product/financial-close-software/
- **ERP Integration Overview:** https://www.highradius.com/product/financial-close-software/erp/
- **Standards:** API and SFTP-based integrations; pre-built connectors to SAP, Oracle, NetSuite, Dynamics, Sage Intacct, Workday; 100+ financial data source connectors
- **Authentication:** Not publicly detailed; enterprise SSO and API key authentication assumed

---

## Notes

**Emerging and evolving areas:**

- **IFRS 18 (effective 2027):** All financial statement presentation templates in consolidation software will need to be updated to reflect IFRS 18's restructured income statement categories. The 2025 IFRS Accounting Taxonomy already includes IFRS 18 elements in anticipation.

- **ESRS XBRL digital reporting (2026+):** The ESRS XBRL taxonomy integration into the ESEF taxonomy is expected to be mandatory for 2025 reporting year (filed in 2026). This creates a significant build requirement for platforms that currently handle only financial XBRL tagging and not ESG/sustainability data tagging.

- **EU Data Act (September 2025):** Mandates data portability and prohibits switching charges (from January 2027). Consolidation SaaS platforms must offer machine-readable data export and support smooth customer offboarding to comply — this is also a competitive differentiator for open-source platforms.

- **No open API standard for consolidation data models:** Unlike banking (ISO 20022, FDX) or open banking domains, there is no standardised API schema or data model for group consolidation data (entity hierarchies, intercompany transactions, elimination journals). An open-source project has the opportunity to define and publish such a schema — potentially as an OpenAPI specification covering the core consolidation data objects — which would be valuable to the broader finance community.

- **Model Context Protocol (MCP):** No MCP server specifications exist for financial consolidation tools as of May 2026. An AI-native open-source platform exposing consolidation data and actions via MCP would enable AI agents (including Claude) to query consolidated financials, propose elimination entries, and generate narrative commentary — a significant differentiator over existing proprietary platforms.
