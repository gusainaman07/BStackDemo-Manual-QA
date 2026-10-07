# BStackDemo Manual QA Testing — Test Cases

## 1. Document Information

| Field            | Details                      |
| ---------------- | ---------------------------- |
| Project          | BStackDemo Manual QA Testing |
| Application      | BStackDemo                   |
| Document         | Test Cases                   |
| Testing Type     | Manual Testing               |
| Version          | 1.0                          |
| Total Test Cases | 128                          |
| Status           | Baseline                     |

---

# 2. Test Case Format

Each test case contains:

* Test Case ID
* Requirement ID
* Scenario ID
* Module
* Test Objective
* Priority
* Preconditions
* Test Data
* Test Steps
* Expected Result

---

# 3. Test Case Summary

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
| **TOTAL**                |    **128** |

---

# 4. Homepage & Navigation

## TC-NAV-001 — Verify Homepage Loads Successfully

**Requirement:** FR-001
**Scenario:** TS-001
**Priority:** P1

**Preconditions:** Browser is open and internet connection is available.

**Test Steps:**

1. Open the BStackDemo URL.
2. Wait for the application to load.

**Expected Result:**
Homepage loads successfully without unexpected errors and displays the main shopping interface.

---

## TC-NAV-002 — Verify Application Branding

**Requirement:** FR-001
**Scenario:** TS-002
**Priority:** P2

**Test Steps:**

1. Open the homepage.
2. Observe the application branding.

**Expected Result:**
Application branding is displayed correctly and is visually identifiable.

---

## TC-NAV-003 — Verify Product Catalog Navigation

**Requirement:** FR-001
**Scenario:** TS-003
**Priority:** P1

**Test Steps:**

1. Open the homepage.
2. Navigate to the product/catalog area.

**Expected Result:**
Product catalog opens successfully.

---

## TC-NAV-004 — Verify Shopping Cart Navigation

**Requirement:** FR-001
**Scenario:** TS-004
**Priority:** P1

**Test Steps:**

1. Open the homepage.
2. Click the shopping cart control.

**Expected Result:**
Shopping cart page opens successfully.

---

## TC-NAV-005 — Verify Login Navigation

**Requirement:** FR-001
**Scenario:** TS-005
**Priority:** P1

**Test Steps:**

1. Open BStackDemo.
2. Select the login option.

**Expected Result:**
Login interface opens successfully.

---

## TC-NAV-006 — Verify Browser Back Navigation

**Requirement:** FR-001, FR-012
**Scenario:** TS-006
**Priority:** P2

**Test Steps:**

1. Open the product listing.
2. Open a product.
3. Click the browser Back button.

**Expected Result:**
Previous page is displayed correctly without unexpected application errors.

---

## TC-NAV-007 — Verify Browser Forward Navigation

**Requirement:** FR-001, FR-012
**Scenario:** TS-007
**Priority:** P2

**Test Steps:**

1. Navigate from the product listing to a product.
2. Use browser Back.
3. Use browser Forward.

**Expected Result:**
Forward navigation returns to the expected page.

---

## TC-NAV-008 — Verify Navigation Links

**Requirement:** FR-001
**Scenario:** TS-008
**Priority:** P2

**Test Steps:**

1. Open the homepage.
2. Select each major navigation link.
3. Observe the destination.

**Expected Result:**
Each navigation link opens the correct destination.

---

## TC-NAV-009 — Verify Page Refresh

**Requirement:** FR-001, FR-012
**Scenario:** TS-009
**Priority:** P2

**Test Steps:**

1. Open the product listing.
2. Refresh the browser.
3. Observe the page.

**Expected Result:**
Page reloads correctly and application state is not unexpectedly corrupted.

---

## TC-NAV-010 — Verify Navigation Consistency

**Requirement:** FR-001, FR-011
**Scenario:** TS-010
**Priority:** P2

**Test Steps:**

1. Visit homepage.
2. Visit product listing.
3. Visit product details.
4. Visit cart.

**Expected Result:**
Navigation controls remain consistent and usable across pages.

---

# 5. Product Listing

## TC-PROD-001 — Verify Products Are Displayed

**Requirement:** FR-002
**Scenario:** TS-011
**Priority:** P1

**Steps:**

1. Open product listing.
2. Observe displayed products.

**Expected Result:**
Available products are displayed correctly.

---

## TC-PROD-002 — Verify Product Images

**Requirement:** FR-002
**Scenario:** TS-012
**Priority:** P2

**Steps:**

1. Open product listing.
2. Inspect product images.

**Expected Result:**
Product images load correctly without broken-image indicators.

---

## TC-PROD-003 — Verify Product Names

**Requirement:** FR-002
**Scenario:** TS-013
**Priority:** P2

**Steps:**

1. Open product listing.
2. Inspect product names.

**Expected Result:**
Product names are visible and correctly associated with their products.

---

## TC-PROD-004 — Verify Product Prices

**Requirement:** FR-002
**Scenario:** TS-014
**Priority:** P1

**Steps:**

1. Open product listing.
2. Inspect product prices.

**Expected Result:**
Each product displays its corresponding price correctly.

---

## TC-PROD-005 — Verify Product Card Layout

**Requirement:** FR-002, FR-011
**Scenario:** TS-015
**Priority:** P3

**Steps:**

1. Open product listing.
2. Compare multiple product cards.

**Expected Result:**
Product cards maintain a consistent layout.

---

## TC-PROD-006 — Verify Add to Cart Control

**Requirement:** FR-002, FR-007
**Scenario:** TS-016
**Priority:** P1

**Steps:**

1. Select an available product.
2. Click Add to Cart.

**Expected Result:**
Product is added successfully and cart state updates.

---

## TC-PROD-007 — Verify Product Information Consistency

**Requirement:** FR-002, FR-006
**Scenario:** TS-017
**Priority:** P1

**Steps:**

1. Note a product's name and price in listing.
2. Open the same product.
3. Compare the information.

**Expected Result:**
Product listing and product details show consistent information.

---

## TC-PROD-008 — Verify Product List After Navigation

**Requirement:** FR-002
**Scenario:** TS-018
**Priority:** P2

**Steps:**

1. Open product listing.
2. Navigate to another page.
3. Return to product listing.

**Expected Result:**
Product listing loads correctly.

---

## TC-PROD-009 — Verify Product List After Filtering

**Requirement:** FR-002, FR-004
**Scenario:** TS-019
**Priority:** P1

**Steps:**

1. Open product listing.
2. Apply a valid filter.
3. Observe products.

**Expected Result:**
Only products matching the selected filter are displayed.

---

## TC-PROD-010 — Verify Product List After Sorting

**Requirement:** FR-002, FR-005
**Scenario:** TS-020
**Priority:** P1

**Steps:**

1. Open product listing.
2. Apply a sorting option.

**Expected Result:**
Products are displayed in the selected order without incorrect product information.

---

## TC-PROD-011 — Verify Multiple Product Cards

**Requirement:** FR-002
**Scenario:** TS-011
**Priority:** P2

**Steps:**

1. Open the product listing.
2. Observe multiple products.

**Expected Result:**
Multiple available products are displayed independently without overlapping or duplicated card content.

---

## TC-PROD-012 — Verify Product List Stability After Repeated Navigation

**Requirement:** FR-002
**Scenario:** TS-018
**Priority:** P2

**Steps:**

1. Open product listing.
2. Navigate to a product.
3. Return to listing.
4. Repeat for another product.

**Expected Result:**
Product listing continues to display correctly after repeated navigation.

---

# 6. Product Search

## TC-SEARCH-001 — Search Exact Product Name

**Requirement:** FR-003
**Scenario:** TS-021
**Priority:** P1

**Test Data:** Valid product name.

**Steps:**

1. Enter an exact product name in search.
2. Submit the search.

**Expected Result:**
Relevant product is displayed.

---

## TC-SEARCH-002 — Search Partial Product Name

**Requirement:** FR-003
**Scenario:** TS-022
**Priority:** P2

**Test Data:** Partial product keyword.

**Steps:**

1. Enter a partial product name.
2. Execute search.

**Expected Result:**
Relevant results are displayed if partial search is supported.

---

## TC-SEARCH-003 — Search Using Uppercase

**Requirement:** FR-003
**Scenario:** TS-023
**Priority:** P3

**Test Data:** Uppercase search keyword.

**Expected Result:**
Search behaves consistently with supported case-insensitive behavior.

---

## TC-SEARCH-004 — Search Using Lowercase

**Requirement:** FR-003
**Scenario:** TS-024
**Priority:** P3

**Test Data:** Lowercase search keyword.

**Expected Result:**
Search behaves consistently with supported case-insensitive behavior.

---

## TC-SEARCH-005 — Search With Leading/Trailing Spaces

**Requirement:** FR-003
**Scenario:** TS-025
**Priority:** P2

**Test Data:** `"  product  "`.

**Expected Result:**
Unnecessary spaces are handled appropriately and do not cause unexpected results.

---

## TC-SEARCH-006 — Search With No Matching Product

**Requirement:** FR-003
**Scenario:** TS-026
**Priority:** P1

**Test Data:** Non-existing product name.

**Expected Result:**
Appropriate no-results behavior is displayed.

---

## TC-SEARCH-007 — Search With Empty Input

**Requirement:** FR-003
**Scenario:** TS-027
**Priority:** P2

**Steps:**

1. Leave search field empty.
2. Execute search.

**Expected Result:**
Application handles empty search appropriately without errors.

---

## TC-SEARCH-008 — Search With Special Characters

**Requirement:** FR-003
**Scenario:** TS-028
**Priority:** P2

**Test Data:** `@#$%^&*`

**Expected Result:**
Application handles special characters without crashing.

---

## TC-SEARCH-009 — Change Search Criteria

**Requirement:** FR-003
**Scenario:** TS-029
**Priority:** P2

**Steps:**

1. Search for Product A.
2. Change search keyword to Product B.

**Expected Result:**
Results update according to the new search criteria.

---

## TC-SEARCH-010 — Clear Search

**Requirement:** FR-003
**Scenario:** TS-030
**Priority:** P2

**Steps:**

1. Perform a valid search.
2. Clear the search field.

**Expected Result:**
Appropriate product listing is restored.

---

# 7. Product Filtering

## TC-FILTER-001 — Verify Available Filters

**Requirement:** FR-004
**Scenario:** TS-031
**Priority:** P1

**Expected Result:**
Available filter controls are displayed correctly.

---

## TC-FILTER-002 — Apply Single Filter

**Requirement:** FR-004
**Scenario:** TS-032
**Priority:** P1

**Steps:**

1. Select one available filter.
2. Observe product listing.

**Expected Result:**
Products match the selected filter.

---

## TC-FILTER-003 — Remove Applied Filter

**Requirement:** FR-004
**Scenario:** TS-033
**Priority:** P1

**Steps:**

1. Apply a filter.
2. Remove the filter.

**Expected Result:**
Appropriate unfiltered product list is restored.

---

## TC-FILTER-004 — Apply Multiple Filters

**Requirement:** FR-004
**Scenario:** TS-034
**Priority:** P1

**Steps:**

1. Select multiple compatible filters.

**Expected Result:**
Displayed products satisfy the selected filter conditions.

---

## TC-FILTER-005 — Verify Filter Combination

**Requirement:** FR-004
**Scenario:** TS-035
**Priority:** P1

**Expected Result:**
Only products matching the complete filter combination are displayed.

---

## TC-FILTER-006 — Filter With No Matching Products

**Requirement:** FR-004
**Scenario:** TS-036
**Priority:** P2

**Expected Result:**
Application displays an appropriate no-results state.

---

## TC-FILTER-007 — Filter State During Navigation

**Requirement:** FR-004, FR-012
**Scenario:** TS-037
**Priority:** P2

**Steps:**

1. Apply a filter.
2. Navigate to another page.
3. Return to product listing.

**Expected Result:**
Filter behavior remains consistent with the application's intended state management.

---

## TC-FILTER-008 — Filter and Sort Together

**Requirement:** FR-004, FR-005
**Scenario:** TS-038
**Priority:** P1

**Steps:**

1. Apply a filter.
2. Apply sorting.

**Expected Result:**
Filtered products are sorted according to the selected sorting option.

---

## TC-FILTER-009 — Reset Filters

**Requirement:** FR-004
**Scenario:** TS-039
**Priority:** P2

**Expected Result:**
Resetting filters restores the appropriate product listing.

---

## TC-FILTER-010 — Verify Filter Usability

**Requirement:** FR-004, FR-011
**Scenario:** TS-040
**Priority:** P3

**Expected Result:**
Filter controls are understandable and usable.

---

## TC-FILTER-011 — Apply Filter After Search

**Requirement:** FR-003, FR-004
**Scenario:** TS-032
**Priority:** P2

**Steps:**

1. Search for a product.
2. Apply a compatible filter.

**Expected Result:**
Displayed results respect both the search criteria and filter where supported.

---

## TC-FILTER-012 — Remove Filter After Search

**Requirement:** FR-003, FR-004
**Scenario:** TS-033
**Priority:** P2

**Steps:**

1. Perform a search.
2. Apply a filter.
3. Remove the filter.

**Expected Result:**
The search results are restored appropriately.

---

# 8. Product Sorting

## TC-SORT-001 — Verify Default Product Order

**Requirement:** FR-005
**Scenario:** TS-041
**Priority:** P2

**Expected Result:**
Products appear in the application's default order.

---

## TC-SORT-002 — Sort Price Low to High

**Requirement:** FR-005
**Scenario:** TS-042
**Priority:** P1

**Expected Result:**
Products are arranged from lowest price to highest price.

---

## TC-SORT-003 — Sort Price High to Low

**Requirement:** FR-005
**Scenario:** TS-043
**Priority:** P1

**Expected Result:**
Products are arranged from highest price to lowest price.

---

## TC-SORT-004 — Change Sorting Option

**Requirement:** FR-005
**Scenario:** TS-044
**Priority:** P2

**Steps:**

1. Select one sorting option.
2. Select another sorting option.

**Expected Result:**
Product order updates correctly.

---

## TC-SORT-005 — Sort After Filtering

**Requirement:** FR-004, FR-005
**Scenario:** TS-045
**Priority:** P1

**Expected Result:**
Only filtered products are displayed and they follow the selected sort order.

---

## TC-SORT-006 — Verify Sorting Does Not Remove Products

**Requirement:** FR-005
**Scenario:** TS-046
**Priority:** P1

**Expected Result:**
Sorting changes order but does not unexpectedly remove products.

---

## TC-SORT-007 — Repeat Sorting

**Requirement:** FR-005
**Scenario:** TS-044
**Priority:** P2

**Steps:**

1. Apply one sorting option.
2. Apply another.
3. Return to the original option.

**Expected Result:**
Product order correctly follows the selected option each time.

---

## TC-SORT-008 — Sort After Navigation

**Requirement:** FR-005
**Scenario:** TS-041
**Priority:** P2

**Steps:**

1. Apply a sorting option.
2. Open a product.
3. Return to the listing.

**Expected Result:**
Application behaves consistently according to its intended sorting-state behavior.

---

# 9. Product Details

## TC-DETAIL-001 — Open Product Details

**Requirement:** FR-006
**Scenario:** TS-047
**Priority:** P1

**Expected Result:**
Selected product details page opens correctly.

---

## TC-DETAIL-002 — Verify Product Name in Details

**Requirement:** FR-006
**Scenario:** TS-048
**Priority:** P2

**Expected Result:**
Correct product name is displayed.

---

## TC-DETAIL-003 — Verify Product Image in Details

**Requirement:** FR-006
**Scenario:** TS-048
**Priority:** P2

**Expected Result:**
Correct product image is displayed.

---

## TC-DETAIL-004 — Verify Product Price in Details

**Requirement:** FR-006
**Scenario:** TS-048
**Priority:** P1

**Expected Result:**
Correct product price is displayed.

---

## TC-DETAIL-005 — Compare Details With Product Listing

**Requirement:** FR-002, FR-006
**Scenario:** TS-049
**Priority:** P1

**Expected Result:**
Product information matches the product listing.

---

## TC-DETAIL-006 — Add Product to Cart From Details

**Requirement:** FR-006, FR-007
**Scenario:** TS-050
**Priority:** P1

**Expected Result:**
Selected product is added to the cart successfully.

---

## TC-DETAIL-007 — Navigate Back From Details

**Requirement:** FR-006
**Scenario:** TS-051
**Priority:** P2

**Expected Result:**
User returns to the appropriate product listing.

---

## TC-DETAIL-008 — Verify Product Availability Information

**Requirement:** FR-006
**Scenario:** TS-048
**Priority:** P2

**Expected Result:**
Availability information, where provided, is correctly displayed.

---

## TC-DETAIL-009 — Verify Details For Multiple Products

**Requirement:** FR-006
**Scenario:** TS-047
**Priority:** P2

**Steps:**

1. Open Product A.
2. Return to listing.
3. Open Product B.

**Expected Result:**
Each product displays its own correct details.

---

## TC-DETAIL-010 — Verify Details Page Layout

**Requirement:** FR-006, FR-011
**Scenario:** TS-048
**Priority:** P3

**Expected Result:**
Product details page is readable and visually consistent.

---

# 10. Shopping Cart

## TC-CART-001 — Add Single Product

**Requirement:** FR-007
**Scenario:** TS-052
**Priority:** P1

**Expected Result:**
Selected product appears in the cart.

---

## TC-CART-002 — Verify Cart Count After Adding Product

**Requirement:** FR-007
**Scenario:** TS-054
**Priority:** P1

**Expected Result:**
Cart count reflects the added item according to the application's quantity/count behavior.

---

## TC-CART-003 — Add Multiple Different Products

**Requirement:** FR-007
**Scenario:** TS-053
**Priority:** P1

**Expected Result:**
All selected products appear correctly in the cart.

---

## TC-CART-004 — Add Same Product Again

**Requirement:** FR-007
**Scenario:** TS-053
**Priority:** P1

**Expected Result:**
Application handles repeated addition according to its intended cart/quantity behavior.

---

## TC-CART-005 — Verify Product Name in Cart

**Requirement:** FR-007
**Scenario:** TS-055
**Priority:** P2

**Expected Result:**
Correct product name is displayed.

---

## TC-CART-006 — Verify Product Price in Cart

**Requirement:** FR-007
**Scenario:** TS-055
**Priority:** P1

**Expected Result:**
Correct product price is displayed.

---

## TC-CART-007 — Verify Product Quantity

**Requirement:** FR-007
**Scenario:** TS-056
**Priority:** P1

**Expected Result:**
Product quantity is displayed correctly.

---

## TC-CART-008 — Increase Product Quantity

**Requirement:** FR-007
**Scenario:** TS-056
**Priority:** P1

**Expected Result:**
Quantity increases correctly and related totals update appropriately.

---

## TC-CART-009 — Decrease Product Quantity

**Requirement:** FR-007
**Scenario:** TS-056
**Priority:** P1

**Expected Result:**
Quantity decreases correctly and related totals update appropriately.

---

## TC-CART-010 — Remove Product

**Requirement:** FR-007
**Scenario:** TS-057
**Priority:** P1

**Expected Result:**
Selected product is removed from the cart.

---

## TC-CART-011 — Verify Cart Total

**Requirement:** FR-007
**Scenario:** TS-058
**Priority:** P1

**Expected Result:**
Cart total is calculated correctly.

---

## TC-CART-012 — Verify Multiple Product Total

**Requirement:** FR-007
**Scenario:** TS-058
**Priority:** P1

**Expected Result:**
Total reflects all products and quantities correctly.

---

## TC-CART-013 — Remove One Product From Multiple Products

**Requirement:** FR-007
**Scenario:** TS-057
**Priority:** P1

**Expected Result:**
Only the selected product is removed and remaining products remain unchanged.

---

## TC-CART-014 — Remove All Products

**Requirement:** FR-007
**Scenario:** TS-057
**Priority:** P1

**Expected Result:**
Cart becomes empty after removing all products.

---

## TC-CART-015 — Verify Empty Cart

**Requirement:** FR-007
**Scenario:** TS-059
**Priority:** P2

**Expected Result:**
Appropriate empty-cart message/state is displayed.

---

## TC-CART-016 — Verify Cart During Navigation

**Requirement:** FR-007, FR-012
**Scenario:** TS-060
**Priority:** P1

**Steps:**

1. Add a product.
2. Navigate to another page.
3. Return to cart.

**Expected Result:**
Cart contents remain consistent.

---

## TC-CART-017 — Verify Cart-to-Checkout Transition

**Requirement:** FR-007, FR-009
**Scenario:** TS-068
**Priority:** P1

**Expected Result:**
User can proceed from cart to checkout.

---

## TC-CART-018 — Verify Cart Information Matches Checkout

**Requirement:** FR-007, FR-009
**Scenario:** TS-069
**Priority:** P1

**Expected Result:**
Product, quantity and price information remains consistent between cart and checkout.

---

# 11. Authentication

## TC-AUTH-001 — Verify Login Interface

**Requirement:** FR-008
**Scenario:** TS-061
**Priority:** P1

**Expected Result:**
Login interface is displayed correctly.

---

## TC-AUTH-002 — Login With Valid Credentials

**Requirement:** FR-008
**Scenario:** TS-062
**Priority:** P1

**Test Data:** Valid application-supported credentials.

**Expected Result:**
Valid credentials authenticate successfully.

---

## TC-AUTH-003 — Login With Invalid Credentials

**Requirement:** FR-008
**Scenario:** TS-063
**Priority:** P1

**Test Data:** Invalid credentials.

**Expected Result:**
Login attempt is rejected and appropriate feedback is displayed.

---

## TC-AUTH-004 — Login With Incorrect Password

**Requirement:** FR-008
**Scenario:** TS-064
**Priority:** P1

**Test Data:** Valid username with incorrect password.

**Expected Result:**
Authentication fails.

---

## TC-AUTH-005 — Login With Empty Username

**Requirement:** FR-008
**Scenario:** TS-065
**Priority:** P1

**Expected Result:**
Application validates the required username field.

---

## TC-AUTH-006 — Login With Empty Password

**Requirement:** FR-008
**Scenario:** TS-065
**Priority:** P1

**Expected Result:**
Application validates the required password field.

---

## TC-AUTH-007 — Login With Both Fields Empty

**Requirement:** FR-008
**Scenario:** TS-065
**Priority:** P1

**Expected Result:**
Appropriate validation is displayed and authentication does not occur.

---

## TC-AUTH-008 — Verify Authentication State

**Requirement:** FR-008
**Scenario:** TS-066
**Priority:** P1

**Expected Result:**
Authenticated state is maintained correctly during the expected workflow.

---

## TC-AUTH-009 — Verify Logout

**Requirement:** FR-008, FR-012
**Scenario:** TS-067
**Priority:** P1

**Expected Result:**
User is logged out successfully.

---

## TC-AUTH-010 — Verify Login After Logout

**Requirement:** FR-008, FR-012
**Scenario:** TS-067
**Priority:** P1

**Steps:**

1. Login.
2. Logout.
3. Attempt to access the login flow again.

**Expected Result:**
User can authenticate again using valid credentials.

---

# 12. Checkout

## TC-CHECKOUT-001 — Navigate From Cart to Checkout

**Requirement:** FR-009
**Scenario:** TS-068
**Priority:** P1

**Expected Result:**
Checkout page opens successfully.

---

## TC-CHECKOUT-002 — Verify Checkout Product Name

**Requirement:** FR-009
**Scenario:** TS-069
**Priority:** P1

**Expected Result:**
Correct product name is displayed.

---

## TC-CHECKOUT-003 — Verify Checkout Quantity

**Requirement:** FR-009
**Scenario:** TS-069
**Priority:** P1

**Expected Result:**
Correct product quantity is displayed.

---

## TC-CHECKOUT-004 — Verify Checkout Price

**Requirement:** FR-009
**Scenario:** TS-069
**Priority:** P1

**Expected Result:**
Correct product price is displayed.

---

## TC-CHECKOUT-005 — Verify Checkout Total

**Requirement:** FR-009
**Scenario:** TS-070
**Priority:** P1

**Expected Result:**
Checkout total matches the expected cart total.

---

## TC-CHECKOUT-006 — Submit Valid Customer Information

**Requirement:** FR-009
**Scenario:** TS-071
**Priority:** P1

**Test Data:** Valid customer information.

**Expected Result:**
Valid customer information is accepted.

---

## TC-CHECKOUT-007 — Validate Required Customer Fields

**Requirement:** FR-009
**Scenario:** TS-072
**Priority:** P1

**Expected Result:**
Required fields are clearly identified and validated.

---

## TC-CHECKOUT-008 — Submit Invalid Customer Information

**Requirement:** FR-009
**Scenario:** TS-073
**Priority:** P1

**Test Data:** Invalid customer input.

**Expected Result:**
Invalid information is rejected appropriately.

---

## TC-CHECKOUT-009 — Submit Empty Required Fields

**Requirement:** FR-009
**Scenario:** TS-074
**Priority:** P1

**Expected Result:**
Checkout cannot be completed when required information is missing.

---

## TC-CHECKOUT-010 — Verify Checkout Validation Messages

**Requirement:** FR-009, FR-011
**Scenario:** TS-075
**Priority:** P2

**Expected Result:**
Validation messages are understandable and displayed near the relevant input where applicable.

---

## TC-CHECKOUT-011 — Verify Checkout Retains Cart Data

**Requirement:** FR-009
**Scenario:** TS-069
**Priority:** P1

**Expected Result:**
Checkout retains correct products, quantities and prices.

---

## TC-CHECKOUT-012 — Verify Successful Checkout

**Requirement:** FR-009
**Scenario:** TS-076
**Priority:** P1

**Expected Result:**
Valid checkout completes successfully.

---

## TC-CHECKOUT-013 — Verify Order Confirmation

**Requirement:** FR-009
**Scenario:** TS-077
**Priority:** P1

**Expected Result:**
Appropriate order confirmation is displayed.

---

## TC-CHECKOUT-014 — Verify Invalid Data Prevents Completion

**Requirement:** FR-009, FR-010
**Scenario:** TS-083
**Priority:** P1

**Expected Result:**
Invalid required information prevents successful order completion.

---

## TC-CHECKOUT-015 — Verify Checkout Navigation

**Requirement:** FR-009
**Scenario:** TS-068
**Priority:** P2

**Steps:**

1. Open checkout.
2. Navigate according to available controls.

**Expected Result:**
Checkout navigation works correctly without unexpected loss of information.

---

# 13. End-to-End Purchase

## TC-E2E-001 — Complete Single Product Purchase

**Requirement:** FR-010
**Scenario:** TS-078
**Priority:** P1

**Steps:**

1. Open BStackDemo.
2. Select a product.
3. Add it to cart.
4. Open cart.
5. Proceed to checkout.
6. Authenticate if required.
7. Enter valid customer information.
8. Complete the purchase.

**Expected Result:**
Complete purchase flow succeeds and appropriate confirmation is displayed.

---

## TC-E2E-002 — Purchase Product Using Search

**Requirement:** FR-010
**Scenario:** TS-079
**Priority:** P1

**Steps:**

1. Search for a product.
2. Select the product.
3. Add it to cart.
4. Complete checkout.

**Expected Result:**
Product discovered through search can be successfully purchased.

---

## TC-E2E-003 — Purchase Product Using Filters

**Requirement:** FR-010
**Scenario:** TS-080
**Priority:** P1

**Steps:**

1. Apply a valid product filter.
2. Select a product.
3. Add it to cart.
4. Complete checkout.

**Expected Result:**
Filtered product can complete the purchase flow successfully.

---

## TC-E2E-004 — Purchase Multiple Products

**Requirement:** FR-010
**Scenario:** TS-081
**Priority:** P1

**Steps:**

1. Add multiple products to cart.
2. Review cart.
3. Proceed to checkout.
4. Complete purchase.

**Expected Result:**
All selected products are correctly represented and purchase completes successfully.

---

## TC-E2E-005 — Purchase After Cart Modification

**Requirement:** FR-010
**Scenario:** TS-082
**Priority:** P1

**Steps:**

1. Add multiple products.
2. Remove one product.
3. Modify remaining cart data where supported.
4. Complete checkout.

**Expected Result:**
Only the final intended cart contents are used for checkout.

---

## TC-E2E-006 — Invalid Checkout Prevents Purchase

**Requirement:** FR-009, FR-010
**Scenario:** TS-083
**Priority:** P1

**Expected Result:**
Invalid checkout information prevents successful order completion.

---

## TC-E2E-007 — Verify Product/Price Consistency Across E2E Flow

**Requirement:** FR-010
**Scenario:** TS-078
**Priority:** P1

**Steps:**

1. Note product information in listing.
2. Add product to cart.
3. Open checkout.
4. Compare product information.

**Expected Result:**
Product name, quantity and price remain consistent throughout the workflow.

---

## TC-E2E-008 — Verify Order Confirmation After Purchase

**Requirement:** FR-010
**Scenario:** TS-078
**Priority:** P1

**Expected Result:**
Successful purchase produces an appropriate order confirmation.

---

# 14. UI & Usability

## TC-UI-001 — Verify Overall Page Layout

**Requirement:** FR-011
**Scenario:** TS-084
**Priority:** P3

**Expected Result:**
Page layout is organized, readable and consistent.

---

## TC-UI-002 — Verify Button Visibility

**Requirement:** FR-011
**Scenario:** TS-085
**Priority:** P3

**Expected Result:**
Important buttons are visible and distinguishable.

---

## TC-UI-003 — Verify Button Labels

**Requirement:** FR-011
**Scenario:** TS-085
**Priority:** P3

**Expected Result:**
Button labels clearly communicate their purpose.

---

## TC-UI-004 — Verify Form Labels and Inputs

**Requirement:** FR-011
**Scenario:** TS-086
**Priority:** P3

**Expected Result:**
Form fields have understandable labels/placeholders and are usable.

---

## TC-UI-005 — Verify Validation Message Readability

**Requirement:** FR-011
**Scenario:** TS-087
**Priority:** P3

**Expected Result:**
Validation messages are readable and understandable.

---

## TC-UI-006 — Verify Product Card Consistency

**Requirement:** FR-011
**Scenario:** TS-088
**Priority:** P3

**Expected Result:**
Product cards have consistent visual structure.

---

## TC-UI-007 — Verify Responsive Layout

**Requirement:** FR-011
**Scenario:** TS-089
**Priority:** P2

**Steps:**

1. Open application at desktop size.
2. Resize to a smaller supported viewport.
3. Observe layout.

**Expected Result:**
Application remains usable without major layout issues.

---

## TC-UI-008 — Verify UI Consistency Across Major Pages

**Requirement:** FR-011
**Scenario:** TS-084
**Priority:** P3

**Expected Result:**
Major pages maintain consistent visual design and interaction patterns.

---

# 15. Session & Error Handling

## TC-SESSION-001 — Verify Session After Logout

**Requirement:** FR-012
**Scenario:** TS-090
**Priority:** P1

**Expected Result:**
Logout terminates the authenticated session according to expected application behavior.

---

## TC-SESSION-002 — Verify Session After Page Refresh

**Requirement:** FR-012
**Scenario:** TS-091
**Priority:** P1

**Steps:**

1. Establish the applicable application session.
2. Refresh the page.

**Expected Result:**
Application handles the session and page state correctly.

---

## TC-SESSION-003 — Verify Browser Back After Logout

**Requirement:** FR-012
**Scenario:** TS-092
**Priority:** P1

**Steps:**

1. Login.
2. Logout.
3. Press browser Back.

**Expected Result:**
Application does not incorrectly restore an authenticated state.

---

## TC-SESSION-004 — Verify Invalid Input Handling

**Requirement:** FR-012
**Scenario:** TS-093
**Priority:** P1

**Test Data:** Invalid/special-character input.

**Expected Result:**
Invalid input is handled gracefully without application failure.

---

## TC-SESSION-005 — Verify Empty State Handling

**Requirement:** FR-012
**Scenario:** TS-094
**Priority:** P2

**Expected Result:**
Appropriate empty-state information is displayed.

---

## TC-SESSION-006 — Verify Invalid Navigation Handling

**Requirement:** FR-012
**Scenario:** TS-095
**Priority:** P2

**Expected Result:**
Unexpected or invalid navigation is handled gracefully.

---

## TC-SESSION-007 — Verify Application State Consistency

**Requirement:** FR-012
**Scenario:** TS-096
**Priority:** P1

**Steps:**

1. Browse products.
2. Add a product to cart.
3. Navigate between major pages.
4. Return to cart.

**Expected Result:**
Application state remains consistent during normal navigation.

---

# 16. Complete Test Case Index

| Range                             | Module                   |   Count |
| --------------------------------- | ------------------------ | ------: |
| TC-NAV-001 – TC-NAV-010           | Homepage & Navigation    |      10 |
| TC-PROD-001 – TC-PROD-012         | Product Listing          |      12 |
| TC-SEARCH-001 – TC-SEARCH-010     | Product Search           |      10 |
| TC-FILTER-001 – TC-FILTER-012     | Product Filtering        |      12 |
| TC-SORT-001 – TC-SORT-008         | Product Sorting          |       8 |
| TC-DETAIL-001 – TC-DETAIL-010     | Product Details          |      10 |
| TC-CART-001 – TC-CART-018         | Shopping Cart            |      18 |
| TC-AUTH-001 – TC-AUTH-010         | Authentication           |      10 |
| TC-CHECKOUT-001 – TC-CHECKOUT-015 | Checkout                 |      15 |
| TC-E2E-001 – TC-E2E-008           | End-to-End Purchase      |       8 |
| TC-UI-001 – TC-UI-008             | UI & Usability           |       8 |
| TC-SESSION-001 – TC-SESSION-007   | Session & Error Handling |       7 |
| **TOTAL**                         |                          | **128** |

---

# 17. Priority Distribution

The test suite contains a mixture of P1, P2 and P3 test cases.

### P1 — High Priority

Covers business-critical functionality such as:

* Product selection
* Cart
* Cart calculations
* Authentication
* Checkout
* Purchase flow
* Session behavior

### P2 — Medium Priority

Covers important supporting functionality such as:

* Search variations
* Filters
* Navigation
* Product information
* Responsive behavior

### P3 — Lower Priority

Covers usability and cosmetic validation such as:

* Layout
* Visual consistency
* Labels
* Readability

---

# 18. Execution Status

All test cases initially have the following status:

**NOT EXECUTED**

Actual execution results will be recorded in:

`06-Test-Execution/Test_Execution.md`

No simulated PASS/FAIL result should be added to this document.

---

# 19. Defect Traceability

When a test case fails, the corresponding defect will reference the test case ID.

Example:

```text
TC-CART-011
      ↓
BUG-001
```

This allows direct traceability:

```text
Requirement
    ↓
Scenario
    ↓
Test Case
    ↓
Defect
    ↓
Retest
    ↓
Regression
```

---

# 20. Document Control

| Version | Date       | Description                    |
| ------- | ---------- | ------------------------------ |
| 1.0     | 2026-10-07 | Initial 128-test-case baseline |

---

**End of Test Cases Document**
