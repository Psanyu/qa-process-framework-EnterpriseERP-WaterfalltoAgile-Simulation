# Functional Requirement Document (FRD) 

## 1. System Overview

The Enterprise Procurement & Inventory Management System (EPIMS) is a web-based ERP application designed to automate procurement, inventory tracking, and financial reconciliation processes.

The system supports role-based access for Procurement, Warehouse, Finance, and Admin users.

---

## 2. Functional Modules

### 2.1 Vendor Management Module

**FR-VM-01**: System shall allow creation of new vendor records with unique Vendor ID.

**FR-VM-02**: System shall validate mandatory fields (Vendor Name, Tax ID, Address).

**FR-VM-03**: System shall prevent duplicate vendor entries based on Tax ID.

**FR-VM-04**: System shall allow vendor activation/deactivation.

---

### 2.2 Purchase Order (PO) Module

**FR-PO-01**: System shall allow creation of Purchase Orders linked to registered vendors.

**FR-PO-02**: System shall auto-generate unique PO number.

**FR-PO-03**: System shall support multi-level approval workflow.

**FR-PO-04**: System shall prevent PO approval if vendor is inactive.

---

### 2.3 Goods Receipt (GRN) Module

**FR-GR-01**: System shall allow warehouse users to create Goods Receipt Note (GRN) against approved PO.

**FR-GR-02**: System shall validate received quantity against PO quantity.

**FR-GR-03**: System shall update inventory stock upon GRN confirmation.

---

### 2.4 Invoice Matching Module

**FR-IM-01**: System shall perform 3-way matching between PO, GRN, and Vendor Invoice.

**FR-IM-02**: System shall flag discrepancies in quantity or price.

**FR-IM-03**: System shall calculate tax based on predefined tax rules.

---

### 2.5 Financial Posting Module

**FR-FP-01**: System shall post validated invoices to finance ledger.

**FR-FP-02**: System shall generate accounting entries (Debit/Credit).

**FR-FP-03**: System shall maintain transaction audit logs.

---

## 3. Non-Functional Requirements

**NFR-01**: System shall support 200 concurrent users.

**NFR-02**: Page response time shall not exceed 3 seconds under normal load.

**NFR-03**: System shall enforce role-based access control.

**NFR-04**: System shall maintain audit trail for all financial transactions.

---

## 4. Assumptions

- Backend database: Oracle
- Web-based user interface
- Integration with internal finance module only
- Daily build releases during QA phase
