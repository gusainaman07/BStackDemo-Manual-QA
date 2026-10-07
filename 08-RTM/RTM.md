# BStackDemo Manual QA Testing – Requirements Traceability Matrix

## 1. Document Information

| Field             | Details                          |
| ----------------- | -------------------------------- |
| Project           | BStackDemo Manual QA Testing     |
| Application       | BStackDemo                       |
| Document          | Requirements Traceability Matrix |
| Testing Type      | Manual Testing                   |
| Requirements      | 17                               |
| Test Scenarios    | 96                               |
| Test Cases        | 128                              |
| Defects           | 10                               |
| Execution Dataset | Simulated Portfolio Execution    |
| Version           | 1.0                              |

---

# 2. Purpose

The Requirements Traceability Matrix (RTM) establishes traceability between:

```text
Requirements
     ↓
Test Scenarios
     ↓
Test Cases
     ↓
Execution
     ↓
Defects
```

The objective is to ensure that every functional and non-functional requirement has appropriate test coverage.

---

# 3. Traceability Legend

| Symbol  | Meaning                                       |
| ------- | --------------------------------------------- |
| ✓       | Covered                                       |
| FAIL    | Covered but failed during simulated execution |
| BLOCKED | Covered but execution was blocked             |
| —       | Not applicable                                |

---

# 4. Requirement Coverage Summary

| Requirement ID | Requirement              | Scenario Coverage | Test Case Coverage | Execution Result |
| -------------- | ------------------------ | ----------------: | -----------------: | ---------------- |
| FR-001         | Homepage & Navigation    |                10 |                 10 | PASS             |
| FR-002         | Product Listing          |                10 |                 12 | FAIL             |
| FR-003         | Product Search           |                10 |                 10 | PASS             |
| FR-004         | Product Filtering        |                10 |                 12 | FAIL             |
| FR-005         | Product Sorting          |                 6 |                  8 | PASS             |
| FR-006         | Product Details          |                 5 |                 10 | FAIL             |
| FR-007         | Shopping Cart            |                 9 |                 18 | FAIL             |
| FR-008         | User Authentication      |                 7 |                 10 | FAIL             |
| FR-009         | Checkout                 |                10 |                 15 | FAIL             |
| FR-010         | End-to-End Purchase      |                 6 |                  8 | BLOCKED          |
| FR-011         | UI & Usability           |                 6 |                  8 | PASS             |
| FR-012         | Session & Error Handling |                 7 |                  7 | FAIL             |
| NFR-001        | Usability                |                 2 |                  8 | PASS             |
| NFR-002        | Compatibility            |                 1 |                  2 | PASS             |
| NFR-003        | Responsiveness           |                 1 |                  2 | PASS             |
| NFR-004        | Reliability              |                 1 |                  3 | FAIL             |
| NFR-005        | Data Integrity           |                 2 |                  5 | FAIL             |

> Some test cases intentionally provide coverage for more than one requirement. Therefore, requirement-level test-case totals can be greater than the overall 128 unique test cases.

---

# 5. Functional Requirements Traceability

## FR-001 – Homepage & Navigation

**Requirement:** The application should provide functional navigation between major application pages.

| Scenario | Test Cases | Result |
| -------- | ---------- | ------ |
| TS-001   | TC-NAV-001 | PASS   |
| TS-002   | TC-NAV-002 | PASS   |
| TS-003   | TC-NAV-003 | PASS   |
| TS-004   | TC-NAV-004 | PASS   |
| TS-005   | TC-NAV-005 | PASS   |
| TS-006   | TC-NAV-006 | PASS   |
| TS-007   | TC-NAV-007 | PASS   |
| TS-008   | TC-NAV-008 | PASS   |
| TS-009   | TC-NAV-009 | PASS   |
| TS-010   | TC-NAV-010 | PASS   |

**Coverage:** 100%

**Requirement Status:** PASS

---

# FR-002 – Product Listing

**Requirement:** The application should display products with relevant product information and provide product-listing interactions.

| Scenario | Test Cases               | Result         |
| -------- | ------------------------ | -------------- |
| TS-011   | TC-PROD-001, TC-PROD-011 | PASS           |
| TS-012   | TC-PROD-002              | PASS           |
| TS-013   | TC-PROD-003              | PASS           |
| TS-014   | TC-PROD-004              | PASS           |
| TS-015   | TC-PROD-005              | PASS           |
| TS-016   | TC-PROD-006              | FAIL – BUG-001 |
| TS-017   | TC-PROD-007              | PASS           |
| TS-018   | TC-PROD-008, TC-PROD-012 | PASS           |
| TS-019   | TC-PROD-009              | PASS           |
| TS-020   | TC-PROD-010              | FAIL – BUG-006 |

**Requirement Status:** FAIL

**Related Defects:** BUG-001, BUG-006

---

# FR-003 – Product Search

**Requirement:** Users should be able to search the product catalogue using relevant search terms.

| Scenario | Test Cases    | Result |
| -------- | ------------- | ------ |
| TS-021   | TC-SEARCH-001 | PASS   |
| TS-022   | TC-SEARCH-002 | PASS   |
| TS-023   | TC-SEARCH-003 | PASS   |
| TS-024   | TC-SEARCH-004 | PASS   |
| TS-025   | TC-SEARCH-005 | PASS   |
| TS-026   | TC-SEARCH-006 | PASS   |
| TS-027   | TC-SEARCH-007 | PASS   |
| TS-028   | TC-SEARCH-008 | PASS   |
| TS-029   | TC-SEARCH-009 | PASS   |
| TS-030   | TC-SEARCH-010 | PASS   |

**Coverage:** 100%

**Requirement Status:** PASS

---

# FR-004 – Product Filtering

**Requirement:** Users should be able to filter products using available filter criteria.

| Scenario | Test Cases                   | Result         |
| -------- | ---------------------------- | -------------- |
| TS-031   | TC-FILTER-001                | PASS           |
| TS-032   | TC-FILTER-002, TC-FILTER-011 | FAIL – BUG-002 |
| TS-033   | TC-FILTER-003, TC-FILTER-012 | PASS           |
| TS-034   | TC-FILTER-004                | PASS           |
| TS-035   | TC-FILTER-005                | PASS           |
| TS-036   | TC-FILTER-006                | PASS           |
| TS-037   | TC-FILTER-007                | PASS           |
| TS-038   | TC-FILTER-008                | PASS           |
| TS-039   | TC-FILTER-009                | PASS           |
| TS-040   | TC-FILTER-010                | PASS           |

**Requirement Status:** FAIL

**Related Defect:** BUG-002

---

# FR-005 – Product Sorting

**Requirement:** Users should be able to sort products using the available sorting options.

| Scenario | Test Cases               | Result |
| -------- | ------------------------ | ------ |
| TS-041   | TC-SORT-001, TC-SORT-008 | PASS   |
| TS-042   | TC-SORT-002              | PASS   |
| TS-043   | TC-SORT-003              | PASS   |
| TS-044   | TC-SORT-004, TC-SORT-007 | PASS   |
| TS-045   | TC-SORT-005              | PASS   |
| TS-046   | TC-SORT-006              | PASS   |

**Requirement Status:** PASS

---

# FR-006 – Product Details

**Requirement:** Users should be able to open and interact with individual product-detail pages.

| Scenario | Test Cases                                                                | Result         |
| -------- | ------------------------------------------------------------------------- | -------------- |
| TS-047   | TC-DETAIL-001, TC-DETAIL-009                                              | FAIL – BUG-009 |
| TS-048   | TC-DETAIL-002, TC-DETAIL-003, TC-DETAIL-004, TC-DETAIL-008, TC-DETAIL-010 | PASS           |
| TS-049   | TC-DETAIL-005                                                             | PASS           |
| TS-050   | TC-DETAIL-006                                                             | PASS           |
| TS-051   | TC-DETAIL-007                                                             | PASS           |

**Requirement Status:** FAIL

**Related Defect:** BUG-009

---

# FR-007 – Shopping Cart

**Requirement:** Users should be able to add, remove and manage products in the shopping cart.

| Scenario | Test Cases                            | Result            |
| -------- | ------------------------------------- | ----------------- |
| TS-052   | TC-CART-001                           | PASS              |
| TS-053   | TC-CART-003, TC-CART-004              | PASS              |
| TS-054   | TC-CART-002                           | PASS              |
| TS-055   | TC-CART-005, TC-CART-006              | PASS              |
| TS-056   | TC-CART-007, TC-CART-008, TC-CART-009 | FAIL – BUG-003    |
| TS-057   | TC-CART-010, TC-CART-013, TC-CART-014 | PASS              |
| TS-058   | TC-CART-011, TC-CART-012              | FAIL – BUG-007    |
| TS-059   | TC-CART-015                           | PASS              |
| TS-060   | TC-CART-016                           | PASS              |
| TS-068   | TC-CART-017                           | PASS              |
| TS-069   | TC-CART-018                           | BLOCKED – BLK-001 |

**Requirement Status:** FAIL

**Related Defects:** BUG-003, BUG-007

**Related Blocker:** BLK-001

---

# FR-008 – User Authentication

**Requirement:** Users should be able to authenticate using valid credentials and receive appropriate feedback for invalid credentials.

| Scenario | Test Cases                            | Result         |
| -------- | ------------------------------------- | -------------- |
| TS-061   | TC-AUTH-001                           | PASS           |
| TS-062   | TC-AUTH-002                           | PASS           |
| TS-063   | TC-AUTH-003                           | PASS           |
| TS-064   | TC-AUTH-004                           | FAIL – BUG-004 |
| TS-065   | TC-AUTH-005, TC-AUTH-006, TC-AUTH-007 | PASS           |
| TS-066   | TC-AUTH-008                           | PASS           |
| TS-067   | TC-AUTH-009, TC-AUTH-010              | PASS           |

**Requirement Status:** FAIL

**Related Defect:** BUG-004

---

# FR-009 – Checkout

**Requirement:** Users should be able to complete checkout using valid information and receive appropriate validation feedback.

| Scenario | Test Cases                                                         | Result         |
| -------- | ------------------------------------------------------------------ | -------------- |
| TS-068   | TC-CHECKOUT-001, TC-CHECKOUT-015                                   | PASS / BLOCKED |
| TS-069   | TC-CHECKOUT-002, TC-CHECKOUT-003, TC-CHECKOUT-004, TC-CHECKOUT-011 | PASS           |
| TS-070   | TC-CHECKOUT-005                                                    | PASS           |
| TS-071   | TC-CHECKOUT-006                                                    | PASS           |
| TS-072   | TC-CHECKOUT-007                                                    | PASS           |
| TS-073   | TC-CHECKOUT-008                                                    | PASS           |
| TS-074   | TC-CHECKOUT-009                                                    | PASS           |
| TS-075   | TC-CHECKOUT-010                                                    | FAIL – BUG-008 |
| TS-076   | TC-CHECKOUT-012                                                    | FAIL – BUG-005 |
| TS-077   | TC-CHECKOUT-013                                                    | PASS           |
| TS-083   | TC-CHECKOUT-014                                                    | PASS           |

**Requirement Status:** FAIL

**Related Defects:** BUG-005, BUG-008

**Related Blocker:** BLK-002

---

# FR-010 – End-to-End Purchase

**Requirement:** The application should support a complete purchase journey from product selection through order confirmation.

| Scenario | Test Cases                         | Result         |
| -------- | ---------------------------------- | -------------- |
| TS-078   | TC-E2E-001, TC-E2E-007, TC-E2E-008 | PASS / BLOCKED |
| TS-079   | TC-E2E-002                         | PASS           |
| TS-080   | TC-E2E-003                         | PASS           |
| TS-081   | TC-E2E-004                         | PASS           |
| TS-082   | TC-E2E-005                         | PASS           |
| TS-083   | TC-E2E-006                         | PASS           |

**Requirement Status:** BLOCKED

**Related Blocker:** BLK-003

---

# FR-011 – UI & Usability

**Requirement:** The application should provide a consistent and usable interface.

| Scenario | Test Cases           | Result |
| -------- | -------------------- | ------ |
| TS-084   | TC-UI-001, TC-UI-008 | PASS   |
| TS-085   | TC-UI-002, TC-UI-003 | PASS   |
| TS-086   | TC-UI-004            | PASS   |
| TS-087   | TC-UI-005            | PASS   |
| TS-088   | TC-UI-006            | PASS   |
| TS-089   | TC-UI-007            | PASS   |

**Requirement Status:** PASS

---

# FR-012 – Session & Error Handling

**Requirement:** The application should maintain predictable behavior during navigation, refresh and error conditions.

| Scenario | Test Cases     | Result         |
| -------- | -------------- | -------------- |
| TS-090   | TC-SESSION-001 | PASS           |
| TS-091   | TC-SESSION-002 | PASS           |
| TS-092   | TC-SESSION-003 | PASS           |
| TS-093   | TC-SESSION-004 | PASS           |
| TS-094   | TC-SESSION-005 | PASS           |
| TS-095   | TC-SESSION-006 | PASS           |
| TS-096   | TC-SESSION-007 | FAIL – BUG-010 |

**Requirement Status:** FAIL

**Related Defect:** BUG-010

---

# 6. Non-Functional Requirements Traceability

## NFR-001 – Usability

**Requirement:** The application should provide a clear and usable interface.

| Test Cases | Result |
| ---------- | ------ |
| TC-UI-001  | PASS   |
| TC-UI-002  | PASS   |
| TC-UI-003  | PASS   |
| TC-UI-004  | PASS   |
| TC-UI-005  | PASS   |
| TC-UI-006  | PASS   |
| TC-UI-007  | PASS   |
| TC-UI-008  | PASS   |

**Requirement Status:** PASS

---

# NFR-002 – Compatibility

**Requirement:** The application should function correctly in supported browser environments.

| Test Cases | Result |
| ---------- | ------ |
| TC-UI-007  | PASS   |
| TC-NAV-010 | PASS   |

**Requirement Status:** PASS

> Full cross-browser compatibility requires execution on multiple supported browsers. This portfolio execution represents Chrome-based testing only.

---

# NFR-003 – Responsiveness

**Requirement:** The application should remain usable across supported viewport sizes.

| Test Cases | Result |
| ---------- | ------ |
| TC-UI-007  | PASS   |
| TC-UI-008  | PASS   |

**Requirement Status:** PASS

---

# NFR-004 – Reliability

**Requirement:** Application behavior should remain stable during normal user workflows.

| Test Cases     | Result         |
| -------------- | -------------- |
| TC-SESSION-001 | PASS           |
| TC-SESSION-002 | PASS           |
| TC-SESSION-007 | FAIL – BUG-010 |

**Requirement Status:** FAIL

**Related Defect:** BUG-010

---

# NFR-005 – Data Integrity

**Requirement:** Product, cart, quantity and checkout data should remain consistent across user operations.

| Test Cases      | Result         |
| --------------- | -------------- |
| TC-CART-007     | FAIL – BUG-003 |
| TC-CART-011     | FAIL – BUG-007 |
| TC-CART-012     | PASS           |
| TC-CHECKOUT-012 | FAIL – BUG-005 |
| TC-SESSION-007  | FAIL – BUG-010 |

**Requirement Status:** FAIL

**Related Defects:** BUG-003, BUG-005, BUG-007, BUG-010

---

# 7. Defect Traceability

The following table connects defects back to requirements.

| Defect  | Requirement      | Test Case       | Severity | Priority |
| ------- | ---------------- | --------------- | -------- | -------- |
| BUG-001 | FR-002           | TC-PROD-006     | S2       | P1       |
| BUG-002 | FR-004           | TC-FILTER-006   | S3       | P2       |
| BUG-003 | FR-007 / NFR-005 | TC-CART-007     | S2       | P1       |
| BUG-004 | FR-008           | TC-AUTH-004     | S2       | P1       |
| BUG-005 | FR-009 / NFR-005 | TC-CHECKOUT-012 | S1       | P1       |
| BUG-006 | FR-002           | TC-PROD-010     | S3       | P2       |
| BUG-007 | FR-007 / NFR-005 | TC-CART-011     | S2       | P1       |
| BUG-008 | FR-009           | TC-CHECKOUT-010 | S3       | P2       |
| BUG-009 | FR-006           | TC-DETAIL-009   | S2       | P1       |
| BUG-010 | FR-012 / NFR-004 | TC-SESSION-007  | S2       | P1       |

---

# 8. Blocker Traceability

| Blocker | Requirement | Test Case       | Reason                              |
| ------- | ----------- | --------------- | ----------------------------------- |
| BLK-001 | FR-007      | TC-CART-018     | Authentication/session prerequisite |
| BLK-002 | FR-009      | TC-CHECKOUT-015 | Checkout prerequisite               |
| BLK-003 | FR-010      | TC-E2E-008      | Multi-product purchase prerequisite |

---

# 9. Requirement Coverage Metrics

### Functional Requirements

```text
12 / 12 Functional Requirements have test coverage
```

**Functional Requirement Coverage: 100%**

### Non-Functional Requirements

```text
5 / 5 Non-Functional Requirements have test coverage
```

**Non-Functional Requirement Coverage: 100%**

### Overall Requirement Coverage

```text
17 / 17 Requirements have associated test coverage
```

**Overall Requirement Coverage: 100%**

---

# 10. Test Scenario Coverage

| Requirement | Scenarios Covered |
| ----------- | ----------------: |
| FR-001      |                10 |
| FR-002      |                10 |
| FR-003      |                10 |
| FR-004      |                10 |
| FR-005      |                 6 |
| FR-006      |                 5 |
| FR-007      |                11 |
| FR-008      |                 7 |
| FR-009      |                11 |
| FR-010      |                 6 |
| FR-011      |                 6 |
| FR-012      |                 7 |

The project contains **96 unique test scenarios** overall.

---

# 11. Test Case Coverage

The project contains **128 unique test cases**.

| Module                   | Test Cases |
| ------------------------ | ---------: |
| Homepage & Navigation    |         10 |
| Product Listing          |         12 |
| Product Search           |         10 |
| Product Filtering        |         12 |
| Product Sorting          |          8 |
| Product Details          |         10 |
| Shopping Cart            |         18 |
| Authentication           |         10 |
| Checkout                 |         15 |
| End-to-End Purchase      |          8 |
| UI & Usability           |          8 |
| Session & Error Handling |          7 |
| **Total**                |    **128** |

---

# 12. RTM Quality Checks

The following checks should be satisfied before considering the RTM complete:

* [x] Every functional requirement has scenario coverage.
* [x] Every non-functional requirement has test coverage.
* [x] Test scenarios are mapped to test cases.
* [x] Failed test cases are connected to defects.
* [x] Blocked test cases are connected to blockers.
* [x] Critical and major defects can be traced to requirements.
* [x] Test execution results are represented.
* [x] Requirement coverage is measurable.

---

# 13. Traceability Flow

The complete QA traceability chain is:

```text
FR-009 Checkout
      ↓
TS-076 Checkout Completion
      ↓
TC-CHECKOUT-012
      ↓
FAIL
      ↓
BUG-005
      ↓
Retest
      ↓
Regression
```

Another example:

```text
FR-007 Shopping Cart
      ↓
TS-058 Cart Total
      ↓
TC-CART-011
      ↓
FAIL
      ↓
BUG-007
      ↓
Retest
      ↓
Regression
```

---

# 14. RTM Conclusion

The RTM provides complete traceability across the BStackDemo manual QA project.

The current simulated execution shows:

* **17/17 requirements covered**
* **96 scenarios documented**
* **128 test cases executed**
* **115 passed**
* **10 failed**
* **3 blocked**
* **10 defects logged**

The requirement coverage is complete, but several requirements remain at risk because of simulated failures and blockers.

Therefore:

> **Requirement Coverage: COMPLETE**

> **Release Readiness: NOT READY / HOLD**

The failed and blocked requirements must be addressed through defect resolution, retesting and regression testing before final release assessment.

---

# 15. Next QA Activity

The next stage is:

```text
Requirements
      ↓
Test Plan
      ↓
Test Scenarios
      ↓
Test Cases
      ↓
Test Data
      ↓
Test Execution
      ↓
Bug Reports
      ↓
RTM
      ↓
Regression Testing
      ↓
Test Summary
```

Next document:

`09-Regression/Regression_Suite.md`
