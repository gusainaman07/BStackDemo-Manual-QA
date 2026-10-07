# Test Summary Report

## BStackDemo — Manual QA Testing Project

**Project:** BStackDemo Manual QA Testing
**Application:** BStackDemo E-commerce Web Application
**Testing Type:** Manual Functional & Non-Functional Testing
**Test Level:** System / End-to-End
**Primary Browser:** Google Chrome / Chromium
**Operating System:** Windows
**Total Requirements:** 17
**Total Test Scenarios:** 96
**Total Test Cases:** 128
**Initial Defects Identified:** 10
**Regression Test Cases:** 30
**Regression Result:** 30/30 PASS
**Document Status:** Final Portfolio Summary
**Data Classification:** Simulated Portfolio Testing Data

> **Important:** The test execution results, defects, blockers, and regression results documented in this repository are **simulated portfolio data created for demonstration of QA methodology and documentation skills**. They must not be interpreted as actual production defects or an official QA report for BStackDemo.

---

## 1. Executive Summary

This document provides the final summary of the manual testing activities performed for the BStackDemo e-commerce web application as part of a portfolio-based QA project.

The testing process covered the complete customer-facing shopping journey, including:

* Homepage and navigation
* Product listing
* Product search
* Product filtering
* Product sorting
* Product details
* Shopping cart
* User authentication
* Checkout
* End-to-end purchase flow
* UI and usability
* Session and error handling

A total of **128 test cases** were designed and executed against **17 documented requirements**.

The initial simulated execution resulted in:

* **115 PASS**
* **10 FAIL**
* **3 BLOCKED**

The initial execution therefore identified **10 simulated defects** and **3 simulated blockers**.

Following simulated defect resolution, a focused regression suite containing **30 test cases** was executed.

The regression result was:

* **30 PASS**
* **0 FAIL**
* **0 BLOCKED**
* **100% regression pass rate**

Based on the simulated post-fix regression results, the application is assessed as:

> **Conditionally Ready for Release — Pending Final QA Sign-off and Verification**

This recommendation is specific to the simulated portfolio exercise and does not represent an actual release approval for the live BStackDemo application.

---

# 2. Testing Objective

The primary objective of this testing project was to demonstrate a complete manual QA lifecycle for an e-commerce web application.

The testing activities were designed to verify that:

1. Major application features work according to defined requirements.
2. Users can browse and search for products.
3. Product filtering and sorting behave correctly.
4. Product information is displayed correctly.
5. Users can add, update, and remove products from the cart.
6. Authentication behavior is handled correctly.
7. Checkout validation works as expected.
8. A user can complete the intended purchase workflow.
9. The interface remains usable and consistent.
10. Application state is maintained correctly during common user interactions.
11. Defects are documented with sufficient reproduction information.
12. Requirements can be traced to test scenarios and test cases.

---

# 3. Scope of Testing

## 3.1 In Scope

### Functional Testing

* Homepage
* Navigation
* Product listing
* Product search
* Product filtering
* Product sorting
* Product details
* Shopping cart
* Authentication
* Checkout
* Purchase workflow
* Error handling
* Session/state behavior

### Non-Functional Testing

* Basic usability
* UI consistency
* Browser compatibility
* Basic responsive behavior
* Reliability during normal user flows
* Data consistency from a user perspective

### QA Activities

* Requirement analysis
* Test scenario design
* Test case design
* Test data preparation
* Test execution
* Defect identification
* Defect reporting
* Requirement traceability
* Regression testing
* Test summary reporting

---

# 4. Out of Scope

The following activities were intentionally excluded from this project:

* API testing
* Database testing
* Performance/load testing
* Security penetration testing
* Automation testing
* Selenium
* Playwright
* Cypress
* Postman
* Source-code testing
* Backend unit testing
* Infrastructure testing
* Production monitoring

The project is intentionally focused on **manual QA testing**.

---

# 5. Test Environment

| Component          | Configuration                      |
| ------------------ | ---------------------------------- |
| Application        | BStackDemo                         |
| Testing Type       | Manual                             |
| OS                 | Windows                            |
| Primary Browser    | Google Chrome / Chromium           |
| Test Level         | System Testing                     |
| Test Approach      | Requirement-based + Scenario-based |
| Execution Dataset  | Simulated                          |
| Defect Dataset     | Simulated                          |
| Regression Dataset | Simulated                          |

---

# 6. Requirements Coverage

A total of **17 requirements** were documented:

* 12 Functional Requirements
* 5 Non-Functional Requirements

All documented requirements were mapped to test scenarios and test cases.

| Requirement Type            |  Total | Covered | Coverage |
| --------------------------- | -----: | ------: | -------: |
| Functional Requirements     |     12 |      12 |     100% |
| Non-Functional Requirements |      5 |       5 |     100% |
| **Total**                   | **17** |  **17** | **100%** |

### Requirement Coverage Assessment

**Requirement Coverage = 17 / 17 × 100 = 100%**

The RTM demonstrates traceability between:

**Requirement → Test Scenario → Test Case → Execution Result → Defect**

Refer to:

`08-RTM/RTM.md`

for detailed requirement traceability.

---

# 7. Test Scenario Summary

A total of **96 test scenarios** were created.

| Module                   | Scenario Count |
| ------------------------ | -------------: |
| Homepage & Navigation    |             10 |
| Product Listing          |             10 |
| Product Search           |             10 |
| Product Filtering        |             10 |
| Product Sorting          |              6 |
| Product Details          |              5 |
| Shopping Cart            |              9 |
| Authentication           |              7 |
| Checkout                 |             10 |
| End-to-End Purchase      |              6 |
| UI & Usability           |              6 |
| Session & Error Handling |              7 |
| **Total**                |         **96** |

The scenarios were designed to cover normal, negative, boundary, validation, usability, and end-to-end user flows.

---

# 8. Test Case Execution Summary

A total of **128 test cases** were executed in the simulated test cycle.

| Result       |   Count | Percentage |
| ------------ | ------: | ---------: |
| PASS         |     115 |     89.84% |
| FAIL         |      10 |      7.81% |
| BLOCKED      |       3 |      2.34% |
| Not Executed |       0 |         0% |
| **Total**    | **128** |   **100%** |

### Pass Rate Excluding Blocked Cases

There were 125 executable test cases after excluding blocked cases.

**Pass Rate = 115 / 125 × 100 = 92%**

### Failure Rate Excluding Blocked Cases

**Failure Rate = 10 / 125 × 100 = 8%**

### Blocked Rate

**Blocked Rate = 3 / 128 × 100 = 2.34%**

---

# 9. Module-Wise Execution Results

| Module                   |   Total |    PASS |   FAIL | BLOCKED |
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

# 10. Defect Summary

A total of **10 simulated defects** were identified during the initial execution cycle.

| Defect ID | Area                        | Severity | Priority | Status |
| --------- | --------------------------- | -------- | -------- | ------ |
| BUG-001   | Product Listing / Cart      | S2       | P1       | Open   |
| BUG-002   | Product Filtering           | S3       | P2       | Open   |
| BUG-003   | Shopping Cart               | S2       | P1       | Open   |
| BUG-004   | Authentication              | S2       | P1       | Open   |
| BUG-005   | Checkout                    | S1       | P1       | Open   |
| BUG-006   | Product Sorting             | S3       | P2       | Open   |
| BUG-007   | Shopping Cart               | S2       | P1       | Open   |
| BUG-008   | Checkout                    | S3       | P2       | Open   |
| BUG-009   | Product Details             | S2       | P1       | Open   |
| BUG-010   | Session / Application State | S2       | P1       | Open   |

> The defect statuses above represent the **initial defect-reporting stage**. The regression suite later represents the simulated post-fix verification state.

---

# 11. Defect Severity Distribution

| Severity      | Meaning                                   |  Count |
| ------------- | ----------------------------------------- | -----: |
| S1 — Critical | Blocks a critical business flow           |      1 |
| S2 — Major    | Significant functionality is affected     |      6 |
| S3 — Minor    | Limited functionality or usability impact |      3 |
| S4 — Trivial  | Cosmetic / negligible impact              |      0 |
| **Total**     |                                           | **10** |

### Severity Observation

The majority of simulated defects were classified as **S2 — Major**, indicating that the most significant issues were concentrated around important customer workflows such as:

* Cart behavior
* Authentication
* Checkout
* Product navigation
* Application state

One S1 defect was identified in the checkout flow.

---

# 12. Defect Priority Distribution

| Priority    |  Count |
| ----------- | -----: |
| P1 — High   |      7 |
| P2 — Medium |      3 |
| P3 — Low    |      0 |
| **Total**   | **10** |

The high number of P1 defects indicates that the initial simulated execution required corrective action before release consideration.

---

# 13. Critical Defect

### BUG-005 — Valid Checkout Cannot Be Completed Reliably

**Severity:** S1 — Critical
**Priority:** P1 — High

The simulated defect affected the core checkout workflow.

Because checkout is a critical business function for an e-commerce application, this defect was considered a release-blocking issue during the initial test cycle.

### Initial Release Impact

The presence of this defect contributed to the initial:

> **RELEASE ASSESSMENT: HOLD**

The issue was subsequently included in the regression suite through:

`REG-026 → TC-CHECKOUT-012`

The simulated regression result was:

> **PASS**

---

# 14. Blocker Summary

Three simulated blockers were recorded.

| Blocker ID | Related Test Case | Area                | Status  |
| ---------- | ----------------- | ------------------- | ------- |
| BLK-001    | TC-CART-018       | Shopping Cart       | Blocked |
| BLK-002    | TC-CHECKOUT-015   | Checkout            | Blocked |
| BLK-003    | TC-E2E-008        | End-to-End Purchase | Blocked |

### Blocker Impact

The blockers prevented complete execution of specific test cases because their prerequisite conditions could not be completed during the simulated execution cycle.

The blockers were treated separately from functional failures because the intended test behavior could not be evaluated.

---

# 15. Regression Testing Summary

Following the simulated defect-fix cycle, a focused regression suite containing **30 test cases** was executed.

| Result    |  Count |
| --------- | -----: |
| PASS      |     30 |
| FAIL      |      0 |
| BLOCKED   |      0 |
| **Total** | **30** |

### Regression Pass Rate

**30 / 30 × 100 = 100%**

### Regression Result

> **REGRESSION PASSED**

The regression suite covered the highest-risk areas affected by the previously identified defects.

---

# 16. Regression Coverage

The regression suite included coverage across:

* Navigation
* Product listing
* Search
* Filtering
* Product details
* Shopping cart
* Authentication
* Checkout
* End-to-end purchase flow

Important defect retests included:

| Defect  | Regression Test                       | Result |
| ------- | ------------------------------------- | ------ |
| BUG-001 | REG-003                               | PASS   |
| BUG-002 | REG-008                               | PASS   |
| BUG-003 | REG-014                               | PASS   |
| BUG-004 | REG-022                               | PASS   |
| BUG-005 | REG-026                               | PASS   |
| BUG-006 | REG-004                               | PASS   |
| BUG-007 | REG-018                               | PASS   |
| BUG-008 | REG-025                               | PASS   |
| BUG-009 | REG-012                               | PASS   |
| BUG-010 | Related session/navigation regression | PASS   |

All simulated regression checks passed.

---

# 17. Initial vs Post-Fix Assessment

| Metric             | Initial Execution | Simulated Post-Fix Regression |
| ------------------ | ----------------: | ----------------------------: |
| Test Cases         |               128 |                            30 |
| PASS               |               115 |                            30 |
| FAIL               |                10 |                             0 |
| BLOCKED            |                 3 |                             0 |
| Pass Rate          |              92%* |                          100% |
| Release Assessment |              HOLD |                CONDITIONAL GO |

`*` Initial pass rate is calculated excluding blocked cases.

---

# 18. Entry Criteria Assessment

| Entry Criterion                  | Status |
| -------------------------------- | ------ |
| Requirements available           | PASS   |
| Test scope defined               | PASS   |
| Test scenarios prepared          | PASS   |
| Test cases prepared              | PASS   |
| Test data prepared               | PASS   |
| Test environment defined         | PASS   |
| Defect reporting process defined | PASS   |

### Entry Criteria Result

> **ENTRY CRITERIA MET**

---

# 19. Exit Criteria Assessment

| Exit Criterion                          | Status |
| --------------------------------------- | ------ |
| All planned test cases executed         | PASS   |
| Requirement coverage completed          | PASS   |
| Defects documented                      | PASS   |
| Critical defects identified and tracked | PASS   |
| Regression suite executed               | PASS   |
| Regression defects verified             | PASS   |
| Blockers reviewed                       | PASS   |
| Final QA assessment prepared            | PASS   |

### Exit Criteria Result

> **EXIT CRITERIA CONDITIONALLY MET**

The exit criteria are considered conditionally met for this portfolio simulation because the focused regression suite passed, while final production release activities would still require stakeholder approval and complete environment validation.

---

# 20. Risk Assessment

## High-Risk Areas

### 1. Checkout

Checkout is the most business-critical workflow.

Risk:

* Failed purchase completion
* Incorrect validation
* Customer transaction interruption

Recommended action:

* Maintain checkout regression coverage for every release.

---

### 2. Shopping Cart

The cart is responsible for maintaining selected products and calculating order information.

Risk:

* Incorrect quantities
* Incorrect totals
* Product state inconsistencies

Recommended action:

* Include cart calculations and quantity management in every regression cycle.

---

### 3. Authentication

Authentication problems can prevent users from accessing expected application functionality.

Risk:

* Incorrect login behavior
* Session inconsistency
* Invalid credential handling

Recommended action:

* Maintain positive and negative authentication test cases.

---

### 4. Application State

State-related problems may affect multiple modules.

Risk:

* Incorrect navigation state
* Stale information
* Unexpected cart/session behavior

Recommended action:

* Include state transition testing in regression testing.

---

# 21. QA Observations

The testing exercise highlighted several important QA observations.

### Observation 1 — Core workflows require priority-based testing

Not all test cases have equal business impact.

Checkout, authentication, cart, and purchase flows should receive higher priority than cosmetic or low-impact scenarios.

---

### Observation 2 — Requirement traceability improves coverage confidence

Mapping requirements to scenarios and test cases makes it easier to identify missing coverage.

The project achieved:

> **17/17 requirements covered — 100% requirement-level coverage**

---

### Observation 3 — Regression testing is essential after defect fixes

Fixing one feature can affect another feature.

The regression suite therefore included related functionality instead of testing only the exact defect steps.

---

### Observation 4 — Blocked tests should not automatically be counted as failures

A blocked test means the expected execution could not be completed.

Separating:

* PASS
* FAIL
* BLOCKED

provides more accurate QA reporting.

---

### Observation 5 — Defect severity and priority are different

Severity describes the **impact of the defect**.

Priority describes **how urgently the defect should be fixed**.

Using both fields helps development and QA teams communicate release risk more effectively.

---

# 22. Key QA Metrics

| Metric                       | Result |
| ---------------------------- | -----: |
| Requirements                 |     17 |
| Requirement Coverage         |   100% |
| Test Scenarios               |     96 |
| Test Cases                   |    128 |
| Initial PASS                 |    115 |
| Initial FAIL                 |     10 |
| Initial BLOCKED              |      3 |
| Initial Executable Pass Rate |    92% |
| Initial Failure Rate         |     8% |
| Simulated Defects            |     10 |
| S1 Defects                   |      1 |
| S2 Defects                   |      6 |
| S3 Defects                   |      3 |
| P1 Defects                   |      7 |
| P2 Defects                   |      3 |
| Regression Cases             |     30 |
| Regression PASS              |     30 |
| Regression Pass Rate         |   100% |

---

# 23. Release Recommendation

## Initial Assessment

Based on the initial simulated execution:

> **RELEASE STATUS: HOLD**

The presence of one S1 defect, multiple S2 defects, and three blocked test cases represented significant release risk.

---

## Post-Regression Assessment

After simulated defect resolution and execution of the focused regression suite:

> **REGRESSION STATUS: PASS**

> **FINAL SIMULATED RECOMMENDATION: CONDITIONALLY READY FOR RELEASE**

The recommendation is conditional because the following activities would still be required in a real QA environment:

1. Complete retesting of all resolved defects.
2. Verify the three previously blocked workflows.
3. Execute the complete test suite after fixes.
4. Perform cross-browser validation.
5. Validate the application in the intended release environment.
6. Obtain final QA and stakeholder approval.
7. Confirm no new critical or high-priority defects remain open.

---

# 24. QA Sign-Off

### QA Assessment

**Overall Test Result:** CONDITIONALLY PASS

**Initial Execution:** HOLD

**Regression Execution:** PASS

**Final Recommendation:** CONDITIONAL GO / READY PENDING FINAL SIGN-OFF

### Approval

| Role             | Name               | Status           | Date       |
| ---------------- | ------------------ | ---------------- | ---------- |
| QA Tester        | __________________ | Pending Approval | __________ |
| QA Lead          | __________________ | Pending Approval | __________ |
| Product Owner    | __________________ | Pending Approval | __________ |
| Development Lead | __________________ | Pending Approval | __________ |

---

# 25. Project Deliverables

The complete manual QA project contains the following deliverables:

```text
BStackDemo-Manual-QA/
│
├── README.md
├── PROJECT_GUIDE.md
│
├── 01-Requirements/
│   └── Requirements.md
│
├── 02-Test-Plan/
│   └── Test_Plan.md
│
├── 03-Test-Scenarios/
│   └── Test_Scenarios.md
│
├── 04-Test-Cases/
│   └── Test_Cases.md
│
├── 05-Test-Data/
│   └── Test_Data.md
│
├── 06-Test-Execution/
│   └── Test_Execution.md
│
├── 07-Bug-Reports/
│   └── Bug_Reports.md
│
├── 08-RTM/
│   └── RTM.md
│
├── 09-Regression/
│   └── Regression_Suite.md
│
├── 10-Test-Summary/
│   └── Test_Summary_Report.md
│
└── BStackDemo_Manual_QA_Testing.xlsx
```

---

# 26. QA Lifecycle Demonstrated

This project demonstrates the following end-to-end manual QA workflow:

```text
Requirements
     ↓
Test Planning
     ↓
Test Scenarios
     ↓
Test Cases
     ↓
Test Data
     ↓
Test Execution
     ↓
Defect Identification
     ↓
Bug Reporting
     ↓
Requirement Traceability
     ↓
Defect Fix / Retest
     ↓
Regression Testing
     ↓
Test Summary Report
     ↓
Release Recommendation
```

---

# 27. Final Conclusion

The BStackDemo Manual QA project demonstrates a complete, structured manual testing lifecycle for an e-commerce web application.

The project includes:

* **17 documented requirements**
* **96 test scenarios**
* **128 test cases**
* **Complete test data**
* **Simulated execution results**
* **10 simulated defect reports**
* **Requirement Traceability Matrix**
* **30-case regression suite**
* **Final test summary report**

During the initial simulated execution, **115 of 128 test cases passed**, while **10 failed** and **3 were blocked**.

The identified issues included defects in:

* Product listing
* Product filtering
* Product details
* Shopping cart
* Authentication
* Checkout
* Application state

A focused **30-test-case regression suite** was subsequently executed with:

> **30 PASS / 30 — 100% Regression Pass Rate**

The final simulated assessment is therefore:

> **CONDITIONALLY READY FOR RELEASE — PENDING FINAL QA SIGN-OFF**

For a real production release, the results in this portfolio project would need to be replaced with actual execution evidence from the target environment, along with verified defect retest results and stakeholder approval.

---

## 28. Portfolio Disclaimer

This repository is a **personal QA portfolio project** created to demonstrate practical knowledge of:

* Manual testing
* Test planning
* Test scenario design
* Test case design
* Test data preparation
* Test execution
* Defect reporting
* Requirement traceability
* Regression testing
* QA reporting


