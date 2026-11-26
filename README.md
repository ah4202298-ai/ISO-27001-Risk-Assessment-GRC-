
# ISO/IEC 27001:2022 Information Security Risk Assessment & GRC Portfolio — CHMart

![CHMart Risk Register](assets/risk-register-preview.png)

> **Framework:** ISO/IEC 27001:2022 | **Organization:** CHMart (Fictional) | **Author:** Muhammad Ahmed

---

## 1. Project Goal
The goal of this project is to design and execute an end-to-end **ISO/IEC 27001:2022 Information Security Management System (ISMS) Risk Assessment and Governance, Risk, and Compliance (GRC)** implementation from scratch. It demonstrates practical capability in defining ISMS scope, classifying critical business assets, quantifying cybersecurity risk, mapping all 93 Annex A controls in a Statement of Applicability (SoA), and drafting audit-ready security policies.

---

## 2. Fictional Company Scenario
**CHMart** is a fast-growing **E-Commerce & Retail Technology** company employing **185 personnel** under a hybrid operating model (**65 corporate office staff** and **120 remote employees**).

* **Core Technology Stack:** Microsoft 365 & Entra ID (corporate productivity & SSO/MFA), AWS (cloud hosting, microservices, RDS databases, S3 storage), Shopify Plus (customer storefront), Stripe (PCI-compliant payment gateway), and GitHub Enterprise (source code & CI/CD).
* **Sensitive Data Processed:** Customer personally identifiable information (PII) and order histories, tokenized payment transaction records, employee HR/payroll records, and proprietary application source code.

---

## 3. What I Did (End-to-End GRC Implementation)

| Step | Deliverable | Summary of Work Completed |
| :--- | :--- | :--- |
| **1. Company Profile** | [`01-company-profile.md`](docs/01-company-profile.md) | Documented CHMart's workforce structure, hybrid infrastructure, core cloud platforms, and sensitive data flows. |
| **2. ISMS Scope & Context** | [`02-isms-scope.md`](docs/02-isms-scope.md) | Defined in-scope/out-of-scope boundaries (Clauses 4.1–4.3) and mapped expectations for customers, management, regulators, and Stripe. |
| **3. Asset Inventory** | [`03-asset-inventory.xlsx`](docs/03-asset-inventory.xlsx) / [`.csv`](docs/03-asset-inventory.csv) | Cataloged **14 core assets (`A01`–`A14`)** with designated owners, locations, data classifications, and business value ratings (Clause A.5.9). |
| **4. Risk Methodology** | [`04-risk-methodology.md`](docs/04-risk-methodology.md) | Established a 5×5 qualitative/semi-quantitative scoring matrix ($\text{Score} = \text{Likelihood} \times \text{Impact}$) and formal risk acceptance rules. |
| **5. Risk Register** | [`05-risk-register.xlsx`](docs/05-risk-register.xlsx) | Identified **18 threat-vulnerability scenarios (`R01`–`R18`)** across all 14 assets using dynamic Excel formulas and conditional formatting. |
| **6. Risk Treatment Plan** | [`05-risk-register.xlsx`](docs/05-risk-register.xlsx) *(Tab 2)* | Selected treatment options (`Reduce` vs. `Accept`), assigned controls, owners, and deadlines, and calculated residual risk scores. |
| **7. Statement of Applicability** | [`06-statement-of-applicability.xlsx`](docs/06-statement-of-applicability.xlsx) | Evaluated all **93 ISO/IEC 27001:2022 Annex A controls** across Organizational, People, Physical, and Technological themes with risk mappings. |
| **8. Security Policies** | [`07-access-control-policy.md`](docs/07-access-control-policy.md), [`08-incident-response-policy.md`](docs/08-incident-response-policy.md), [`09-acceptable-use-policy.md`](docs/09-acceptable-use-policy.md) | Authored three standardized governance policies covering purpose, scope, enforceable mandates, roles, and Annex A mappings. |

---

## 4. Key Findings & Risk Posture Summary
* **Inherent Risk Distribution (18 Total Risks):**
  * **6 High Risks (33.3%):** Phishing/legacy mail authentication (`R01`), AWS S3/IAM misconfiguration (`R03`), hardcoded GitHub API secrets (`R07`), unencrypted customer PII database access (`R08`), CI/CD supply chain compromise (`R12`), and remote endpoint ransomware (`R15`).
  * **10 Medium Risks (55.6%):** Permissive SharePoint sharing (`R02`), single-region DDoS/outage (`R04`), Shopify app token compromise (`R05`), Stripe webhook spoofing (`R06`), SQL injection/API scraping (`R09`), mutable transaction logs (`R10`), unreviewed HR folder permissions (`R11`), Entra ID break-glass gaps (`R13`), remote laptop theft (`R14`), and office guest Wi-Fi segmentation (`R17`).
  * **2 Low Risks (11.1%):** Office workstation screen lock (`R16`) and public catalog plugin maintenance (`R18`) — formally **Accepted** under CHMart's risk appetite criteria.
* **Post-Treatment Residual Risk:** Implementing targeted controls (FIDO2 MFA, S3 Block Public Access, GitHub Secret Scanning, AES-256 encryption, MDM/BitLocker, and quarterly access reviews) reduces **100% of High and Medium risks to Low residual scores (3–4)**.
* **Annex A Control Coverage:** **88 of 93 controls** are applicable (**39 Implemented**, **46 Planned**, **3 Not Started**); **5 controls** (`A.7.5`, `A.7.6`, `A.7.11`, `A.7.12`, `A.8.30`) are excluded with documented cloud/in-house justifications.

---

## 5. Skills Demonstrated
* **GRC & Compliance Frameworks:** ISO/IEC 27001:2022 Clauses 4–8 & all 93 Annex A Controls, PCI DSS alignment, Shared Responsibility Model.
* **Risk Management:** Asset valuation, threat/vulnerability modeling, 5×5 risk matrix design, risk treatment planning, and residual risk calculation.
* **Cloud & Identity Security Governance:** AWS IAM/S3 hardening, Microsoft Entra ID Conditional Access & FIDO2 MFA, RBAC, secrets management, and endpoint MDM/EDR governance.
* **Security Policy & Audit Documentation:** Executive policy authoring, control mapping, and structured GRC reporting.

---

## 6. Disclaimer
> **Disclaimer:** *CHMart* is a completely fictional organization created solely for educational and cybersecurity portfolio demonstration purposes. All system architectures, employee counts, risk scenarios, and audit artifacts are simulated and do not represent any real company.
