# Incident Response Policy: CHMart

> **Document ID:** GRC-09 | **Framework:** ISO/IEC 27001:2022 | **Owner:** Information Security Lead | **Status:** Approved Baseline

## 1. Purpose
This policy establishes a structured framework for detecting, reporting, triaging, containing, eradicating, and recovering from information security incidents to minimize operational disruption, protect customer and payment data, and meet statutory breach-notification deadlines.

---

## 2. Scope
This policy covers all security events and incidents affecting **CHMart**'s corporate office, 120 remote endpoints, cloud infrastructure (**AWS**, **Microsoft 365**, **Shopify Plus**, **Stripe**, **GitHub Enterprise**), and any Restricted or Confidential information assets.

---

## 3. Policy Statements

| Phase / Requirement | Mandatory Policy Requirement |
| :--- | :--- |
| **Mandatory Event Reporting** | All employees and contractors must report suspected phishing emails, lost/stolen laptops, unauthorized access, or anomalous system behavior to the Security Operations channel within **30 minutes** of discovery. |
| **Incident Classification & SLAs** | Incidents are triaged by severity:<br>• **P1 (Critical — Active PII/payment breach or storefront outage):** Acknowledge within **15 minutes**; executive escalation within **1 hour**.<br>• **P2 (High — Compromised employee account or malware infection):** Acknowledge within **1 hour**.<br>• **P3 (Medium/Low — Blocked phishing or policy violation):** Acknowledge within **4 business hours**. |
| **Containment, Eradication & Recovery** | Authorized responders must isolate compromised endpoints via EDR/MDM, revoke compromised Entra ID/AWS tokens, eradicate root causes, and restore services from verified encrypted backups. |
| **Forensic Evidence Preservation** | Immutable logs (AWS CloudTrail, S3 Object Lock WORM storage, Entra ID sign-in logs, and endpoint telemetry) must be preserved with documented chain-of-custody prior to system rebuilds. |
| **External & Regulatory Notification** | Legal counsel and Executive Management must evaluate regulatory data-protection obligations and PCI DSS notification rules (via Stripe) within **24 hours** of confirming a personal data or payment incident. |
| **Post-Incident Review** | A formal root-cause analysis (Lessons Learned) report must be completed within **5 business days** of resolving any P1 or P2 incident, updating the Risk Register (`GRC-05`) and controls accordingly. |

---

## 4. Roles and Responsibilities

| Role | Responsibilities |
| :--- | :--- |
| **Incident Commander (Information Security Lead)** | Leads incident triage, coordinates containment and eradication, maintains evidence chain-of-custody, and authors post-incident reviews. |
| **Technical Responders (DevOps, IT Support, Network Admin)** | Executes technical containment (account lockouts, firewall/WAF blocks, remote laptop wipe, backup restoration). |
| **Executive Management & Legal/DPO** | Approves external customer disclosures, regulatory breach notifications, and business continuity decisions. |
| **All Staff** | Reports suspicious activity immediately and cooperates with incident investigations without altering affected devices. |

---

## 5. Enforcement
Failure to report a known or suspected security incident, intentional concealment of a security breach, or unauthorized tampering with forensic logs is a serious violation of this policy and will result in formal disciplinary action up to termination or legal referral.

---

## 6. Review Date & Annex A Alignment
* **Effective Date:** November 26, 2026
* **Next Scheduled Review:** November 26, 2027 (Annual, or following any P1 security incident)
* **Referenced ISO/IEC 27001:2022 Annex A Controls:**
  * **A.5.5** — Contact with authorities
  * **A.5.24** — Information security incident management planning and preparation
  * **A.5.25** — Assessment and decision on information security events
  * **A.5.26** — Response to information security incidents
  * **A.5.27** — Learning from information security incidents
  * **A.5.28** — Collection of evidence
  * **A.5.29** — Information security during disruption
  * **A.6.8** — Information security event reporting
  * **A.8.15** — Logging
  * **A.8.16** — Monitoring activities
