# Defect Log (Sample) – System & Integration Testing

**Project:** Enterprise Procurement & Inventory Management System (EPIMS)  
**Test Phase:** System Testing / Integration Testing  
**Defect Tracking Tool:** JIRA (simulated)

---

## Defect Summary

| Defect ID | Title | Module | Severity | Priority | Status | Linked Req | Linked TC |
|----------|-------|--------|----------|----------|--------|-----------|----------|
| BUG-001 | Duplicate vendor allowed with same Tax ID | Vendor Mgmt | High | P1 | Open | FR-VM-03 | TC-VM-02 |
| BUG-002 | PO number not auto-generated after Save | Purchase Order | High | P1 | Fixed / Retest | FR-PO-02 | TC-PO-01 |
| BUG-003 | PO approval allowed for inactive vendor | Purchase Order | Critical | P0 | Open | FR-PO-04 | TC-PO-02 |
| BUG-004 | GRN accepts received qty > PO qty | Goods Receipt | High | P1 | Fixed / Retest | FR-GR-02 | TC-GR-01 |
| BUG-005 | 3-way matching passes with price mismatch | Invoice Matching | Medium | P2 | Open | FR-IM-02 | (Add TC-IM-02) |
| BUG-006 | Ledger posting creates duplicate entries on refresh | Financial Posting | Critical | P0 | Open | FR-FP-01 | (Add TC-FP-02) |

---

## Defect Details (Sample)

### BUG-001 – Duplicate vendor allowed with same Tax ID
- **Module:** Vendor Management  
- **Severity / Priority:** High / P1  
- **Environment:** QA  
- **Precondition:** Vendor exists with Tax ID = `TX-889900`  
- **Steps to Reproduce:**
  1. Navigate to Vendor Management → Create Vendor
  2. Enter valid vendor details
  3. Enter Tax ID = `TX-889900` (existing)
  4. Click Save
- **Expected Result:** System blocks creation and shows duplicate validation error
- **Actual Result:** Vendor is created successfully with duplicate Tax ID
- **Impact:** Duplicate vendor records cause PO and finance reconciliation issues
- **Status:** Open

---

### BUG-003 – PO approval allowed for inactive vendor
- **Module:** Purchase Order  
- **Severity / Priority:** Critical / P0  
- **Environment:** QA  
- **Precondition:** Vendor status = Inactive  
- **Steps to Reproduce:**
  1. Create PO for inactive vendor
  2. Submit for approval
  3. Approver clicks Approve
- **Expected Result:** System blocks approval and prompts “Vendor inactive”
- **Actual Result:** PO is approved successfully
- **Impact:** Risk of unauthorized procurement + audit compliance violation
- **Status:** Open
