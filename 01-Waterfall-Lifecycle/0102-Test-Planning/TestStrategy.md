# Test Strategy Document

## 1. Objective

This document defines the testing approach for the Enterprise Procurement & Inventory Management System (EPIMS) implemented under a structured Waterfall lifecycle.

The objective is to validate system functionality, integration accuracy, and data consistency before production release.

---

## 2. Scope of Testing

### In Scope
- Vendor Creation & Management
- Purchase Order Processing
- Goods Receipt (GRN)
- Inventory Updates
- 3-Way Invoice Matching
- Financial Ledger Posting

### Out of Scope
- Payroll Module
- HR Integration
- External Banking Gateway

---

## 3. Test Levels

The following test phases will be executed sequentially:

1. Unit Testing (by Development Team)
2. System Testing (by QA Team)
3. Integration Testing
4. User Acceptance Testing (UAT)
5. Regression Testing before release

---

## 4. Test Types

- Functional Testing
- Integration Testing
- Regression Testing
- Smoke Testing
- Backend Data Validation (SQL)
- Basic Performance Validation (simulated load scenarios)

---

## 5. Entry Criteria

- Approved BRD and FRS
- Stable build deployed in QA environment
- Test cases reviewed and approved

---

## 6. Exit Criteria

- 95% test cases passed
- No Critical or High severity defects open
- Regression cycle completed
- Test summary report approved

---

## 7. Environment

- Web-based ERP Application
- Backend: Oracle Database
- Defect Tracking Tool: JIRA (simulated)
- Test Management: HP ALM (simulated structure)

---

## 8. Risk & Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| Incomplete requirements | Medium | Early review & sign-off |
| Data mismatch between modules | High | Backend SQL validation |
| Build instability | Medium | Smoke testing before full regression |

