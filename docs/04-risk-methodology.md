# Risk Assessment Methodology: CHMart

> **Document ID:** GRC-04 | **Framework:** ISO/IEC 27001 (Clause 6.1.2 & Clause 8.2) | **Status:** Baseline Methodology

## 1. Purpose
This document establishes a consistent, repeatable qualitative and semi-quantitative methodology for identifying, analyzing, evaluating, and treating information security risks across **CHMart**'s in-scope systems, personnel, and data assets.

---

## 2. Likelihood Scale (1 to 5)
Likelihood measures the probability that a threat source will successfully exploit a vulnerability within a 12-month period.

| Score | Rating | Definition & Frequency Criteria |
| :---: | :--- | :--- |
| **1** | **Rare** | Highly unlikely to occur; expected less than once every 5 years (< 5% probability). |
| **2** | **Unlikely** | Could occur under specific circumstances; expected once every 2 to 5 years (5%–20% probability). |
| **3** | **Possible** | Might occur occasionally; expected once every 1 to 2 years (21%–50% probability). |
| **4** | **Likely** | Will probably occur in most circumstances; expected multiple times per year (51%–85% probability). |
| **5** | **Almost Certain** | Expected to occur frequently or imminently without additional controls (> 85% probability). |

---

## 3. Impact Scale (1 to 5)
Impact measures the potential operational, financial, legal, and reputational consequences to **CHMart** if a security incident compromises the Confidentiality, Integrity, or Availability (CIA) of an asset.

| Score | Rating | Definition & Business Consequence |
| :---: | :--- | :--- |
| **1** | **Minor** | Negligible operational disruption; isolated to non-critical systems; no regulatory, financial, or customer data impact. |
| **2** | **Moderate** | Limited disruption to internal workflows (< 4 hours); minor recovery cost; no external PII or payment data exposure. |
| **3** | **Significant** | Noticeable service degradation (4–24 hours); moderate financial loss or contractual SLA breach; limited internal data exposure. |
| **4** | **Major** | Extended outage of core e-commerce or cloud operations (> 24 hours); unauthorized exposure of customer PII; formal regulatory inquiry. |
| **5** | **Severe** | Critical business shutdown; large-scale breach of customer PII or payment data; heavy regulatory fines, PCI DSS non-compliance, or severe reputational damage. |

---

## 4. Risk Scoring Formula & Matrix
Every identified risk is evaluated using the formula:

$$\text{Risk Score} = \text{Likelihood} \times \text{Impact}$$

| Likelihood \ Impact | 1 (Minor) | 2 (Moderate) | 3 (Significant) | 4 (Major) | 5 (Severe) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **5 (Almost Certain)** | 5 (Low) | 10 (Medium) | 15 (High) | 20 (High) | 25 (High) |
| **4 (Likely)** | 4 (Low) | 8 (Medium) | 12 (Medium) | 16 (High) | 20 (High) |
| **3 (Possible)** | 3 (Low) | 6 (Low) | 9 (Medium) | 12 (Medium) | 15 (High) |
| **2 (Unlikely)** | 2 (Low) | 4 (Low) | 6 (Low) | 8 (Medium) | 10 (Medium) |
| **1 (Rare)** | 1 (Low) | 2 (Low) | 3 (Low) | 4 (Low) | 5 (Low) |

---

## 5. Risk Levels & Acceptance Criteria

| Score Range | Risk Level | Risk Acceptance & Treatment Rule |
| :---: | :---: | :--- |
| **1 – 6** | **Low** | **Accepted:** Risk falls within CHMart's risk appetite. No immediate treatment required; monitor during annual ISMS reviews. |
| **7 – 14** | **Medium** | **Treatment Required:** Risk is above acceptable thresholds. Must be reduced via security controls (mitigate), transferred, or avoided within 90 days. |
| **15 – 25** | **High** | **Mandatory Immediate Treatment:** Unacceptable risk to business continuity or customer/payment data. Requires executive escalation and a prioritized remediation plan within 30 days. |

---

> **Assumptions:** This risk assessment methodology is tailored for the fictional organization CHMart as part of an ISO/IEC 27001 GRC portfolio project.
