# BStackDemo Manual QA Testing — Test Scenarios

## 1. Document Information

| Field                | Details                      |
| -------------------- | ---------------------------- |
| Project              | BStackDemo Manual QA Testing |
| Application          | BStackDemo                   |
| Document             | Test Scenarios               |
| Testing Type         | Manual Testing               |
| Version              | 1.0                          |
| Total Test Scenarios | 60                           |
| Status               | Baseline                     |

---

# 2. Purpose

This document defines the high-level test scenarios for validating the BStackDemo e-commerce web application.

These scenarios are derived from the requirements defined in:

`01-Requirements/Requirements.md`

Each detailed test case in:

`04-Test-Cases/Test_Cases.md`

will be mapped to one or more scenarios from this document.

---

# 3. Scenario Identification

Test scenario IDs follow this format:

```text
TS-XXX
```

Example:

```text
TS-001
TS-002
TS-003
```

---

# 4. Homepage & Navigation Scenarios

## TS-001 — Verify BStackDemo homepage loads successfully

**Requirement:** FR-001

Verify that the application homepage loads without errors and displays the expected main shopping interface.

---

## TS-002 — Verify application branding and main UI elements

**Requirement:** FR-001

Verify that the application branding and primary UI elements are displayed correctly.

---

## TS-003 — Verify navigation to product catalog

**Requirement:** FR-001

Verify that users can navigate to the product catalog from the homepage.

---

## TS-004 — Verify navigation to shopping cart

**Requirement:** FR-001

Verify that the shopping cart can be opened from the main navigation.

---

## TS-005 — Verify navigation to login

**Requirement:** FR-001

Verify that users can access the login functionality from the application.

---

## TS-006 — Verify browser Back navigation

**Requirement:** FR-001, FR-012

Verify that browser Back navigation behaves correctly during normal shopping activity.

---

## TS-007 — Verify browser Forward navigation

**Requirement:** FR-001, FR-012

Verify that browser Forward navigation behaves correctly.

---

## TS-008 — Verify navigation links do not lead to unexpected errors

**Requirement:** FR-001

Verify that important navigation links lead to the correct pages.

---

## TS-009 — Verify page refresh behavior

**Requirement:** FR-001, FR-012

Verify that refreshing pages does not unexpectedly corrupt the application state.

---

## TS-010 — Verify navigation consistency across the application

**Requirement:** FR-001, FR-011

Verify that navigation controls remain consistent across major application pages.

---

# 5. Product Listing Scenarios

## TS-011 — Verify products are displayed

**Requirement:** FR-002

Verify that available products are displayed correctly in the product catalog.

---

## TS-012 — Verify product images

**Requirement:** FR-002

Verify that product images load correctly.

---

## TS-013 — Verify product names

**Requirement:** FR-002

Verify that product names are displayed correctly.

---

## TS-014 — Verify product prices

**Requirement:** FR-002

Verify that product prices are displayed correctly.

---

## TS-015 — Verify product card layout

**Requirement:** FR-002, FR-011

Verify that product cards maintain a consistent layout.

---

## TS-016 — Verify Add to Cart controls

**Requirement:** FR-002, FR-007

Verify that available products provide the expected Add to Cart functionality.

---

## TS-017 — Verify product information consistency

**Requirement:** FR-002, FR-006

Verify that product information shown in the listing matches the corresponding product details.

---

## TS-018 — Verify product list after navigation

**Requirement:** FR-002

Verify that the product listing remains correct after navigating away and returning.

---

## TS-019 — Verify product list after applying filters

**Requirement:** FR-002, FR-004

Verify that products displayed after filtering are correct.

---

## TS-020 — Verify product list after sorting

**Requirement:** FR-002, FR-005

Verify that products remain correct after sorting.

---

# 6. Product Search Scenarios

## TS-021 — Verify search using an exact product name

**Requirement:** FR-003

Verify that searching for an exact product name returns the appropriate product.

---

## TS-022 — Verify search using a partial product name

**Requirement:** FR-003

Verify that partial search terms behave correctly where supported.

---

## TS-023 — Verify search with uppercase characters

**Requirement:** FR-003

Verify search behavior when uppercase characters are used.

---

## TS-024 — Verify search with lowercase characters

**Requirement:** FR-003

Verify search behavior when lowercase characters are used.

---

## TS-025 — Verify search with leading and trailing spaces

**Requirement:** FR-003

Verify that unnecessary spaces are handled appropriately.

---

## TS-026 — Verify search with no matching product

**Requirement:** FR-003

Verify that an appropriate no-results state is displayed when no product matches the search.

---

## TS-027 — Verify empty search input

**Requirement:** FR-003

Verify application behavior when the search field is empty.

---

## TS-028 — Verify search using special characters

**Requirement:** FR-003

Verify that special characters do not cause unexpected application behavior.

---

## TS-029 — Verify changing search criteria

**Requirement:** FR-003

Verify that search results update correctly when the search keyword is changed.

---

## TS-030 — Verify clearing the search

**Requirement:** FR-003

Verify that clearing search criteria restores the appropriate product listing.

---

# 7. Product Filter Scenarios

## TS-031 — Verify available filter options

**Requirement:** FR-004

Verify that available product filter options are displayed correctly.

---

## TS-032 — Verify applying a single filter

**Requirement:** FR-004

Verify that selecting a single filter displays the appropriate products.

---

## TS-033 — Verify removing an applied filter

**Requirement:** FR-004

Verify that removing a filter restores the appropriate product results.

---

## TS-034 — Verify multiple filter selection

**Requirement:** FR-004

Verify behavior when multiple filters are selected where supported.

---

## TS-035 — Verify filter combination results

**Requirement:** FR-004

Verify that products displayed after combining filters satisfy the selected criteria.

---

## TS-036 — Verify filter with no matching products

**Requirement:** FR-004

Verify that the application handles a filter combination producing no results.

---

## TS-037 — Verify filter state during navigation

**Requirement:** FR-004, FR-012

Verify that filter state behaves appropriately while navigating through the application.

---

## TS-038 — Verify filter and sorting interaction

**Requirement:** FR-004, FR-005

Verify that filtering and sorting work correctly together.

---

## TS-039 — Verify filter reset behavior

**Requirement:** FR-004

Verify that resetting or clearing filters restores the appropriate product listing.

---

## TS-040 — Verify filter usability

**Requirement:** FR-004, FR-011

Verify that filter controls are understandable and usable.

---

# 8. Product Sorting Scenarios

## TS-041 — Verify default product ordering

**Requirement:** FR-005

Verify that products are displayed in the expected default order.

---

## TS-042 — Verify sorting by price low to high

**Requirement:** FR-005

Verify that products are correctly arranged from lowest to highest price.

---

## TS-043 — Verify sorting by price high to low

**Requirement:** FR-005

Verify that products are correctly arranged from highest to lowest price.

---

## TS-044 — Verify changing sorting option

**Requirement:** FR-005

Verify that changing the sorting option updates the product order correctly.

---

## TS-045 — Verify sorting after applying a filter

**Requirement:** FR-004, FR-005

Verify that sorting works correctly on filtered results.

---

## TS-046 — Verify sorting does not remove products

**Requirement:** FR-005

Verify that sorting does not unexpectedly remove valid products.

---

# 9. Product Details Scenarios

## TS-047 — Verify opening product details

**Requirement:** FR-006

Verify that selecting a product opens its corresponding details.

---

## TS-048 — Verify product detail information

**Requirement:** FR-006

Verify product name, image, price and other available information.

---

## TS-049 — Verify product detail consistency with listing

**Requirement:** FR-002, FR-006

Verify that product details match information shown in the product listing.

---

## TS-050 — Verify Add to Cart from product details

**Requirement:** FR-006, FR-007

Verify that a product can be added to the cart from its details page where supported.

---

## TS-051 — Verify navigation back from product details

**Requirement:** FR-006

Verify that users can return to the product listing correctly.

---

# 10. Shopping Cart Scenarios

## TS-052 — Verify adding a single product to cart

**Requirement:** FR-007

Verify that a selected product is successfully added to the shopping cart.

---

## TS-053 — Verify adding multiple products

**Requirement:** FR-007

Verify that multiple products can be added and displayed correctly in the cart.

---

## TS-054 — Verify cart count

**Requirement:** FR-007

Verify that the cart item count updates correctly after adding or removing products.

---

## TS-055 — Verify product information in cart

**Requirement:** FR-007

Verify product name and price displayed in the cart.

---

## TS-056 — Verify cart quantity behavior

**Requirement:** FR-007

Verify that product quantity behaves correctly when changed.

---

## TS-057 — Verify removing a product

**Requirement:** FR-007

Verify that users can remove products from the cart.

---

## TS-058 — Verify cart total calculation

**Requirement:** FR-007

Verify that the cart total is calculated correctly.

---

## TS-059 — Verify empty cart behavior

**Requirement:** FR-007

Verify that an empty cart displays the appropriate state.

---

## TS-060 — Verify cart contents during navigation

**Requirement:** FR-007, FR-012

Verify that cart contents remain consistent during normal navigation.

---

# 11. Authentication Scenarios

## TS-061 — Verify login page accessibility

**Requirement:** FR-008

Verify that the login page/interface can be accessed correctly.

---

## TS-062 — Verify login with valid credentials

**Requirement:** FR-008

Verify successful authentication using valid credentials.

---

## TS-063 — Verify login with invalid credentials

**Requirement:** FR-008

Verify that invalid credentials are rejected.

---

## TS-064 — Verify login with incorrect password

**Requirement:** FR-008

Verify that an incorrect password does not authenticate the user.

---

## TS-065 — Verify login with empty credentials

**Requirement:** FR-008

Verify validation when required login fields are empty.

---

## TS-066 — Verify authentication state

**Requirement:** FR-008

Verify that authenticated state is maintained correctly during the expected workflow.

---

## TS-067 — Verify logout

**Requirement:** FR-008, FR-012

Verify that users can log out successfully.

---

# 12. Checkout Scenarios

## TS-068 — Verify navigation from cart to checkout

**Requirement:** FR-009

Verify that users can proceed from the cart to checkout.

---

## TS-069 — Verify checkout product information

**Requirement:** FR-009

Verify product, quantity and price information at checkout.

---

## TS-070 — Verify checkout total

**Requirement:** FR-009

Verify that checkout total matches the expected cart total.

---

## TS-071 — Verify valid checkout information

**Requirement:** FR-009

Verify that valid customer information is accepted.

---

## TS-072 — Verify required checkout fields

**Requirement:** FR-009

Verify validation of required checkout fields.

---

## TS-073 — Verify invalid checkout information

**Requirement:** FR-009

Verify that invalid customer information is rejected.

---

## TS-074 — Verify empty checkout fields

**Requirement:** FR-009

Verify behavior when required checkout fields are left empty.

---

## TS-075 — Verify checkout validation messages

**Requirement:** FR-009, FR-011

Verify that checkout validation messages are understandable and correctly displayed.

---

## TS-076 — Verify successful order completion

**Requirement:** FR-009

Verify that a valid checkout can be completed successfully.

---

## TS-077 — Verify order confirmation

**Requirement:** FR-009

Verify that an appropriate confirmation is displayed after successful order completion.

---

# 13. End-to-End Purchase Scenarios

## TS-078 — Verify complete single-product purchase flow

**Requirement:** FR-010

Verify the complete purchase journey using a single product.

---

## TS-079 — Verify purchase flow after product search

**Requirement:** FR-010

Verify purchase completion when the product is discovered using search.

---

## TS-080 — Verify purchase flow after filtering

**Requirement:** FR-010

Verify purchase completion after selecting a product using filters.

---

## TS-081 — Verify purchase flow with multiple products

**Requirement:** FR-010

Verify end-to-end purchase behavior with multiple products.

---

## TS-082 — Verify purchase flow after cart modification

**Requirement:** FR-010

Verify that modifying the cart before checkout does not corrupt the purchase flow.

---

## TS-083 — Verify invalid checkout prevents order completion

**Requirement:** FR-009, FR-010

Verify that invalid required information prevents successful order completion.

---

# 14. UI & Usability Scenarios

## TS-084 — Verify overall page layout

**Requirement:** FR-011

Verify that the overall page layout is consistent and usable.

---

## TS-085 — Verify button visibility and usability

**Requirement:** FR-011

Verify that important buttons are visible and understandable.

---

## TS-086 — Verify labels and input controls

**Requirement:** FR-011

Verify that labels, placeholders and input controls are understandable.

---

## TS-087 — Verify validation message readability

**Requirement:** FR-011

Verify that validation messages are clear and readable.

---

## TS-088 — Verify product card visual consistency

**Requirement:** FR-011

Verify that product cards maintain consistent visual structure.

---

## TS-089 — Verify responsive layout

**Requirement:** FR-011, NFR-003

Verify usability across supported viewport sizes.

---

# 15. Session & Error Handling Scenarios

## TS-090 — Verify session behavior after logout

**Requirement:** FR-012

Verify that logout terminates the authenticated session appropriately.

---

## TS-091 — Verify browser refresh behavior

**Requirement:** FR-012

Verify application behavior after refreshing the current page.

---

## TS-092 — Verify browser Back after logout

**Requirement:** FR-012

Verify that browser Back navigation does not incorrectly restore an authenticated state.

---

## TS-093 — Verify invalid user input handling

**Requirement:** FR-012

Verify that invalid inputs are handled without application failure.

---

## TS-094 — Verify empty-state handling

**Requirement:** FR-012

Verify that empty product/cart/search states are handled appropriately.

---

## TS-095 — Verify invalid navigation handling

**Requirement:** FR-012

Verify that invalid or unexpected navigation is handled gracefully.

---

## TS-096 — Verify application state consistency

**Requirement:** FR-012

Verify that application state remains consistent during normal user navigation.

---

# 16. Scenario Summary

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

---

# 17. Scenario-to-Requirement Mapping

| Requirement | Scenario IDs                                             |
| ----------- | -------------------------------------------------------- |
| FR-001      | TS-001 to TS-010                                         |
| FR-002      | TS-011 to TS-020                                         |
| FR-003      | TS-021 to TS-030                                         |
| FR-004      | TS-031 to TS-040                                         |
| FR-005      | TS-038, TS-041 to TS-046                                 |
| FR-006      | TS-047 to TS-051                                         |
| FR-007      | TS-016, TS-050, TS-052 to TS-060                         |
| FR-008      | TS-061 to TS-067                                         |
| FR-009      | TS-068 to TS-077, TS-083                                 |
| FR-010      | TS-078 to TS-083                                         |
| FR-011      | TS-002, TS-015, TS-040, TS-075, TS-084 to TS-089         |
| FR-012      | TS-006, TS-007, TS-009, TS-037, TS-060, TS-090 to TS-096 |

---

# 18. Scenario Design Principles

The scenarios intentionally cover:

* Positive flows
* Negative flows
* Boundary conditions
* Invalid input
* Empty input
* Search behavior
* Filter behavior
* Sorting behavior
* Cart calculations
* Authentication
* Checkout validation
* End-to-end workflows
* Session behavior
* UI consistency
* Usability
* Error handling

---

# 19. Traceability

The project will maintain the following traceability:

```text
Requirement
    ↓
Test Scenario
    ↓
Test Case
    ↓
Test Data
    ↓
Execution
    ↓
Defect
    ↓
Regression
    ↓
Test Summary
```

Every detailed test case should reference a valid:

* Requirement ID
* Scenario ID

This ensures that the final RTM can demonstrate complete requirement coverage.

---

# 20. Document Control

| Version | Date       | Description               |
| ------- | ---------- | ------------------------- |
| 1.0     | 2026-10-07 | Initial scenario baseline |

---

**End of Test Scenarios Document**
