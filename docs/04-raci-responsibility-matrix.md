# RACI / RESPONSIBILITY MATRIX

## 1. Purpose of This Document

This document defines **clear responsibility boundaries** for the Invoice-to-Cash (I2C) process using a RACI model.

RACI ensures that:

* Every activity has a clear owner
* Accountability gaps are avoided
* Business and IT roles are aligned
* Escalations and audits are straightforward

---

## 2. Roles in Scope

| Role                           | Description                               |
| ------------------------------ | ----------------------------------------- |
| Business (Operations)          | Owns day-to-day invoicing operations      |
| Finance / Accounting           | Owns financial correctness and compliance |
| Business Systems Analyst (BSA) | Owns process & system alignment           |
| IT / ERP Team                  | Owns system configuration and stability   |
| Data / BI Team                 | Owns analytics and reporting              |

---

## 3. RACI Definitions

* **R – Responsible**: Executes the activity
* **A – Accountable**: Ultimately answerable (one only)
* **C – Consulted**: Provides input
* **I – Informed**: Kept up to date

---

## 4. Invoice-to-Cash RACI Matrix

| Activity                 | Business | Finance | BSA | IT / ERP | Data / BI |
| ------------------------ | -------- | ------- | --- | -------- | --------- |
| Invoice creation         | R        | I       | C   | I        | I         |
| Invoice submission       | R        | I       | C   | I        | I         |
| Invoice validation rules | C        | A       | R   | C        | I         |
| Duplicate detection      | I        | A       | R   | C        | I         |
| Invoice approval         | I        | A       | C   | I        | I         |
| AR posting               | I        | A       | C   | R        | I         |
| Revenue recognition      | I        | A       | C   | R        | I         |
| Data replication         | I        | I       | C   | R        | A         |
| Reconciliation KPIs      | I        | C       | R   | I        | A         |
| Exception monitoring     | I        | C       | R   | I        | A         |
| Issue escalation         | I        | A       | R   | C        | I         |

---

## 5. Key Design Principles

### One Accountable Party

* Each activity has **exactly one A**
* Prevents decision paralysis

### BSA as Integrator

* BSA is rarely Accountable
* BSA is often Responsible for **definition and alignment**

### Finance Owns Risk

* Financial correctness always sits with Finance

---

## 6. Common Anti-Patterns (Avoided)

| Anti-pattern                | Risk                  |
| --------------------------- | --------------------- |
| Multiple Accountables       | Conflicting decisions |
| IT owning finance rules     | Compliance failures   |
| BI fixing data              | Audit issues          |
| Business bypassing controls | Revenue leakage       |


