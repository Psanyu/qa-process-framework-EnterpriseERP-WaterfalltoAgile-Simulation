# Test Cases – Enterprise ERP (System Testing Phase)

---

## Module: Vendor Management

### TC-VM-01
**Requirement ID:** FR-VM-01  
**Scenario:** Create new vendor  
**Precondition:** User logged in as Procurement Admin  
**Test Steps:**
1. Navigate to Vendor Module
2. Click "Create Vendor"
3. Enter valid vendor details
4. Click Save
**Expected Result:** Vendor record created with unique Vendor ID

---

### TC-VM-02
**Requirement ID:** FR-VM-03  
**Scenario:** Prevent duplicate vendor creation  
**Precondition:** Vendor with same Tax ID already exists  
**Test Steps:**
1. Attempt to create vendor using existing Tax ID
2. Click Save
**Expected Result:** System displays duplicate validation error

---

## Module: Purchase Order

### TC-PO-01
**Requirement ID:** FR-PO-02  
**Scenario:** Auto-generation of PO number  
**Precondition:** Vendor exists  
**Test Steps:**
1. Create new PO
2. Select Vendor
3. Save PO
**Expected Result:** Unique PO number auto-generated

---

### TC-PO-02
**Requirement ID:** FR-PO-04  
**Scenario:** Prevent PO approval for inactive vendor  
**Precondition:** Vendor status = Inactive  
**Test Steps:**
1. Create PO for inactive vendor
2. Attempt approval
**Expected Result:** System blocks approval

---

## Module: Goods Receipt

### TC-GR-01
**Requirement ID:** FR-GR-02  
**Scenario:** Validate received quantity  
**Precondition:** Approved PO exists  
**Test Steps:**
1. Create GRN
2. Enter quantity greater than PO quantity
3. Submit
**Expected Result:** System displays quantity validation error

---

## Module: Invoice Matching

### TC-IM-01
**Requirement ID:** FR-IM-01  
**Scenario:** Successful 3-way matching  
**Precondition:** PO and GRN exist  
**Test Steps:**
1. Enter vendor invoice
2. Submit for validation
**Expected Result:** Invoice approved and ready for posting

---

## Module: Financial Posting

### TC-FP-01
**Requirement ID:** FR-FP-01  
**Scenario:** Ledger posting after validation  
**Precondition:** Invoice approved  
**Test Steps:**
1. Trigger financial posting
2. Verify ledger entry
**Expected Result:** Debit/Credit entry recorded successfully

----

### TC-IM-02
**Requirement ID:** FR-IM-02  
**Scenario:** Invoice price mismatch validation  
**Precondition:** Approved PO and GRN exist  
**Test Steps:**
1. Create vendor invoice
2. Enter unit price different from PO price
3. Submit for validation
**Expected Result:** System flags price discrepancy and blocks approval

---

### TC-FP-02
**Requirement ID:** FR-FP-01  
**Scenario:** Prevent duplicate ledger posting on refresh  
**Precondition:** Invoice approved for posting  
**Test Steps:**
1. Trigger financial posting
2. Refresh the page during processing
3. Verify ledger entries
**Expected Result:** Only one ledger entry is created
---
