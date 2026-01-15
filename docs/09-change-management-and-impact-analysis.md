# CHANGE MANAGEMENT & IMPACT ANALYSIS (BSA GOVERNANCE CORE)

## 1. Purpose of This Document

This document demonstrates how a **Business Systems Analyst (BSA)** manages change in a controlled, transparent, and auditable way.

The goal is to ensure that **business needs evolve without breaking financial integrity, compliance, or system stability**.

---

## 2. Why Change Management Is Critical

In finance and ERP environments:

* Small changes can have **financial or audit impact**
* Uncontrolled changes increase **operational risk**
* Stakeholder alignment is mandatory

The BSA acts as the **gatekeeper between business demand and system change**.

---

## 3. Change Request (CR) Lifecycle

1. Change Request Submission
2. Impact Analysis
3. Stakeholder Review & Approval
4. Implementation Planning
5. Testing & Validation
6. Deployment
7. Post-Implementation Review

---

## 4. Change Request Types

| Change Type          | Example                         |
| -------------------- | ------------------------------- |
| Business Rule Change | New invoice validation rule     |
| System Enhancement   | New reconciliation KPI          |
| Regulatory Change    | Audit or compliance requirement |
| Reporting Change     | New Power BI dashboard          |

---

## 5. Impact Analysis Dimensions

For every change request, the BSA evaluates impact across:

### 5.1 Process Impact

* Invoice intake flow
* Exception handling
* Month-end close activities

### 5.2 System Impact

| System        | Impact Example             |
| ------------- | -------------------------- |
| Intake System | New validation logic       |
| ERP (SAP)     | Posting rule adjustment    |
| Data Platform | New data field replication |
| Power BI      | Dashboard update           |

### 5.3 Data Impact

* New or modified fields
* Historical data backfill
* Data quality risks

### 5.4 User Impact

* Finance users
* Operations users
* IT support teams

---

## 6. Risk Assessment

| Risk                        | Mitigation               |
| --------------------------- | ------------------------ |
| Incorrect financial posting | Extended SIT & UAT       |
| Audit non-compliance        | Auditor review           |
| Reporting inconsistency     | Reconciliation controls  |
| User confusion              | Training & communication |

---

## 7. Approval & Governance

| Role           | Responsibility          |
| -------------- | ----------------------- |
| Business Owner | Business approval       |
| Finance        | Financial correctness   |
| IT Lead        | Technical feasibility   |
| BSA            | End-to-end coordination |

---

## 8. Example Change Request

**CR Title:** Add Duplicate Invoice Threshold Check
**Reason:** Reduce false positives
**Impact:** Intake system, ERP validation, dashboards
**Risk Level:** Medium
**Decision:** Approved with extended testing

---

## 9. Communication Plan

| Audience       | Message                  |
| -------------- | ------------------------ |
| Business Users | What changes and why     |
| Finance        | Financial impact         |
| IT             | Technical implementation |
| Management     | Risk & timeline          |

---

## 10. Post-Implementation Review

The BSA ensures:

* Change objectives met
* No unexpected financial impact
* Lessons learned documented

---

## 11. BSA Value Demonstrated

This document shows the BSA’s ability to:

* Control scope and risk
* Protect financial integrity
* Coordinate stakeholders
* Support governance and audit readiness

