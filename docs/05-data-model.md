# HIGH-LEVEL DATA MODEL

## 1. Purpose of This Document

This document defines the **high-level data model** for the Invoice-to-Cash (I2C) process. It identifies key entities, relationships, and ownership of data. The model provides clarity on:

* Source of truth for each data entity
* How data flows between systems
* Which system is responsible for updates and storage

---

## 2. Core Entities

| Entity                   | Description                                                     | Source of Truth           | Notes                                                        |
| ------------------------ | --------------------------------------------------------------- | ------------------------- | ------------------------------------------------------------ |
| Invoice                  | Represents client invoice, including header and line items      | Accounting ERP            | Created by client, validated by Intake System, posted to ERP |
| Accounts Receivable (AR) | Represents invoice balance, payment status                      | Accounting ERP            | Updated by ERP upon payment or adjustment                    |
| Revenue                  | Represents revenue recognition entries                          | Accounting ERP            | Must match Invoice and AR postings                           |
| Payment                  | Represents client payment                                       | Accounting ERP            | Linked to AR and Invoice                                     |
| Exception / Flag         | Represents invalid invoice, duplicate, or reconciliation issues | Invoice Intake / Power BI | For monitoring only, does not update ERP                     |
| KPI / Analytics          | Aggregated data for dashboards                                  | Power BI                  | Read-only, updated from Data Platform                        |

---

## 3. Relationships

* **Invoice → AR**: One-to-One or One-to-Many (partial payments)
* **Invoice → Revenue**: One-to-One (revenue recognized per invoice)
* **Payment → AR**: Many-to-One (payment can cover multiple invoices)
* **Exceptions → Invoice / AR**: Optional, indicates issue
* **KPI / Analytics → all entities**: Read-only aggregation for reporting

Visual diagram can be created in draw.io using **rectangles for entities** and **lines for relationships**, with arrows showing direction of data flow.

---

## 4. Ownership / Responsibility Summary

| Entity          | Responsible System        | Accountable Role |
| --------------- | ------------------------- | ---------------- |
| Invoice         | Accounting ERP            | Finance          |
| AR              | Accounting ERP            | Finance          |
| Revenue         | Accounting ERP            | Finance          |
| Payment         | Accounting ERP            | Finance          |
| Exceptions      | Invoice Intake / Power BI | BSA / Finance    |
| KPI / Analytics | Power BI                  | Data / BI Team   |

---

## 5. Design Principles

* Source of truth is **always ERP** for financial data
* Analytics and exceptions are **read-only replicas**
* Relationships are designed to support **reconciliation and control dashboards**
* BSA role ensures data model aligns with process and system responsibilities

