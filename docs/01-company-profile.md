# Company Profile: CHMART

> **Document ID:** GRC-01 | **Framework:** ISO/IEC 27001 | **Status:** Baseline Scope

## 1. Organization Overview

| Attribute | Details |
| :--- | :--- |
| **Company Name** | CHMart |
| **Industry** | E-Commerce & Retail Technology |
| **Total Workforce** | 80 Employees (60 On-Site / 20 Remote) |
| **Operating Model** | Hybrid |

---

## 2. Work Environment & Infrastructure

* **Corporate Office (60 Staff):** Houses executive, finance, HR, and operations teams on managed corporate workstations connected via segmented office Wi-Fi and corporate VPN.
* **Remote Workforce (20 Staff):** Covers engineering, customer support, and digital marketing teams using company-issued laptops secured with Endpoint Detection and Response (EDR), full-disk encryption, and Single Sign-On (SSO) with Multi-Factor Authentication (MFA).

---

## 3. Core Systems & Platforms

| Platform | Role in Operations | Primary Users |
| :--- | :--- | :--- |
| **Microsoft 365** | Corporate email, internal messaging, document collaboration, and identity management | All Staff |
| **AWS** | Cloud hosting, backend microservices, production databases, and object storage | Engineering & DevOps |
| **Shopify** | Customer-facing e-commerce storefront, catalog, and order management | Operations & Support |
| **Stripe** | Online payment gateway, tokenization, and transaction processing | Finance & Automated Checkout |
| **GitHub** | Source code repositories, version control, and CI/CD deployment pipelines | Engineering |

---

## 4. Data Types Processed

| Data Category | Examples of Records | Primary Storage / Processor |
| :--- | :--- | :--- |
| **Customer Data** | Full names, email addresses, shipping/billing addresses, phone numbers, order history | Shopify, AWS |
| **Payment Data** | Tokenized card details, transaction IDs, billing confirmations, refund logs | Stripe |
| **HR Data** | Employee PII, payroll records, employment contracts, tax forms, performance reviews | Microsoft 365 |

---

> **Assumptions:** This company is fictional and was created solely for an ISO/IEC 27001 Information Security Management System (ISMS) risk assessment portfolio project.
