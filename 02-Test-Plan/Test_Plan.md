# BStackDemo Manual QA Testing — Test Plan

## 1. Document Information

| Field           | Details                      |
| --------------- | ---------------------------- |
| Project         | BStackDemo Manual QA Testing |
| Application     | BStackDemo                   |
| Application URL | https://bstackdemo.com/      |
| Document        | Test Plan                    |
| Testing Type    | Manual Testing               |
| Version         | 1.0                          |
| Status          | Baseline                     |

---

# 2. Test Plan Objective

The objective of this test plan is to define the testing approach, scope, resources, environment, testing techniques, entry criteria, exit criteria, risks and deliverables for the BStackDemo manual testing project.

The goal is to systematically validate the application's major e-commerce workflows and identify functional, usability, validation and integration issues.

---

# 3. Application Under Test

**BStackDemo** is a web-based e-commerce demonstration application used for practicing web application testing.

The testing will focus on the customer shopping journey:

```text
Homepage
   ↓
Browse Products
   ↓
Search / Filter / Sort
   ↓
Product Details
   ↓
Add to Cart
   ↓
Cart
   ↓
Login
   ↓
Checkout
   ↓
Order Completion
```

---

# 4. Testing Scope

## 4.1 In Scope

The following areas will be manually tested:

### A. Homepage & Navigation

* Homepage loading
* Application branding
* Navigation controls
* Product navigation
* Cart navigation
* Login navigation
* Browser navigation

### B. Product Listing

* Product visibility
* Product names
* Product images
* Product prices
* Product cards
* Add-to-cart controls
* Product consistency

### C. Product Search

* Valid searches
* Invalid searches
* Partial searches
* Case variations
* Whitespace
* Empty searches
* Special characters
* No-result searches

### D. Product Filters

* Available filters
* Individual filters
* Multiple filters
* Removing filters
* Filter combinations
* No-result combinations
* Filter and sorting interaction

### E. Product Sorting

* Default ordering
* Price ascending
* Price descending
* Sorting after filtering
* Changing sorting options
* Product preservation

### F. Product Details

* Product navigation
* Product name
* Product image
* Product price
* Product information
* Availability
* Add-to-cart functionality

### G. Shopping Cart

* Add product
* Multiple products
* Quantity
* Remove product
* Cart count
* Cart total
* Empty cart
* Cart persistence
* Checkout transition

### H. Authentication

* Login
* Valid credentials
* Invalid credentials
* Empty fields
* Validation
* Authentication state
* Logout

### I. Checkout

* Cart-to-checkout transition
* Product information
* Quantity
* Price
* Customer information
* Required fields
* Invalid input
* Order confirmation

### J. End-to-End Purchase

* Product discovery
* Product selection
* Cart
* Authentication
* Checkout
* Order completion

### K. UI & Usability

* Layout
* Labels
* Buttons
* Messages
* Navigation
* Consistency
* Responsive behavior

### L. Session & Error Handling

* Logout behavior
* Refresh
* Browser navigation
* Invalid actions
* Empty states
* Invalid input
* Unexpected conditions

---

# 5. Testing Types

The following testing types will be used.

## 5.1 Functional Testing

Verifies that application functionality behaves according to the defined requirements.

---

## 5.2 Positive Testing

Uses valid input and expected user workflows.

Example:

```text
Valid product
      ↓
Add to Cart
      ↓
Product appears in Cart
```

---

## 5.3 Negative Testing

Uses invalid or unexpected input to verify that the application handles it correctly.

Example:

```text
Invalid checkout data
      ↓
Validation
      ↓
Order should NOT be completed
```

---

## 5.4 Boundary Value Analysis

Tests values at and around important boundaries.

Examples include:

* Quantity
* Input length
* Empty values
* Minimum/maximum values where applicable

---

## 5.5 Equivalence Partitioning

Divides input values into valid and invalid classes.

Example:

```text
Valid Input
Invalid Input
Empty Input
Special Character Input
```

---

## 5.6 Exploratory Testing

Tester-driven exploration will be performed to identify unexpected application behavior outside predefined test cases.

---

## 5.7 Regression Testing

Previously tested functionality will be re-tested after defect fixes or application changes.

---

## 5.8 End-to-End Testing

Complete business workflows will be validated across multiple modules.

---

## 5.9 Session Testing

Authentication, logout, navigation and session-state behavior will be validated.

---

## 5.10 UI Testing

Visual layout, controls, labels, buttons and consistency will be checked manually.

---

## 5.11 Usability Testing

The application will be evaluated from a user's perspective for clarity, navigation and ease of use.

---

## 5.12 Compatibility Testing

The application may be checked across supported browsers and viewport sizes.

Primary browser:

**Google Chrome / Chromium**

---

# 6. Test Environment

| Component        | Configuration            |
| ---------------- | ------------------------ |
| Application      | BStackDemo               |
| Application Type | Web Application          |
| Testing          | Manual                   |
| Primary Browser  | Google Chrome / Chromium |
| Operating System | Windows                  |
| Test Data        | Dedicated QA test data   |
| Documentation    | Markdown                 |
| Test Management  | Markdown / Excel         |
| Version Control  | Git / GitHub             |

---

# 7. Test Data Strategy

Test data will include:

### Product Data

* Valid products
* Multiple products
* Product search keywords
* Partial keywords
* Invalid keywords

### Search Data

* Exact product names
* Partial names
* Uppercase/lowercase variations
* Empty search
* Whitespace
* Special characters
* Non-existing product names

### Cart Data

* Single product
* Multiple products
* Different quantities
* Product removal
* Empty cart

### Authentication Data

* Valid credentials
* Invalid credentials
* Incorrect password
* Empty username
* Empty password

### Checkout Data

* Valid customer details
* Missing required fields
* Invalid input
* Boundary input
* Special characters where applicable

---

# 8. Test Case Design Strategy

Each test case will contain:

| Field           | Description                          |
| --------------- | ------------------------------------ |
| Test Case ID    | Unique identifier                    |
| Requirement ID  | Related requirement                  |
| Scenario ID     | Related test scenario                |
| Module          | Application module                   |
| Test Objective  | What is being validated              |
| Preconditions   | Conditions required before execution |
| Test Data       | Data required                        |
| Test Steps      | Detailed execution steps             |
| Expected Result | Expected application behavior        |
| Actual Result   | Observed behavior                    |
| Status          | PASS / FAIL / BLOCKED / NOT EXECUTED |
| Severity        | Impact of failure                    |
| Priority        | Fix priority                         |
| Defect ID       | Related defect                       |
| Remarks         | Additional information               |

---

# 9. Test Case Distribution

The project will contain **128 detailed manual test cases**.

| Module                   | Planned Cases |
| ------------------------ | ------------: |
| Homepage & Navigation    |            10 |
| Product Listing          |            12 |
| Product Search           |            10 |
| Product Filtering        |            12 |
| Product Sorting          |             8 |
| Product Details          |            10 |
| Shopping Cart            |            18 |
| Authentication           |            10 |
| Checkout                 |            15 |
| End-to-End Purchase      |             8 |
| UI & Usability           |             8 |
| Session & Error Handling |             7 |
| **Total**                |       **128** |

---

# 10. Severity Classification

## Critical

A defect that prevents a major business workflow or creates severe data/security risk.

Example:

* User cannot complete purchase.
* Incorrect order completion.
* Major transaction/data integrity issue.

---

## High

A major feature is not functioning correctly but the application remains partially usable.

Example:

* Checkout cannot proceed.
* Cart total is incorrect.
* Valid login cannot proceed.

---

## Medium

A feature works incorrectly but has a workaround or limited business impact.

Example:

* Incorrect validation message.
* Filter behaves incorrectly in a specific condition.

---

## Low

Minor visual, wording or usability issue.

Example:

* Minor alignment issue.
* Typographical error.

---

# 11. Priority Classification

### P1 — Immediate

Critical functionality or business flow affected.

### P2 — High

Important functionality affected and should be fixed before release.

### P3 — Medium

Should be fixed but does not block the main workflow.

### P4 — Low

Minor improvement or cosmetic issue.

---

# 12. Entry Criteria

Testing may begin when:

* Application is accessible.
* Major application pages are available.
* Requirements baseline is available.
* Test scenarios are prepared.
* Test cases are reviewed.
* Test data is prepared.
* Test environment is available.
* Required credentials are available where applicable.

---

# 13. Exit Criteria

Testing may be considered complete when:

* All planned test cases have been executed.
* All critical and high-priority defects are resolved or formally accepted.
* Failed test cases have been retested.
* Blocked test cases have been executed where possible.
* Regression testing is completed.
* No unresolved critical defects remain for release.
* Test summary has been prepared.
* Release recommendation has been documented.

---

# 14. Defect Lifecycle

Defects will follow the following lifecycle:

```text
New
 ↓
Assigned
 ↓
Open
 ↓
Fixed
 ↓
Ready for Retest
 ↓
Retest
 ↓
 ┌───────────────┐
 │               │
PASS            FAIL
 │               │
Closed       Reopened
                 │
                 └──→ Fixed → Retest
```

---

# 15. Defect Reporting

Each defect should contain:

* Defect ID
* Summary
* Module
* Requirement ID
* Test Case ID
* Severity
* Priority
* Environment
* Preconditions
* Steps to Reproduce
* Test Data
* Expected Result
* Actual Result
* Evidence
* Status
* Assignee
* Retest Result
* Remarks

---

# 16. Regression Strategy

Regression testing will focus on functionality affected by defects or application changes.

### Regression Priority

```text
Authentication
      ↓
Cart
      ↓
Checkout
      ↓
Order Flow
      ↓
Product Listing
      ↓
Search / Filter / Sort
      ↓
UI / Navigation
```

A dedicated regression suite will be created in:

```text
09-Regression/Regression_Suite.md
```

---

# 17. End-to-End Test Strategy

The primary end-to-end business flow will validate:

```text
Open BStackDemo
      ↓
Browse/Search Product
      ↓
Select Product
      ↓
Add Product to Cart
      ↓
Open Cart
      ↓
Proceed to Checkout
      ↓
Login
      ↓
Enter Customer Information
      ↓
Submit Order
      ↓
Verify Order Confirmation
```

Additional variations will cover:

* Different products
* Multiple products
* Different quantities
* Invalid checkout information
* Cart modifications
* Authentication variations

---

# 18. Risks

| Risk                            | Impact | Mitigation                          |
| ------------------------------- | ------ | ----------------------------------- |
| Application unavailable         | High   | Retry testing / document blocker    |
| Test environment changes        | Medium | Record environment details          |
| Dynamic product data            | Medium | Capture data before execution       |
| Login issues                    | High   | Verify credentials before execution |
| Unexpected application behavior | Medium | Create defect with evidence         |
| Browser-specific behavior       | Medium | Perform compatibility checks        |
| Test data changes               | Medium | Maintain dedicated test data        |

---

# 19. Assumptions

* BStackDemo remains accessible during testing.
* The application provides the required functionality described in the requirements baseline.
* Test data can be created or reused where supported.
* Manual testing is sufficient for the scope of this portfolio project.
* Actual observed results will be recorded during execution.
* Simulated execution data, if used for portfolio demonstration, will be clearly labeled as simulated.

---

# 20. Deliverables

The project will produce:

```text
01-Requirements/
    Requirements.md

02-Test-Plan/
    Test_Plan.md

03-Test-Scenarios/
    Test_Scenarios.md

04-Test-Cases/
    Test_Cases.md

05-Test-Data/
    Test_Data.md

06-Test-Execution/
    Test_Execution.md

07-Bug-Reports/
    Bug_Reports.md

08-RTM/
    RTM.md

09-Regression/
    Regression_Suite.md

10-Test-Summary/
    Test_Summary_Report.md

ParaBank_Manual_QA_Testing.xlsx
```

> The final workbook will be named `BStackDemo_Manual_QA_Testing.xlsx`.

---

# 21. Roles and Responsibilities

For this portfolio project, the tester is responsible for:

* Requirement analysis
* Test planning
* Test scenario creation
* Test case creation
* Test data preparation
* Manual execution
* Defect identification
* Defect documentation
* Retesting
* Regression testing
* RTM maintenance
* Test summary preparation

---

# 22. Testing Workflow

The complete workflow is:

```text
1. Analyze Requirements
        ↓
2. Prepare Test Plan
        ↓
3. Create Test Scenarios
        ↓
4. Create 128 Test Cases
        ↓
5. Prepare Test Data
        ↓
6. Execute Tests
        ↓
7. Report Defects
        ↓
8. Retest Fixes
        ↓
9. Execute Regression Suite
        ↓
10. Update RTM
        ↓
11. Prepare Test Summary
        ↓
12. Release Recommendation
```

---

# 23. Project Success Criteria

The project will be considered successful when:

* All 12 requirements have test coverage.
* 128 test cases are documented.
* Test cases contain positive and negative coverage.
* Appropriate boundary and equivalence testing is included.
* Test data is documented.
* Execution results are recorded.
* Defects are traceable to failed test cases.
* Regression cases are identified.
* RTM provides requirement-to-test traceability.
* Final test summary reflects the actual recorded results.
* No execution results are falsely represented as live findings.

---

# 24. Document Control

| Version | Date       | Description                |
| ------- | ---------- | -------------------------- |
| 1.0     | 2026-10-07 | Initial test plan baseline |

---

**End of Test Plan**
