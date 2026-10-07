# BStackDemo Manual QA Testing – Test Data

## 1. Document Information

| Field                | Details                      |
| -------------------- | ---------------------------- |
| Project              | BStackDemo Manual QA Testing |
| Document             | Test Data                    |
| Application          | BStackDemo                   |
| Testing Type         | Manual Testing               |
| Test Data Version    | 1.0                          |
| Test Cases Supported | 128                          |
| Status               | Ready for Execution          |
| Data Classification  | Synthetic / Test Data        |

---

## 2. Purpose

This document defines the test data required to execute the manual test cases for the BStackDemo application.

The data covers:

* Product search
* Product filtering
* Product sorting
* Product details
* Shopping cart
* Authentication
* Checkout
* End-to-end purchase flows
* Negative testing
* Boundary testing
* UI and usability testing
* Session and error-handling scenarios

All personal information in this document is synthetic and should be used only for testing.

---

# 3. Test Data Categories

| Category | Purpose                     |
| -------- | --------------------------- |
| TD-01    | Product data                |
| TD-02    | Search data                 |
| TD-03    | Filter data                 |
| TD-04    | Sorting data                |
| TD-05    | Authentication data         |
| TD-06    | Cart data                   |
| TD-07    | Checkout data               |
| TD-08    | Negative data               |
| TD-09    | Boundary data               |
| TD-10    | Special-character data      |
| TD-11    | End-to-end purchase data    |
| TD-12    | Session/error-handling data |

---

# 4. Product Test Data

BStackDemo provides a catalogue of products that can be used for product-listing, product-detail, cart and checkout testing.

| Data ID  | Product Category | Example Product   | Purpose                    |
| -------- | ---------------- | ----------------- | -------------------------- |
| PROD-D01 | iPhone           | iPhone 12         | Product search/detail/cart |
| PROD-D02 | iPhone           | iPhone 12 Pro Max | Search/filter/detail       |
| PROD-D03 | Samsung          | Galaxy S20        | Product listing/detail     |
| PROD-D04 | Samsung          | Galaxy S20+       | Search/detail              |
| PROD-D05 | Samsung          | Galaxy S21        | Listing/detail             |
| PROD-D06 | Google           | Pixel 4           | Search/detail              |
| PROD-D07 | OnePlus          | OnePlus 8         | Product testing            |
| PROD-D08 | OnePlus          | OnePlus 8T        | Search/detail              |
| PROD-D09 | Motorola         | Moto G7           | Listing/detail             |
| PROD-D10 | Apple            | iPhone 11         | Search/detail              |
| PROD-D11 | Apple            | iPhone XR         | Product testing            |
| PROD-D12 | Apple            | iPhone XS         | Product testing            |

> **Note:** Product names should be verified against the current BStackDemo catalogue before execution because demo application data can change.

---

# 5. Search Test Data

## 5.1 Valid Search Terms

| Data ID    | Search Input | Expected Use                         |
| ---------- | ------------ | ------------------------------------ |
| SEARCH-D01 | iPhone       | Matching products displayed          |
| SEARCH-D02 | Samsung      | Samsung products displayed           |
| SEARCH-D03 | Galaxy       | Products containing Galaxy displayed |
| SEARCH-D04 | Pixel        | Matching Pixel products displayed    |
| SEARCH-D05 | OnePlus      | Matching OnePlus products displayed  |
| SEARCH-D06 | Moto         | Matching Motorola products displayed |

### Related Test Cases

Used primarily by:

* TC-SEARCH-001
* TC-SEARCH-002
* TC-SEARCH-003
* TC-SEARCH-004
* TC-SEARCH-005
* TC-PROD-003
* TC-PROD-004

---

## 5.2 Invalid Search Terms

| Data ID    | Search Input        | Purpose                  |
| ---------- | ------------------- | ------------------------ |
| SEARCH-D07 | xyzabc999           | No-result search         |
| SEARCH-D08 | productdoesnotexist | No-result search         |
| SEARCH-D09 | 999999              | Numeric no-result search |
| SEARCH-D10 | qwertyuiop          | Random invalid input     |

Expected behavior:

* Application should handle the search gracefully.
* No unrelated products should be displayed.
* Appropriate empty/no-result state should be shown where supported.

---

## 5.3 Empty Search Data

| Data ID    | Input       | Purpose                 |
| ---------- | ----------- | ----------------------- |
| SEARCH-D11 | Empty       | Empty search validation |
| SEARCH-D12 | Spaces only | Whitespace handling     |

---

# 6. Filter Test Data

## 6.1 Brand Filters

| Data ID    | Filter   | Purpose            |
| ---------- | -------- | ------------------ |
| FILTER-D01 | Apple    | Filter by Apple    |
| FILTER-D02 | Samsung  | Filter by Samsung  |
| FILTER-D03 | Google   | Filter by Google   |
| FILTER-D04 | OnePlus  | Filter by OnePlus  |
| FILTER-D05 | Motorola | Filter by Motorola |

---

## 6.2 Multiple Filter Combinations

| Data ID    | Filter Combination | Purpose                     |
| ---------- | ------------------ | --------------------------- |
| FILTER-D06 | Apple + Samsung    | Multiple selection behavior |
| FILTER-D07 | Samsung + Google   | Multiple selection behavior |
| FILTER-D08 | Apple + OnePlus    | Multiple selection behavior |

Expected result:

Only products satisfying the selected filter criteria should be displayed.

---

## 6.3 Filter Reset Data

| Data ID    | Initial Filter  | Reset Action       |
| ---------- | --------------- | ------------------ |
| FILTER-D09 | Apple           | Clear/reset filter |
| FILTER-D10 | Samsung         | Clear/reset filter |
| FILTER-D11 | Multiple brands | Clear all filters  |

Expected result:

The complete product catalogue should be restored after clearing filters.

---

# 7. Sorting Test Data

| Data ID  | Sorting Option    | Purpose          |
| -------- | ----------------- | ---------------- |
| SORT-D01 | Lowest to Highest | Price ascending  |
| SORT-D02 | Highest to Lowest | Price descending |
| SORT-D03 | A to Z            | Name ascending   |
| SORT-D04 | Z to A            | Name descending  |

### Validation

For price sorting:

```text
Product A price <= Product B price <= Product C price
```

For reverse price sorting:

```text
Product A price >= Product B price >= Product C price
```

For alphabetical sorting:

```text
A → B → C → ... → Z
```

---

# 8. Authentication Test Data

## 8.1 Valid Login Data

| Data ID  | Username              | Password       | Purpose          |
| -------- | --------------------- | -------------- | ---------------- |
| AUTH-D01 | Valid registered user | Valid password | Successful login |

> Use the valid demo credentials provided by the BStackDemo application/documentation at execution time rather than storing personal credentials in the repository.

---

## 8.2 Invalid Login Data

| Data ID  | Username     | Password         | Expected Purpose         |
| -------- | ------------ | ---------------- | ------------------------ |
| AUTH-D02 | Invalid user | Valid password   | Invalid username         |
| AUTH-D03 | Valid user   | Invalid password | Invalid password         |
| AUTH-D04 | Invalid user | Invalid password | Both credentials invalid |
| AUTH-D05 | Empty        | Valid password   | Empty username           |
| AUTH-D06 | Valid user   | Empty            | Empty password           |
| AUTH-D07 | Empty        | Empty            | Empty login form         |

Expected behavior:

* Invalid credentials should not authenticate the user.
* Appropriate validation/error feedback should be displayed.
* The application should remain stable.

---

# 9. Cart Test Data

## 9.1 Single Product

| Data ID  | Product            | Quantity |
| -------- | ------------------ | -------: |
| CART-D01 | iPhone 12          |        1 |
| CART-D02 | Samsung Galaxy S20 |        1 |
| CART-D03 | OnePlus 8          |        1 |

Purpose:

* Add one product
* Verify product information
* Verify quantity
* Verify price
* Verify cart total

---

## 9.2 Multiple Products

| Data ID  | Product 1 | Product 2  | Quantity |
| -------- | --------- | ---------- | -------: |
| CART-D04 | iPhone 12 | Galaxy S20 |   1 each |
| CART-D05 | OnePlus 8 | Pixel 4    |   1 each |
| CART-D06 | iPhone 12 | OnePlus 8T |   1 each |

Purpose:

* Multiple product handling
* Cart total calculation
* Product removal
* Quantity management

---

## 9.3 Quantity Test Data

| Data ID  | Quantity | Purpose                   |
| -------- | -------: | ------------------------- |
| CART-D07 |        1 | Minimum normal quantity   |
| CART-D08 |        2 | Multiple quantity         |
| CART-D09 |        3 | Quantity increase         |
| CART-D10 |        5 | Higher quantity           |
| CART-D11 |        0 | Boundary/invalid quantity |
| CART-D12 |       -1 | Negative quantity         |
| CART-D13 |      999 | Large quantity            |

> Whether quantities can be directly edited depends on the current UI implementation. If quantity controls are not exposed, these values should be tested through available UI actions.

---

# 10. Checkout Test Data

## 10.1 Valid Customer Data

| Field       | Test Value      |
| ----------- | --------------- |
| First Name  | Aman            |
| Last Name   | Singh           |
| Address     | 123 Test Street |
| City        | Dehradun        |
| State       | Uttarakhand     |
| Postal Code | 248001          |

Data ID: `CHECKOUT-D01`

---

## 10.2 Alternate Valid Customer Data

| Field       | Test Value        |
| ----------- | ----------------- |
| First Name  | Rahul             |
| Last Name   | Sharma            |
| Address     | 45 Testing Avenue |
| City        | Delhi             |
| State       | Delhi             |
| Postal Code | 110001            |

Data ID: `CHECKOUT-D02`

---

# 11. Checkout Negative Data

## 11.1 Missing Required Fields

| Data ID      | Field Left Empty | Purpose                   |
| ------------ | ---------------- | ------------------------- |
| CHECKOUT-D03 | First Name       | Required-field validation |
| CHECKOUT-D04 | Last Name        | Required-field validation |
| CHECKOUT-D05 | Address          | Required-field validation |
| CHECKOUT-D06 | City             | Required-field validation |
| CHECKOUT-D07 | State            | Required-field validation |
| CHECKOUT-D08 | Postal Code      | Required-field validation |

Expected result:

The application should prevent completion of checkout when required information is missing.

---

# 12. Boundary Test Data

## 12.1 Name Fields

| Data ID   | Input              | Purpose                   |
| --------- | ------------------ | ------------------------- |
| BOUND-D01 | A                  | Minimum-length check      |
| BOUND-D02 | Aman               | Normal value              |
| BOUND-D03 | 50-character name  | Maximum-length behavior   |
| BOUND-D04 | 100-character name | Excessive-length behavior |

---

## 12.2 Postal Code

| Data ID   | Input  | Purpose                      |
| --------- | ------ | ---------------------------- |
| BOUND-D05 | 1      | Too short                    |
| BOUND-D06 | 248001 | Valid Indian PIN             |
| BOUND-D07 | 000000 | Boundary/invalid-value check |
| BOUND-D08 | 999999 | Upper numeric boundary       |

---

# 13. Special Character Test Data

| Data ID     | Input         | Purpose                          |
| ----------- | ------------- | -------------------------------- |
| SPECIAL-D01 | `@#$%`        | Special-character handling       |
| SPECIAL-D02 | `Aman@123`    | Alphanumeric + special character |
| SPECIAL-D03 | `<script>`    | Input validation check           |
| SPECIAL-D04 | `' OR '1'='1` | Negative input handling          |
| SPECIAL-D05 | `Test & Demo` | Ampersand handling               |
| SPECIAL-D06 | `Aman-Singh`  | Hyphen handling                  |

These values are used only to verify that normal application input fields handle unexpected characters safely and gracefully.

---

# 14. Whitespace Test Data

| Data ID   | Input   | Purpose                   |
| --------- | ------- | ------------------------- |
| SPACE-D01 | ` Aman` | Leading space             |
| SPACE-D02 | `Aman ` | Trailing space            |
| SPACE-D03 | `Aman`  | Leading + trailing spaces |
| SPACE-D04 | `   `   | Spaces only               |

Expected behavior:

The application should handle whitespace consistently and should not produce unexpected application errors.

---

# 15. End-to-End Purchase Data

## E2E Dataset 1

| Field       | Value           |
| ----------- | --------------- |
| Product     | iPhone 12       |
| Quantity    | 1               |
| First Name  | Aman            |
| Last Name   | Singh           |
| Address     | 123 Test Street |
| City        | Dehradun        |
| State       | Uttarakhand     |
| Postal Code | 248001          |

Data ID: `E2E-D01`

Flow:

```text
Homepage
   ↓
Product Listing
   ↓
Search Product
   ↓
Product Details
   ↓
Add to Cart
   ↓
Cart
   ↓
Checkout
   ↓
Enter Customer Data
   ↓
Submit Order
   ↓
Order Confirmation
```

---

## E2E Dataset 2

| Field       | Value              |
| ----------- | ------------------ |
| Product     | Samsung Galaxy S20 |
| Quantity    | 1                  |
| First Name  | Rahul              |
| Last Name   | Sharma             |
| Address     | 45 Testing Avenue  |
| City        | Delhi              |
| State       | Delhi              |
| Postal Code | 110001             |

Data ID: `E2E-D02`

---

# 16. Multi-Product E2E Data

| Data ID | Product 1 | Product 2  | Quantity |
| ------- | --------- | ---------- | -------: |
| E2E-D03 | iPhone 12 | Galaxy S20 |   1 each |
| E2E-D04 | OnePlus 8 | Pixel 4    |   1 each |

Purpose:

* Multiple product selection
* Cart validation
* Total calculation
* Checkout with multiple items

---

# 17. Session Test Data

| Data ID     | Action                        | Purpose                   |
| ----------- | ----------------------------- | ------------------------- |
| SESSION-D01 | Refresh page                  | State persistence         |
| SESSION-D02 | Navigate back                 | Navigation/state handling |
| SESSION-D03 | Navigate forward              | Browser history handling  |
| SESSION-D04 | Open new tab                  | Session behavior          |
| SESSION-D05 | Close and reopen browser      | Session persistence       |
| SESSION-D06 | Clear browser storage/cookies | Session reset behavior    |

---

# 18. Error-Handling Data

| Data ID   | Condition                       | Expected Behavior                       |
| --------- | ------------------------------- | --------------------------------------- |
| ERROR-D01 | Invalid search                  | Graceful no-result state                |
| ERROR-D02 | Invalid login                   | Authentication error                    |
| ERROR-D03 | Empty login                     | Validation message                      |
| ERROR-D04 | Missing checkout field          | Field validation                        |
| ERROR-D05 | Invalid postal code             | Validation/error                        |
| ERROR-D06 | Empty cart checkout attempt     | Application should handle appropriately |
| ERROR-D07 | Browser refresh during workflow | Stable application state                |

---

# 19. Test Data Mapping

| Test Data Category     | Related Test Modules             |
| ---------------------- | -------------------------------- |
| Product Data           | Product Listing, Product Details |
| Search Data            | Product Search                   |
| Filter Data            | Product Filtering                |
| Sort Data              | Product Sorting                  |
| Authentication Data    | Authentication                   |
| Cart Data              | Shopping Cart                    |
| Checkout Data          | Checkout                         |
| Boundary Data          | UI, Checkout, Authentication     |
| Special Character Data | Search, Authentication, Checkout |
| Session Data           | Session & Error Handling         |
| E2E Data               | End-to-End Purchase              |

---

# 20. Test Data Management Guidelines

### 20.1 Do Not Use Real Personal Information

All names, addresses and other customer information in this document are synthetic.

Do not commit:

* Personal passwords
* Real payment information
* Real customer information
* API keys
* Authentication tokens
* Private credentials

to the GitHub repository.

### 20.2 Credentials

Credentials supplied by the demo application should be treated as test credentials.

If credentials change, update the test execution environment rather than hard-coding credentials into multiple test cases.

### 20.3 Reusability

The same test data can be reused across multiple test cases when the objective is identical.

For example:

`CHECKOUT-D01`

can be reused for:

* TC-CHECKOUT-001
* TC-CHECKOUT-002
* TC-CHECKOUT-005
* TC-CHECKOUT-012
* TC-E2E-001

### 20.4 Data Isolation

Where a test modifies application state, reset the application state before executing the next independent test.

Examples:

* Empty the cart.
* Reset filters.
* Reset sorting.
* Log out when required.
* Refresh the application.
* Start with a clean browser session where required.

---

# 21. Test Data Traceability

| Data ID          | Primary Test Area         |
| ---------------- | ------------------------- |
| PROD-D01–D12     | Product Listing / Details |
| SEARCH-D01–D12   | Search                    |
| FILTER-D01–D11   | Filtering                 |
| SORT-D01–D04     | Sorting                   |
| AUTH-D01–D07     | Authentication            |
| CART-D01–D13     | Shopping Cart             |
| CHECKOUT-D01–D08 | Checkout                  |
| BOUND-D01–D08    | Boundary Testing          |
| SPECIAL-D01–D06  | Negative/Input Testing    |
| SPACE-D01–D04    | Input Validation          |
| E2E-D01–D04      | End-to-End Testing        |
| SESSION-D01–D06  | Session Testing           |
| ERROR-D01–D07    | Error Handling            |

---

# 22. Data Validation Checklist

Before executing the test suite, verify:

* [ ] Product data exists in the current BStackDemo catalogue.
* [ ] Search terms return expected results.
* [ ] Filter values are available.
* [ ] Sorting options are available.
* [ ] Valid demo credentials are available.
* [ ] Checkout fields are accessible.
* [ ] Test customer data is ready.
* [ ] Invalid and boundary data is prepared.
* [ ] Browser session is clean where required.
* [ ] Previous cart items have been removed where required.
* [ ] Test data does not contain real sensitive information.

---

# 23. Document Status

**Status:** Ready for Manual Execution

**Important:** Product names, available filters, authentication credentials and UI behavior should be verified against the current BStackDemo build before execution because this is a live demo application and its data may change.
