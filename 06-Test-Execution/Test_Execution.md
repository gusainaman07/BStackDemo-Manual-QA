# BStackDemo Manual QA Testing – Test Execution

## 1. Document Information

| Field              | Details                       |
| ------------------ | ----------------------------- |
| Project            | BStackDemo Manual QA Testing  |
| Application        | BStackDemo                    |
| Testing Type       | Manual Testing                |
| Execution Type     | Simulated Portfolio Execution |
| Total Test Cases   | 128                           |
| Passed             | 115                           |
| Failed             | 10                            |
| Blocked            | 3                             |
| Not Executed       | 0                             |
| Execution Status   | Completed                     |
| Release Assessment | HOLD                          |
| Version            | 1.0                           |

> **Important:** The execution results in this document are a **simulated portfolio dataset** created to demonstrate a complete QA workflow. They are not claimed to be results from an actual live execution of BStackDemo.

---

# 2. Execution Objective

The objective of this execution cycle is to evaluate the functional behavior of BStackDemo across:

* Homepage and navigation
* Product listing
* Product search
* Product filtering
* Product sorting
* Product details
* Shopping cart
* Authentication
* Checkout
* End-to-end purchase
* UI and usability
* Session and error handling

The execution covers all **128 planned manual test cases**.

---

# 3. Test Environment

| Environment Item  | Configuration           |
| ----------------- | ----------------------- |
| Application       | BStackDemo              |
| URL               | https://bstackdemo.com/ |
| Testing Type      | Manual                  |
| OS                | Windows                 |
| Browser           | Google Chrome           |
| Browser Type      | Chromium-based          |
| Network           | Internet                |
| Test Data         | Synthetic               |
| Execution Dataset | Simulated               |
| Automation        | Not Used                |
| API Testing       | Not Included            |

---

# 4. Execution Summary

| Status    |   Count | Percentage |
| --------- | ------: | ---------: |
| PASS      |     115 |     89.84% |
| FAIL      |      10 |      7.81% |
| BLOCKED   |       3 |      2.34% |
| **Total** | **128** |   **100%** |

### Pass Rate Excluding Blocked Cases

```text
Pass Rate = Passed / (Passed + Failed) × 100

          = 115 / (115 + 10) × 100

          = 92.00%
```

### Failure Rate Excluding Blocked Cases

```text
Failure Rate = Failed / (Passed + Failed) × 100

             = 10 / 125 × 100

             = 8.00%
```

---

# 5. Execution Status Legend

| Status  | Meaning                                                     |
| ------- | ----------------------------------------------------------- |
| PASS    | Actual/simulated behavior meets the expected result         |
| FAIL    | Actual/simulated behavior does not meet the expected result |
| BLOCKED | Test could not be completed because of a blocking condition |

---

# 6. Homepage & Navigation Execution

| TC ID      | Test Case                                                | Status | Defect / Blocker |
| ---------- | -------------------------------------------------------- | ------ | ---------------- |
| TC-NAV-001 | Verify BStackDemo homepage loads successfully            | PASS   | —                |
| TC-NAV-002 | Verify application logo/navigation is displayed          | PASS   | —                |
| TC-NAV-003 | Verify navigation to product listing                     | PASS   | —                |
| TC-NAV-004 | Verify navigation menu options                           | PASS   | —                |
| TC-NAV-005 | Verify home navigation                                   | PASS   | —                |
| TC-NAV-006 | Verify cart navigation                                   | PASS   | —                |
| TC-NAV-007 | Verify login/account navigation                          | PASS   | —                |
| TC-NAV-008 | Verify browser Back navigation                           | PASS   | —                |
| TC-NAV-009 | Verify browser Forward navigation                        | PASS   | —                |
| TC-NAV-010 | Verify navigation links do not lead to unexpected errors | PASS   | —                |

**Module Result:** 10 PASS / 0 FAIL / 0 BLOCKED

---

# 7. Product Listing Execution

| TC ID       | Test Case                                                      | Status | Defect / Blocker |
| ----------- | -------------------------------------------------------------- | ------ | ---------------- |
| TC-PROD-001 | Verify product listing page loads                              | PASS   | —                |
| TC-PROD-002 | Verify products display with required information              | PASS   | —                |
| TC-PROD-003 | Verify product names are visible                               | PASS   | —                |
| TC-PROD-004 | Verify product prices are visible                              | PASS   | —                |
| TC-PROD-005 | Verify product images are displayed                            | PASS   | —                |
| TC-PROD-006 | Verify Add to Cart from product listing                        | FAIL   | BUG-001          |
| TC-PROD-007 | Verify multiple products can be added                          | PASS   | —                |
| TC-PROD-008 | Verify product cards are clickable                             | PASS   | —                |
| TC-PROD-009 | Verify product listing after filtering                         | PASS   | —                |
| TC-PROD-010 | Verify product listing after sorting                           | FAIL   | BUG-006          |
| TC-PROD-011 | Verify product list remains usable after navigation            | PASS   | —                |
| TC-PROD-012 | Verify product list state after returning from product details | PASS   | —                |

**Module Result:** 10 PASS / 2 FAIL / 0 BLOCKED

---

# 8. Product Search Execution

| TC ID         | Test Case                             | Status | Defect / Blocker |
| ------------- | ------------------------------------- | ------ | ---------------- |
| TC-SEARCH-001 | Search using a valid product name     | PASS   | —                |
| TC-SEARCH-002 | Search using a partial product name   | PASS   | —                |
| TC-SEARCH-003 | Search using brand name               | PASS   | —                |
| TC-SEARCH-004 | Search using lowercase input          | PASS   | —                |
| TC-SEARCH-005 | Search using uppercase input          | PASS   | —                |
| TC-SEARCH-006 | Search using invalid product name     | PASS   | —                |
| TC-SEARCH-007 | Search using numeric input            | PASS   | —                |
| TC-SEARCH-008 | Search with empty input               | PASS   | —                |
| TC-SEARCH-009 | Search with leading/trailing spaces   | PASS   | —                |
| TC-SEARCH-010 | Clear search and restore product list | PASS   | —                |

**Module Result:** 10 PASS / 0 FAIL / 0 BLOCKED

---

# 9. Product Filtering Execution

| TC ID         | Test Case                                            | Status | Defect / Blocker |
| ------------- | ---------------------------------------------------- | ------ | ---------------- |
| TC-FILTER-001 | Filter products by Apple                             | PASS   | —                |
| TC-FILTER-002 | Filter products by Samsung                           | PASS   | —                |
| TC-FILTER-003 | Filter products by Google                            | PASS   | —                |
| TC-FILTER-004 | Filter products by OnePlus                           | PASS   | —                |
| TC-FILTER-005 | Filter products by Motorola                          | PASS   | —                |
| TC-FILTER-006 | Verify no-result filter state                        | FAIL   | BUG-002          |
| TC-FILTER-007 | Apply multiple filters                               | PASS   | —                |
| TC-FILTER-008 | Remove one active filter                             | PASS   | —                |
| TC-FILTER-009 | Clear all filters                                    | PASS   | —                |
| TC-FILTER-010 | Verify filter results after navigation               | PASS   | —                |
| TC-FILTER-011 | Verify filter state after search                     | PASS   | —                |
| TC-FILTER-012 | Verify filtering does not display unrelated products | PASS   | —                |

**Module Result:** 11 PASS / 1 FAIL / 0 BLOCKED

---

# 10. Product Sorting Execution

| TC ID       | Test Case                                       | Status | Defect / Blocker |
| ----------- | ----------------------------------------------- | ------ | ---------------- |
| TC-SORT-001 | Sort products by price ascending                | PASS   | —                |
| TC-SORT-002 | Sort products by price descending               | PASS   | —                |
| TC-SORT-003 | Sort products alphabetically A-Z                | PASS   | —                |
| TC-SORT-004 | Sort products alphabetically Z-A                | PASS   | —                |
| TC-SORT-005 | Verify sorting after filtering                  | PASS   | —                |
| TC-SORT-006 | Verify sorting after search                     | PASS   | —                |
| TC-SORT-007 | Verify product state after changing sort option | PASS   | —                |
| TC-SORT-008 | Verify sorting does not remove valid products   | PASS   | —                |

**Module Result:** 8 PASS / 0 FAIL / 0 BLOCKED

---

# 11. Product Details Execution

| TC ID         | Test Case                                          | Status | Defect / Blocker |
| ------------- | -------------------------------------------------- | ------ | ---------------- |
| TC-DETAIL-001 | Open product details page                          | PASS   | —                |
| TC-DETAIL-002 | Verify product name on details page                | PASS   | —                |
| TC-DETAIL-003 | Verify product price on details page               | PASS   | —                |
| TC-DETAIL-004 | Verify product image on details page               | PASS   | —                |
| TC-DETAIL-005 | Verify product information consistency             | PASS   | —                |
| TC-DETAIL-006 | Add product to cart from details page              | PASS   | —                |
| TC-DETAIL-007 | Navigate back from details page                    | PASS   | —                |
| TC-DETAIL-008 | Verify details for different products              | PASS   | —                |
| TC-DETAIL-009 | Verify navigation between multiple product details | FAIL   | BUG-009          |
| TC-DETAIL-010 | Verify product details after returning from cart   | PASS   | —                |

**Module Result:** 9 PASS / 1 FAIL / 0 BLOCKED

---

# 12. Shopping Cart Execution

| TC ID       | Test Case                                     | Status | Defect / Blocker |
| ----------- | --------------------------------------------- | ------ | ---------------- |
| TC-CART-001 | Open empty shopping cart                      | PASS   | —                |
| TC-CART-002 | Add one product to cart                       | PASS   | —                |
| TC-CART-003 | Verify product appears in cart                | PASS   | —                |
| TC-CART-004 | Verify product price in cart                  | PASS   | —                |
| TC-CART-005 | Add multiple products to cart                 | PASS   | —                |
| TC-CART-006 | Verify multiple products in cart              | PASS   | —                |
| TC-CART-007 | Verify cart quantity display                  | FAIL   | BUG-003          |
| TC-CART-008 | Increase product quantity                     | PASS   | —                |
| TC-CART-009 | Decrease product quantity                     | PASS   | —                |
| TC-CART-010 | Remove product from cart                      | PASS   | —                |
| TC-CART-011 | Verify cart total calculation                 | FAIL   | BUG-007          |
| TC-CART-012 | Verify total after removing product           | PASS   | —                |
| TC-CART-013 | Verify cart after browser refresh             | PASS   | —                |
| TC-CART-014 | Verify cart state after navigation            | PASS   | —                |
| TC-CART-015 | Verify empty-cart state                       | PASS   | —                |
| TC-CART-016 | Navigate from cart to checkout                | PASS   | —                |
| TC-CART-017 | Verify cart behavior for unauthenticated user | PASS   | —                |
| TC-CART-018 | Verify cart state after login                 | PASS   | —                |

**Module Result:** 15 PASS / 2 FAIL / 1 BLOCKED

**Blocker:** `BLK-001`

---

# 13. Authentication Execution

| TC ID       | Test Case                      | Status | Defect / Blocker |
| ----------- | ------------------------------ | ------ | ---------------- |
| TC-AUTH-001 | Open login page                | PASS   | —                |
| TC-AUTH-002 | Verify login form fields       | PASS   | —                |
| TC-AUTH-003 | Login using valid credentials  | PASS   | —                |
| TC-AUTH-004 | Login using incorrect password | FAIL   | BUG-004          |
| TC-AUTH-005 | Login using invalid username   | PASS   | —                |
| TC-AUTH-006 | Login with empty username      | PASS   | —                |
| TC-AUTH-007 | Login with empty password      | PASS   | —                |
| TC-AUTH-008 | Login with both fields empty   | PASS   | —                |
| TC-AUTH-009 | Verify logged-in state         | PASS   | —                |
| TC-AUTH-010 | Verify logout functionality    | PASS   | —                |

**Module Result:** 9 PASS / 1 FAIL / 0 BLOCKED

---

# 14. Checkout Execution

| TC ID           | Test Case                                | Status  | Defect / Blocker |
| --------------- | ---------------------------------------- | ------- | ---------------- |
| TC-CHECKOUT-001 | Navigate to checkout with cart item      | PASS    | —                |
| TC-CHECKOUT-002 | Verify checkout form                     | PASS    | —                |
| TC-CHECKOUT-003 | Enter valid customer details             | PASS    | —                |
| TC-CHECKOUT-004 | Verify customer data is accepted         | PASS    | —                |
| TC-CHECKOUT-005 | Submit checkout with valid information   | PASS    | —                |
| TC-CHECKOUT-006 | Verify required-field validation         | PASS    | —                |
| TC-CHECKOUT-007 | Verify missing first-name validation     | PASS    | —                |
| TC-CHECKOUT-008 | Verify missing last-name validation      | PASS    | —                |
| TC-CHECKOUT-009 | Verify missing address validation        | PASS    | —                |
| TC-CHECKOUT-010 | Verify validation messages               | FAIL    | BUG-008          |
| TC-CHECKOUT-011 | Verify invalid postal-code handling      | PASS    | —                |
| TC-CHECKOUT-012 | Verify valid checkout completion         | FAIL    | BUG-005          |
| TC-CHECKOUT-013 | Verify order confirmation                | PASS    | —                |
| TC-CHECKOUT-014 | Verify checkout from E2E flow            | PASS    | —                |
| TC-CHECKOUT-015 | Verify checkout with multiple cart items | BLOCKED | BLK-002          |

**Module Result:** 13 PASS / 1 FAIL / 1 BLOCKED

---

# 15. End-to-End Purchase Execution

| TC ID      | Test Case                                  | Status  | Defect / Blocker |
| ---------- | ------------------------------------------ | ------- | ---------------- |
| TC-E2E-001 | Complete single-product purchase flow      | PASS    | —                |
| TC-E2E-002 | Complete purchase using product search     | PASS    | —                |
| TC-E2E-003 | Complete purchase after filtering          | PASS    | —                |
| TC-E2E-004 | Complete purchase after sorting            | PASS    | —                |
| TC-E2E-005 | Complete purchase from product details     | PASS    | —                |
| TC-E2E-006 | Verify order confirmation after purchase   | PASS    | —                |
| TC-E2E-007 | Verify complete user journey from homepage | PASS    | —                |
| TC-E2E-008 | Verify multi-product purchase journey      | BLOCKED | BLK-003          |

**Module Result:** 7 PASS / 0 FAIL / 1 BLOCKED

---

# 16. UI & Usability Execution

| TC ID     | Test Case                              | Status | Defect / Blocker |
| --------- | -------------------------------------- | ------ | ---------------- |
| TC-UI-001 | Verify overall page layout             | PASS   | —                |
| TC-UI-002 | Verify product-card consistency        | PASS   | —                |
| TC-UI-003 | Verify button visibility               | PASS   | —                |
| TC-UI-004 | Verify text readability                | PASS   | —                |
| TC-UI-005 | Verify navigation usability            | PASS   | —                |
| TC-UI-006 | Verify form usability                  | PASS   | —                |
| TC-UI-007 | Verify responsive behavior             | PASS   | —                |
| TC-UI-008 | Verify visual consistency across pages | PASS   | —                |

**Module Result:** 8 PASS / 0 FAIL / 0 BLOCKED

---

# 17. Session & Error Handling Execution

| TC ID          | Test Case                            | Status | Defect / Blocker |
| -------------- | ------------------------------------ | ------ | ---------------- |
| TC-SESSION-001 | Refresh page during normal browsing  | PASS   | —                |
| TC-SESSION-002 | Refresh page with cart item          | PASS   | —                |
| TC-SESSION-003 | Use browser Back during workflow     | PASS   | —                |
| TC-SESSION-004 | Use browser Forward during workflow  | PASS   | —                |
| TC-SESSION-005 | Verify state after reopening session | PASS   | —                |
| TC-SESSION-006 | Verify behavior after session reset  | PASS   | —                |
| TC-SESSION-007 | Verify application state consistency | FAIL   | BUG-010          |

**Module Result:** 6 PASS / 1 FAIL / 0 BLOCKED

---

# 18. Failed Test Cases

| Defect ID | Test Case       | Failure Area              | Severity | Priority |
| --------- | --------------- | ------------------------- | -------- | -------- |
| BUG-001   | TC-PROD-006     | Add to Cart               | S2       | P1       |
| BUG-002   | TC-FILTER-006   | No-result filter state    | S3       | P2       |
| BUG-003   | TC-CART-007     | Cart quantity             | S2       | P1       |
| BUG-004   | TC-AUTH-004     | Invalid password handling | S2       | P1       |
| BUG-005   | TC-CHECKOUT-012 | Checkout completion       | S1       | P1       |
| BUG-006   | TC-PROD-010     | Listing after sorting     | S3       | P2       |
| BUG-007   | TC-CART-011     | Cart total calculation    | S2       | P1       |
| BUG-008   | TC-CHECKOUT-010 | Validation messages       | S3       | P2       |
| BUG-009   | TC-DETAIL-009   | Product navigation        | S2       | P1       |
| BUG-010   | TC-SESSION-007  | State consistency         | S2       | P1       |

---

# 19. Blocked Test Cases

| Blocker ID | Test Case       | Reason                                                                                                       |
| ---------- | --------------- | ------------------------------------------------------------------------------------------------------------ |
| BLK-001    | TC-CART-018     | Required authentication/session state could not be established consistently in the simulated execution       |
| BLK-002    | TC-CHECKOUT-015 | Multi-product checkout prerequisite could not be completed because of the simulated checkout/cart dependency |
| BLK-003    | TC-E2E-008      | Multi-product purchase flow could not proceed because the prerequisite checkout condition was blocked        |

---

# 20. Defect Distribution

| Severity      | Number |
| ------------- | -----: |
| S1 – Critical |      1 |
| S2 – Major    |      6 |
| S3 – Minor    |      3 |
| S4 – Trivial  |      0 |
| **Total**     | **10** |

### Priority Distribution

| Priority    | Number |
| ----------- | -----: |
| P1 – High   |      7 |
| P2 – Medium |      3 |
| P3 – Low    |      0 |

---

# 21. Execution by Module

| Module                   |   Total |    Pass |   Fail | Blocked |
| ------------------------ | ------: | ------: | -----: | ------: |
| Homepage & Navigation    |      10 |      10 |      0 |       0 |
| Product Listing          |      12 |      10 |      2 |       0 |
| Product Search           |      10 |      10 |      0 |       0 |
| Product Filtering        |      12 |      11 |      1 |       0 |
| Product Sorting          |       8 |       8 |      0 |       0 |
| Product Details          |      10 |       9 |      1 |       0 |
| Shopping Cart            |      18 |      15 |      2 |       1 |
| Authentication           |      10 |       9 |      1 |       0 |
| Checkout                 |      15 |      13 |      1 |       1 |
| End-to-End Purchase      |       8 |       7 |      0 |       1 |
| UI & Usability           |       8 |       8 |      0 |       0 |
| Session & Error Handling |       7 |       6 |      1 |       0 |
| **Total**                | **128** | **115** | **10** |   **3** |

---

# 22. Execution Observations

The simulated execution identifies the following risk areas:

### High-Risk Areas

1. Shopping cart behavior
2. Checkout completion
3. Product-to-cart interaction
4. Authentication error handling
5. Application state consistency

### Medium-Risk Areas

1. Filtering empty states
2. Product sorting
3. Checkout validation
4. Product-detail navigation

### Low-Risk Areas

1. Homepage navigation
2. Basic product search
3. General UI usability
4. Basic sorting behavior

---

# 23. Defect Retest Requirement

The following failed cases require retesting after the corresponding defect is resolved:

| Test Case       | Defect  |
| --------------- | ------- |
| TC-PROD-006     | BUG-001 |
| TC-FILTER-006   | BUG-002 |
| TC-CART-007     | BUG-003 |
| TC-AUTH-004     | BUG-004 |
| TC-CHECKOUT-012 | BUG-005 |
| TC-PROD-010     | BUG-006 |
| TC-CART-011     | BUG-007 |
| TC-CHECKOUT-010 | BUG-008 |
| TC-DETAIL-009   | BUG-009 |
| TC-SESSION-007  | BUG-010 |

---

# 24. Execution Completion Criteria

The execution cycle is considered complete because:

* [x] All 128 planned test cases have an execution status.
* [x] Failed cases have defect references.
* [x] Blocked cases have blocker references.
* [x] Execution metrics have been calculated.
* [x] Failed test cases are identified for retesting.
* [x] High-risk areas are documented.
* [x] Regression testing is required after defect resolution.

---

# 25. Release Assessment

### Simulated Result: HOLD

The simulated execution contains:

* 10 failed test cases
* 3 blocked test cases
* 1 critical-severity defect
* 6 major-severity defects

Therefore, the simulated release decision is:

> **HOLD – Defects must be addressed and regression testing completed before release approval.**

This is a **portfolio simulation**, not a real production release decision.

---

# 26. Next QA Activity

After defect logging:

```text
Test Execution
      ↓
Defect Reporting
      ↓
Developer Fix
      ↓
Defect Retest
      ↓
Regression Testing
      ↓
Final Test Summary
      ↓
Release Recommendation
```

The next project document is:

`07-Bug-Reports/Bug_Reports.md`
