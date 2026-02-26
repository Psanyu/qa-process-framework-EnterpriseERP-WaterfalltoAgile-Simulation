**Sprint 1 Review Summary**

Sprint Goal: Enable user registration, login, browsing, and cart functionality.

Committed: 6 stories
Completed: 6 stories

**Testing Coverage:**
- Functional testing of all user stories
- Negative scenario validation
- Smoke testing on each new build
- Light regression of completed flows

**Defects Found:** 11 Total

**Critical:** 2

**Medium:** 5

**Low:** 4

**Key Defects Identified:**
- Cart price miscalculation when updating quantity (Critical)
- Login session timeout handling issue (Critical)
- Field validation message inconsistency (Medium)

**Risks / Observations:**

- Minor environment instability during mid-sprint deployment
- Limited test data variations for edge-case validation
- Tight testing window toward sprint closure

**Outcome:**
- All Critical defects resolved within sprint
- Medium defects addressed or planned
- Sprint goal achieved
- Features approved by Product Owner

**Sprint 2 Review Summary**

Sprint Goal: Enable checkout, payment integration, and order confirmation.

Committed: 5 stories
Completed: 5 stories

**Testing Coverage:**
- End-to-end checkout flow validation
- Payment success and failure scenarios
- Full regression of Sprint 1 + Sprint 2 functionality
- Cross-browser sanity validation

**Defects Found:** 9 Total

**Critical:** 1

**Medium:** 4

**Low:** 4

**Key Defects Identified:**
- Payment failure message not displayed correctly (Critical)
- Order confirmation email delay (Medium)
- UI alignment issue in checkout summary (Low)

**Risks / Observations:**
- External payment gateway sandbox latency
- High regression effort due to integration dependencies

**Outcome:**
- All Critical defects fixed and verified
- Regression passed successfully
- Product Owner approved release
- Release marked as production-ready
