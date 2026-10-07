# BStackDemo — Manual QA Testing Project

A complete **end-to-end Manual QA Testing project** for the BStackDemo e-commerce web application.

This project demonstrates the complete Software Testing Life Cycle (STLC), from requirement analysis and test planning to test execution, defect reporting, regression testing, requirement traceability, and final test reporting.



---

##  Project Overview

| Item                  | Details                                         |
| --------------------- | ----------------------------------------------- |
| Application           | BStackDemo                                      |
| Application Type      | E-commerce Web Application                      |
| Testing Type          | Manual Testing                                  |
| Testing Level         | System Testing / End-to-End Testing             |
| Primary Browser       | Google Chrome / Chromium                        |
| Operating System      | Windows                                         |
| Requirements          | 17                                              |
| Test Scenarios        | 96                                              |
| Test Cases            | 128                                             |
| Simulated Defects     | 10                                              |
| Regression Test Cases | 30                                              |
| Regression Result     | 30/30 PASS                                      |
| Initial Pass Rate     | 92%*                                            |
| Final Recommendation  | Conditionally Ready / Pending Final QA Sign-off |

* Pass rate is calculated excluding blocked test cases.

---

#  Project Objective

The objective of this project is to demonstrate practical manual QA skills by testing the major user-facing workflows of an e-commerce application.

The project focuses on:

* Requirement analysis
* Test planning
* Test scenario design
* Test case design
* Test data preparation
* Functional testing
* Negative testing
* Boundary testing
* UI and usability testing
* Defect reporting
* Requirement traceability
* Regression testing
* End-to-end testing
* Test summary reporting

---

#  Testing Scope

## Functional Testing

The following application areas were covered:

* Homepage & Navigation
* Product Listing
* Product Search
* Product Filtering
* Product Sorting
* Product Details
* Shopping Cart
* User Authentication
* Checkout
* End-to-End Purchase Flow
* UI & Usability
* Session & Error Handling

## Non-Functional Testing

Basic coverage was included for:

* Usability
* Browser compatibility
* Responsiveness
* Reliability
* Data integrity

---

#  Out of Scope

This project intentionally focuses on **Manual QA Testing**.

The following are not included:

* API Testing
* Postman
* Selenium
* Playwright
* Cypress
* Automation Testing
* Database Testing
* Performance Testing
* Load Testing
* Security Penetration Testing
* Backend Code Testing
* Unit Testing
* Infrastructure Testing

These areas can be added as separate projects or future extensions.

---

#  Project Metrics

## Requirements

**17 total requirements**

* 12 Functional Requirements
* 5 Non-Functional Requirements

### Requirement Coverage

**17 / 17 = 100%**

---

## Test Scenarios

**96 total test scenarios**

| Module                   | Scenarios |
| ------------------------ | --------: |
| Homepage & Navigation    |        10 |
| Product Listing          |        10 |
| Product Search           |        10 |
| Product Filtering        |        10 |
| Product Sorting          |         6 |
| Product Details          |         5 |
| Shopping Cart            |         9 |
| Authentication           |         7 |
| Checkout                 |        10 |
| End-to-End Purchase      |         6 |
| UI & Usability           |         6 |
| Session & Error Handling |         7 |
| **Total**                |    **96** |

---

## Test Cases

**128 total test cases**

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

#  Test Execution Results

A simulated execution cycle was performed across all 128 test cases.

| Result    |   Count |
| --------- | ------: |
| PASS    |     115 |
| FAIL    |      10 |
| BLOCKED |       3 |
| **Total** | **128** |

### Pass Rate

Excluding blocked test cases:

```text
Executable Test Cases = 128 - 3
                      = 125

Pass Rate = 115 / 125 × 100
          = 92%
```

### Failure Rate

```text
Failure Rate = 10 / 125 × 100
             = 8%
```

### Blocked Rate

```text
Blocked Rate = 3 / 128 × 100
             = 2.34%
```

---

#  Defect Summary

A total of **10 simulated defects** were identified during the initial execution cycle.

| Defect ID | Area                        | Severity | Priority |
| --------- | --------------------------- | -------- | -------- |
| BUG-001   | Product Listing / Cart      | S2       | P1       |
| BUG-002   | Product Filtering           | S3       | P2       |
| BUG-003   | Shopping Cart               | S2       | P1       |
| BUG-004   | Authentication              | S2       | P1       |
| BUG-005   | Checkout                    | S1       | P1       |
| BUG-006   | Product Sorting             | S3       | P2       |
| BUG-007   | Shopping Cart               | S2       | P1       |
| BUG-008   | Checkout                    | S3       | P2       |
| BUG-009   | Product Details             | S2       | P1       |
| BUG-010   | Session / Application State | S2       | P1       |

### Severity Distribution

| Severity      |  Count |
| ------------- | -----: |
| S1 — Critical |      1 |
| S2 — Major    |      6 |
| S3 — Minor    |      3 |
| S4 — Trivial  |      0 |
| **Total**     | **10** |

### Priority Distribution

| Priority    |  Count |
| ----------- | -----: |
| P1 — High   |      7 |
| P2 — Medium |      3 |
| P3 — Low    |      0 |
| **Total**   | **10** |

---

#  Blockers

Three simulated blockers were recorded during the initial execution.

| Blocker | Test Case       | Area                |
| ------- | --------------- | ------------------- |
| BLK-001 | TC-CART-018     | Shopping Cart       |
| BLK-002 | TC-CHECKOUT-015 | Checkout            |
| BLK-003 | TC-E2E-008      | End-to-End Purchase |

Blocked cases were tracked separately from failed cases because the intended test execution could not be completed.

---

# 🔄 Regression Testing

After the simulated defect-fix cycle, a focused regression suite was executed.

### Regression Results

| Result    |  Count |
| --------- | -----: |
|  PASS    |     30 |
|  FAIL    |      0 |
|  BLOCKED |      0 |
| **Total** | **30** |

### Regression Pass Rate

```text
30 / 30 × 100 = 100%
```

### Regression Status

> ** REGRESSION PASSED**

The regression suite focused on high-risk and previously affected areas including:

* Product listing
* Search
* Filtering
* Product details
* Shopping cart
* Authentication
* Checkout
* End-to-end purchase flow
* Application navigation/state

---

#  QA Lifecycle

The project follows a complete manual QA workflow:

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
Defect Retesting
     ↓
Regression Testing
     ↓
Test Summary
     ↓
Release Recommendation
```

---

#  Repository Structure

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

#  Deliverables

## 01 — Requirements

Contains:

* Functional requirements
* Non-functional requirements
* Acceptance criteria
* Requirement IDs
* Requirement coverage

---

## 02 — Test Plan

Contains:

* Testing objectives
* Scope
* Testing approach
* Test environment
* Test types
* Test data strategy
* Entry criteria
* Exit criteria
* Defect lifecycle
* Regression strategy
* Risks

---

## 03 — Test Scenarios

Contains **96 test scenarios** covering the application's major workflows.

---

## 04 — Test Cases

Contains **128 detailed manual test cases** with structured test information.

Test cases cover:

* Positive testing
* Negative testing
* Boundary testing
* Validation
* Navigation
* Business workflows
* UI behavior
* Session/state behavior

---

## 05 — Test Data

Contains test data for:

* Products
* Search
* Filters
* Sorting
* Authentication
* Cart
* Checkout
* Boundary conditions
* Special characters
* Whitespace
* End-to-end flows

---

## 06 — Test Execution

Contains:

* Execution results
* Module-wise results
* PASS/FAIL/BLOCKED status
* Defect references
* Blocker references
* Execution metrics
* Release assessment

---

## 07 — Bug Reports

Contains **10 simulated defect reports** with:

* Defect ID
* Title
* Preconditions
* Steps to reproduce
* Expected result
* Actual result
* Severity
* Priority
* Impact
* Recommendation
* Retest criteria

---

## 08 — RTM

The Requirement Traceability Matrix connects:

```text
Requirement
     ↓
Test Scenario
     ↓
Test Case
     ↓
Execution Result
     ↓
Defect
```

Requirement coverage:

> **100% — 17/17 requirements mapped**

---

## 09 — Regression

Contains a **30-test-case regression suite**.

Result:

> **30/30 PASS — 100%**

---

## 10 — Test Summary

Contains the final QA assessment including:

* Test execution summary
* Defect summary
* Blocker summary
* Regression results
* Risk assessment
* QA metrics
* Release recommendation
* QA sign-off section

---

#  Testing Techniques Used

The project demonstrates several practical manual testing techniques.

### Equivalence Partitioning

Inputs are divided into valid and invalid groups to reduce unnecessary test combinations.

### Boundary Value Analysis

Values around valid boundaries are tested to identify edge-case failures.

### Positive Testing

Verifies that valid user actions produce the expected result.

### Negative Testing

Verifies that invalid input and unexpected actions are handled correctly.

### Scenario-Based Testing

Tests realistic user workflows instead of isolated UI elements only.

### End-to-End Testing

Validates complete business workflows from product selection through checkout.

### Regression Testing

Verifies that fixes do not introduce problems in previously working functionality.

### Exploratory Thinking

Testers consider unexpected user behavior and potential failure points beyond scripted steps.

---

#  Severity vs Priority

This project distinguishes between **severity** and **priority**.

### Severity

Describes the impact of the defect.

```text
S1 → Critical
S2 → Major
S3 → Minor
S4 → Trivial
```

### Priority

Describes how urgently the defect should be addressed.

```text
P1 → High
P2 → Medium
P3 → Low
```

Example:

> A checkout failure can be **S1 Critical / P1 High** because it can prevent a core business transaction.

---

#  Release Assessment

## Initial Execution

The initial simulated execution resulted in:

```text
115 PASS
10 FAIL
3 BLOCKED
```

Because critical/major issues were identified, the initial release assessment was:

> ** HOLD**

---

## Post-Fix Regression

The simulated regression cycle resulted in:

```text
30 PASS
0 FAIL
0 BLOCKED
```

Regression status:

> ** PASS**

---

## Final Simulated Recommendation

> ** CONDITIONALLY READY FOR RELEASE**

This recommendation assumes that:

* Identified defects have been fixed.
* Defect retesting has passed.
* Blocked workflows have been verified.
* Required regression testing has passed.
* Final QA and stakeholder approval are obtained.

This is **not an actual production release approval**.

---

#  Portfolio Disclaimer

This project is a personal QA portfolio project created to demonstrate practical knowledge of:

* Manual Testing
* Software Testing Life Cycle
* Test Planning
* Test Scenario Design
* Test Case Design
* Test Data Preparation
* Test Execution
* Defect Reporting
* Requirement Traceability
* Regression Testing
* End-to-End Testing
* QA Reporting

The following project data is **simulated**:

* Test execution results
* Failed test cases
* Defects
* Blockers
* Defect fixes
* Regression results
* Release recommendation

These results should **not** be represented as actual production testing performed for the BStackDemo application.

---

#  Skills Demonstrated

This project demonstrates practical QA skills including:

```text
Manual Testing
Functional Testing
Non-Functional Testing
Test Case Design
Test Scenario Design
Test Planning
Test Data Design
Negative Testing
Boundary Testing
End-to-End Testing
Regression Testing
Defect Reporting
Severity & Priority Classification
Requirement Traceability
Risk Analysis
QA Documentation
Test Reporting
```

---

#  Project Highlights

### 17 Requirements

Complete functional and non-functional requirement coverage.

### 96 Test Scenarios

Scenario-level coverage across the application's major workflows.

### 128 Test Cases

Detailed manual test coverage including positive, negative, boundary, validation, and workflow testing.

### 10 Simulated Defects

Defects documented using a structured QA defect-reporting format.

### 30 Regression Tests

Focused regression suite covering high-risk areas.

### 100% Regression Pass

All 30 simulated regression cases passed.

### Complete QA Documentation

The repository demonstrates the complete manual QA lifecycle from requirements through final test reporting.

---

#  Final Project Status

```text
Project Type       : Manual QA Testing
Requirements       : 17
Scenarios          : 96
Test Cases         : 128
Initial PASS       : 115
Initial FAIL       : 10
Initial BLOCKED    : 3
Simulated Defects  : 10
Regression Cases   : 30
Regression PASS    : 30
Regression Rate    : 100%
Final Assessment   : Conditionally Ready
Data Status        : Simulated Portfolio Data
```

---

## Conclusion

The BStackDemo Manual QA project demonstrates an end-to-end approach to software quality assurance.

It shows how a QA tester can move from:

**Requirements → Planning → Scenarios → Test Cases → Execution → Defects → RTM → Regression → Test Summary → Release Recommendation**

while maintaining traceability and structured documentation throughout the testing lifecycle.
