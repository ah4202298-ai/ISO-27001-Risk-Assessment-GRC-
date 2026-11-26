# Access Control Policy: CHMart

> **Document ID:** GRC-08 | **Framework:** ISO/IEC 27001:2022 | **Owner:** Information Security Lead | **Status:** Approved Baseline

## 1. Purpose
This policy establishes strict identity, authentication, and authorization rules to prevent unauthorized access to **CHMart**'s cloud infrastructure, corporate applications, source code, and Restricted/Confidential data assets.

---

## 2. Scope
This policy applies to all 185 **CHMart** employees (65 corporate office staff and 120 remote staff), contractors, and service accounts accessing in-scope systems: **Microsoft 365**, **Microsoft Entra ID**, **AWS**, **Shopify Plus**, **Stripe**, **GitHub Enterprise**, and internal customer/HR databases.

---

## 3. Policy Statements

| Control Area | Mandatory Policy Requirement |
| :--- | :--- |
| **Least Privilege & RBAC** | All user and service accounts shall be provisioned strictly according to Role-Based Access Control (RBAC) and the Principle of Least Privilege. Default access is denied unless explicitly authorized. |
| **Multi-Factor Authentication (MFA)** | Phishing-resistant MFA (FIDO2/WebAuthn or authenticator app with number matching) is mandatory for all employees and contractors across Microsoft Entra ID, AWS, Shopify, Stripe, and GitHub. Legacy authentication protocols (IMAP, POP3, basic auth) must be disabled. |
| **Privileged Access Management** | Administrative privileges (AWS IAM Admin, Entra ID Global Admin, Shopify Store Owner) shall be restricted to dedicated, audited accounts. Local administrator rights are removed from standard employee endpoints. Break-glass emergency accounts must be stored offline and monitored via real-time alerts. |
| **Joiner / Mover / Leaver Lifecycle** | Access is granted only upon HR approval. Role transfers trigger immediate privilege adjustment. Upon termination, all identity tokens, VPN certificates, and SaaS sessions must be revoked within **1 hour**. |
| **Periodic Access Reviews** | Asset owners must conduct **quarterly access reviews** for all Restricted data repositories (AWS RDS customer PII, HR SharePoint sites, Stripe, and production GitHub repositories) and revoke stale permissions within 5 business days. |
| **API Keys & Secrets** | Hardcoding credentials, tokens, or API keys in source code is strictly prohibited. All secrets must be stored in AWS Secrets Manager or GitHub Encrypted Secrets and rotated every 90 days. |

---

## 4. Roles and Responsibilities

| Role | Responsibilities |
| :--- | :--- |
| **Information Security Lead** | Maintains this policy, defines Entra ID Conditional Access baselines, and oversees quarterly access review compliance. |
| **IT Operations & Support Leads** | Provisions/deprovisions user accounts, enforces MFA enrollment, and manages endpoint privilege restrictions. |
| **Asset Owners (DevOps, Engineering, HR, Finance)** | Approves role-based access requests for their respective platforms and executes quarterly access recertifications. |
| **All Employees & Contractors** | Safeguards credentials, never shares accounts or MFA tokens, and reports suspected account compromise immediately. |

---

## 5. Enforcement
Violations of this policy—including sharing login credentials, bypassing MFA, or storing unencrypted API keys in public or private repositories—will result in immediate access suspension and disciplinary action up to termination of employment or contract, in accordance with CHMart's HR disciplinary procedures.

---

## 6. Review Date & Annex A Alignment
* **Effective Date:** November 26, 2026
* **Next Scheduled Review:** November 26, 2027 (Annual, or upon major architectural/regulatory change)
* **Referenced ISO/IEC 27001:2022 Annex A Controls:**
  * **A.5.3** — Segregation of duties
  * **A.5.15** — Access control
  * **A.5.16** — Identity management
  * **A.5.17** — Authentication information
  * **A.5.18** — Access rights
  * **A.6.5** — Responsibilities after termination or change of employment
  * **A.8.2** — Privileged access rights
  * **A.8.3** — Information access restriction
  * **A.8.4** — Access to source code
  * **A.8.5** — Secure authentication
