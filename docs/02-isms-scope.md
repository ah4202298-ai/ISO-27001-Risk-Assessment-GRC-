# ISMS Scope and Context: CHMart

> **Document ID:** GRC-02 | **Framework:** ISO/IEC 27001 (Clauses 4.1–4.3) | **Status:** Baseline Scope

## 1. Purpose
This document defines the boundaries and applicability of the Information Security Management System (ISMS) for **CHMart**, as well as the internal and external stakeholders relevant to information security.

---

## 2. ISMS Scope Boundaries

| Boundary | Included / Excluded Assets & Operations |
| :--- | :--- |
| **In Scope** | • **Physical Locations:** All corporate offices and on-site workspaces.<br>• **Personnel:** All full-time, part-time, and remote employees.<br>• **Cloud & SaaS Systems:** Microsoft 365, AWS, Shopify, Stripe, and GitHub.<br>• **Information Assets:** All customer data, payment transaction records, HR data, and source code. |
| **Out of Scope** | • **Unmanaged Devices:** Personal employee devices (BYOD) not enrolled in corporate endpoint management or used for work.<br>• **Third-Party Infrastructure:** Underlying physical data center facilities managed by cloud providers (AWS, Microsoft, Shopify, Stripe, GitHub) under the Shared Responsibility Model.<br>• **Personal Accounts:** Non-corporate email and personal cloud storage accounts. |

---

## 3. Interested Parties & Security Expectations

| Interested Party | Key Security & Compliance Expectations |
| :--- | :--- |
| **Customers** | Protection of personal identifiable information (PII), secure checkout experience, data privacy, and transparency in data handling. |
| **Executive Management** | Business continuity, operational resilience, protection of brand reputation, and measurable risk reduction. |
| **Regulators & Legal Authorities** | Compliance with applicable data protection laws, privacy regulations, and statutory breach-notification timelines. |
| **Payment Providers (Stripe)** | Strict adherence to Payment Card Industry Data Security Standard (PCI DSS) requirements and secure payment tokenization. |

---

> **Assumptions:** This ISMS scope statement applies to the fictional organization CHMart and is created for an ISO/IEC 27001 GRC portfolio project.
