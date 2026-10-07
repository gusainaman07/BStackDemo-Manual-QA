# BStackDemo Manual QA Testing – Bug Reports

## 1. Document Information

| Field          | Details                      |
| -------------- | ---------------------------- |
| Project        | BStackDemo Manual QA Testing |
| Application    | BStackDemo                   |
| Testing Type   | Manual Testing               |
| Defect Type    | Functional / UI / Validation |
| Total Defects  | 10                           |
| Defect Dataset | Simulated Portfolio Defects  |
| Status         | Defects Logged               |
| Version        | 1.0                          |

> **Important:** The defects documented here are **simulated portfolio defects** created to demonstrate a complete manual QA defect-management workflow. They are not claimed to be actual defects currently present in the live BStackDemo application.

---

# 2. Defect Severity Definitions

| Severity      | Definition                                                    |
| ------------- | ------------------------------------------------------------- |
| S1 – Critical | Blocks a core business flow or makes the application unusable |
| S2 – Major    | Important functionality is significantly affected             |
| S3 – Minor    | Functionality works but has a noticeable issue                |
| S4 – Trivial  | Cosmetic or very low-impact issue                             |

---

# 3. Defect Priority Definitions

| Priority    | Definition                                   |
| ----------- | -------------------------------------------- |
| P1 – High   | Should be fixed immediately                  |
| P2 – Medium | Should be fixed in the current release cycle |
| P3 – Low    | Can be fixed in a future release             |

---

# 4. Defect Status Definitions

| Status   | Meaning                               |
| -------- | ------------------------------------- |
| Open     | Defect has been identified and logged |
| Assigned | Defect assigned to a developer        |
| Fixed    | Developer has implemented a fix       |
| Retest   | Fix is ready for QA verification      |
| Reopened | Defect still exists after retesting   |
| Closed   | Fix verified successfully             |

---

# BUG-001 – Add to Cart Does Not Update Cart Correctly

| Field       | Details          |
| ----------- | ---------------- |
| Defect ID   | BUG-001          |
| Test Case   | TC-PROD-006      |
| Module      | Product Listing  |
| Severity    | S2 – Major       |
| Priority    | P1 – High        |
| Type        | Functional       |
| Status      | Open             |
| Environment | Windows + Chrome |
| Dataset     | Simulated        |

### Title

**Add to Cart action does not consistently update the shopping cart**

### Preconditions

1. BStackDemo is accessible.
2. Product listing page is open.
3. At least one product is available.

### Steps to Reproduce

1. Open the BStackDemo product listing.
2. Select an available product.
3. Click **Add to Cart**.
4. Open the shopping cart.
5. Check the selected product and cart count.

### Expected Result

The selected product should be added successfully to the cart and the cart count should update accordingly.

### Simulated Actual Result

The Add to Cart action does not consistently update the cart state immediately.

### Impact

Users may believe that the product was added successfully when the cart does not reflect the action correctly.

### Recommendation

Verify the Add to Cart state transition and ensure the cart count and cart contents are updated consistently.

### Retest Criteria

Repeat the same Add to Cart flow with:

* One product
* Multiple products
* Different product cards
* Navigation away and back to the cart

---

# BUG-002 – No-Result Filter State Is Not Handled Correctly

| Field       | Details           |
| ----------- | ----------------- |
| Defect ID   | BUG-002           |
| Test Case   | TC-FILTER-006     |
| Module      | Product Filtering |
| Severity    | S3 – Minor        |
| Priority    | P2 – Medium       |
| Type        | Functional / UI   |
| Status      | Open              |
| Environment | Windows + Chrome  |
| Dataset     | Simulated         |

### Title

**No-result filter state does not provide clear user feedback**

### Preconditions

Product listing page is open.

### Steps to Reproduce

1. Open the product listing.
2. Apply a filter combination that produces no matching products.
3. Observe the product-listing area.

### Expected Result

The application should clearly communicate that no products match the selected filter criteria.

### Simulated Actual Result

The no-result state is not presented clearly enough to the user.

### Impact

Users may incorrectly assume that the application or filter functionality has stopped working.

### Recommendation

Display a clear empty-state message such as:

> No products found for the selected filters.

### Retest Criteria

Verify:

* No-result filter
* Valid filter
* Reset filter
* Filter followed by search

---

# BUG-003 – Cart Quantity Display Is Inconsistent

| Field       | Details          |
| ----------- | ---------------- |
| Defect ID   | BUG-003          |
| Test Case   | TC-CART-007      |
| Module      | Shopping Cart    |
| Severity    | S2 – Major       |
| Priority    | P1 – High        |
| Type        | Functional       |
| Status      | Open             |
| Environment | Windows + Chrome |
| Dataset     | Simulated        |

### Title

**Cart quantity does not consistently reflect the selected product quantity**

### Preconditions

A product has been added to the shopping cart.

### Steps to Reproduce

1. Add a product to the cart.
2. Open the cart.
3. Increase the product quantity.
4. Observe the displayed quantity.
5. Refresh or navigate within the application.
6. Recheck the quantity.

### Expected Result

The displayed quantity should always match the current cart quantity.

### Simulated Actual Result

The displayed quantity becomes inconsistent after a cart-state change.

### Impact

Incorrect quantity information can result in incorrect order expectations and potentially incorrect totals.

### Recommendation

Ensure the cart quantity is synchronized with the underlying cart state after every quantity update.

### Retest Criteria

Test quantities:

* 1
* 2
* 3
* Multiple products
* Quantity change followed by refresh

---

# BUG-004 – Incorrect Password Handling

| Field       | Details                 |
| ----------- | ----------------------- |
| Defect ID   | BUG-004                 |
| Test Case   | TC-AUTH-004             |
| Module      | Authentication          |
| Severity    | S2 – Major              |
| Priority    | P1 – High               |
| Type        | Functional / Validation |
| Status      | Open                    |
| Environment | Windows + Chrome        |
| Dataset     | Simulated               |

### Title

**Incorrect password scenario does not provide consistent authentication feedback**

### Preconditions

A valid test username is available.

### Steps to Reproduce

1. Open the login page.
2. Enter a valid test username.
3. Enter an incorrect password.
4. Click the Login button.
5. Observe the result.

### Expected Result

Login should fail and a clear authentication error should be displayed.

### Simulated Actual Result

The incorrect-password flow does not consistently provide the expected feedback.

### Impact

Users may be confused about whether authentication succeeded or failed.

### Recommendation

Ensure that invalid password attempts:

* Do not authenticate the user.
* Provide clear feedback.
* Keep the user on the login flow.

### Retest Criteria

Test:

* Valid username + invalid password
* Invalid username + valid password
* Invalid username + invalid password
* Empty password

---

# BUG-005 – Valid Checkout Cannot Be Completed Reliably

| Field       | Details                    |
| ----------- | -------------------------- |
| Defect ID   | BUG-005                    |
| Test Case   | TC-CHECKOUT-012            |
| Module      | Checkout                   |
| Severity    | S1 – Critical              |
| Priority    | P1 – High                  |
| Type        | Functional / Business Flow |
| Status      | Open                       |
| Environment | Windows + Chrome           |
| Dataset     | Simulated                  |

### Title

**Valid checkout flow does not complete successfully**

### Preconditions

1. Product is available.
2. Product has been added to the cart.
3. Valid checkout data is available.

### Steps to Reproduce

1. Add a product to the cart.
2. Open the cart.
3. Proceed to checkout.
4. Enter valid customer information.
5. Submit the checkout form.
6. Observe the result.

### Expected Result

The checkout should complete successfully and the user should receive an order confirmation.

### Simulated Actual Result

The valid checkout flow fails to complete successfully.

### Impact

This is a critical business-flow issue because it can prevent customers from completing purchases.

### Recommendation

Investigate the complete checkout transaction flow and verify:

* Cart state
* Customer information
* Checkout validation
* Order creation
* Confirmation state

### Retest Criteria

Verify:

1. Single-product checkout.
2. Multiple-product checkout.
3. Valid customer data.
4. Checkout after search.
5. Checkout after filtering.
6. Checkout after sorting.

---

# BUG-006 – Product Listing State Incorrect After Sorting

| Field       | Details                   |
| ----------- | ------------------------- |
| Defect ID   | BUG-006                   |
| Test Case   | TC-PROD-010               |
| Module      | Product Listing / Sorting |
| Severity    | S3 – Minor                |
| Priority    | P2 – Medium               |
| Type        | Functional                |
| Status      | Open                      |
| Environment | Windows + Chrome          |
| Dataset     | Simulated                 |

### Title

**Product listing does not consistently reflect the selected sorting option**

### Preconditions

Product listing contains multiple products.

### Steps to Reproduce

1. Open the product listing.
2. Select a sorting option.
3. Observe the product order.
4. Navigate away from the page.
5. Return to the product listing.
6. Check the product order.

### Expected Result

Products should be displayed according to the selected sorting rule.

### Simulated Actual Result

The product order does not consistently match the selected sorting state after navigation.

### Impact

Users may receive unexpected product ordering.

### Recommendation

Synchronize the displayed product list with the selected sorting state.

### Retest Criteria

Test:

* Price ascending
* Price descending
* A-Z
* Z-A
* Sorting after filtering
* Sorting after search

---

# BUG-007 – Cart Total Calculation Is Incorrect

| Field       | Details                  |
| ----------- | ------------------------ |
| Defect ID   | BUG-007                  |
| Test Case   | TC-CART-011              |
| Module      | Shopping Cart            |
| Severity    | S2 – Major               |
| Priority    | P1 – High                |
| Type        | Functional / Calculation |
| Status      | Open                     |
| Environment | Windows + Chrome         |
| Dataset     | Simulated                |

### Title

**Cart total does not consistently equal the sum of product prices and quantities**

### Preconditions

At least one product is present in the cart.

### Steps to Reproduce

1. Add a product to the cart.
2. Note the product price.
3. Change the product quantity.
4. Observe the cart total.
5. Add another product.
6. Compare the displayed total with the expected total.

### Expected Result

The cart total should be calculated correctly based on:

```text
Product Price × Quantity
```

and the sum of all cart items.

### Simulated Actual Result

The displayed cart total does not consistently match the expected calculation after cart changes.

### Impact

Incorrect totals can directly affect the purchase amount displayed to the customer.

### Recommendation

Verify cart calculation logic after:

* Add
* Remove
* Quantity increase
* Quantity decrease
* Multiple-product operations

### Retest Criteria

Execute calculations for:

* One product × 1
* One product × 2
* Multiple products
* Remove one product
* Change quantity

---

# BUG-008 – Checkout Validation Messages Are Inconsistent

| Field       | Details          |
| ----------- | ---------------- |
| Defect ID   | BUG-008          |
| Test Case   | TC-CHECKOUT-010  |
| Module      | Checkout         |
| Severity    | S3 – Minor       |
| Priority    | P2 – Medium      |
| Type        | Validation / UI  |
| Status      | Open             |
| Environment | Windows + Chrome |
| Dataset     | Simulated        |

### Title

**Checkout validation messages are not displayed consistently**

### Preconditions

Checkout form is open.

### Steps to Reproduce

1. Open checkout.
2. Leave one or more required fields empty.
3. Submit the form.
4. Observe validation messages.

### Expected Result

Each invalid or missing required field should provide clear and understandable validation feedback.

### Simulated Actual Result

Validation feedback is inconsistent between fields.

### Impact

Users may not understand which information needs correction.

### Recommendation

Standardize:

* Validation message placement
* Message wording
* Error visibility
* Field highlighting

### Retest Criteria

Test each required field independently and in combination.

---

# BUG-009 – Product Detail Navigation Is Inconsistent

| Field       | Details                 |
| ----------- | ----------------------- |
| Defect ID   | BUG-009                 |
| Test Case   | TC-DETAIL-009           |
| Module      | Product Details         |
| Severity    | S2 – Major              |
| Priority    | P1 – High               |
| Type        | Functional / Navigation |
| Status      | Open                    |
| Environment | Windows + Chrome        |
| Dataset     | Simulated               |

### Title

**Navigation between multiple product-detail views is inconsistent**

### Preconditions

Multiple products are available.

### Steps to Reproduce

1. Open the product listing.
2. Open Product A.
3. Return to the product listing.
4. Open Product B.
5. Navigate back.
6. Observe the resulting product page/state.

### Expected Result

The user should be taken to the correct product page and browser navigation should maintain a predictable state.

### Simulated Actual Result

Navigation state becomes inconsistent when moving between multiple product-detail views.

### Impact

Users may be returned to an unexpected product or page state.

### Recommendation

Verify:

* Product identifiers
* Browser history
* Back navigation
* Product-detail routing
* State restoration

### Retest Criteria

Repeat navigation across at least three different products.

---

# BUG-010 – Application State Becomes Inconsistent

| Field       | Details                       |
| ----------- | ----------------------------- |
| Defect ID   | BUG-010                       |
| Test Case   | TC-SESSION-007                |
| Module      | Session & Error Handling      |
| Severity    | S2 – Major                    |
| Priority    | P1 – High                     |
| Type        | Functional / State Management |
| Status      | Open                          |
| Environment | Windows + Chrome              |
| Dataset     | Simulated                     |

### Title

**Application state is not consistently maintained across navigation/session actions**

### Preconditions

A product or cart state has been established.

### Steps to Reproduce

1. Open BStackDemo.
2. Add a product to the cart.
3. Navigate to another page.
4. Use browser Back/Forward.
5. Refresh the page.
6. Observe the application state.

### Expected Result

The application should maintain a consistent state according to its intended session behavior.

### Simulated Actual Result

The application state does not remain fully consistent after the navigation/session sequence.

### Impact

Inconsistent state can affect:

* Cart contents
* Product selection
* User workflow
* Checkout readiness

### Recommendation

Review state handling across:

* Refresh
* Browser Back
* Browser Forward
* Page navigation
* Session reset

### Retest Criteria

Repeat the workflow using:

* Product state
* Cart state
* Login state
* Refresh
* Browser navigation

---

# 5. Defect Summary

| Defect ID | Module            | Severity | Priority | Status |
| --------- | ----------------- | -------- | -------- | ------ |
| BUG-001   | Product Listing   | S2       | P1       | Open   |
| BUG-002   | Product Filtering | S3       | P2       | Open   |
| BUG-003   | Shopping Cart     | S2       | P1       | Open   |
| BUG-004   | Authentication    | S2       | P1       | Open   |
| BUG-005   | Checkout          | S1       | P1       | Open   |
| BUG-006   | Product Listing   | S3       | P2       | Open   |
| BUG-007   | Shopping Cart     | S2       | P1       | Open   |
| BUG-008   | Checkout          | S3       | P2       | Open   |
| BUG-009   | Product Details   | S2       | P1       | Open   |
| BUG-010   | Session Handling  | S2       | P1       | Open   |

---

# 6. Severity Summary

| Severity      |  Count |
| ------------- | -----: |
| S1 – Critical |      1 |
| S2 – Major    |      6 |
| S3 – Minor    |      3 |
| S4 – Trivial  |      0 |
| **Total**     | **10** |

---

# 7. Priority Summary

| Priority    |  Count |
| ----------- | -----: |
| P1 – High   |      7 |
| P2 – Medium |      3 |
| P3 – Low    |      0 |
| **Total**   | **10** |

---

# 8. Defect Lifecycle

The expected defect workflow is:

```text
Open
  ↓
Assigned
  ↓
Fixed
  ↓
Retest
  ↓
 ┌───────────────┐
 │               │
PASS           FAIL
 │               │
 ↓               ↓
Closed        Reopened
                 │
                 └──→ Developer Fix
```

---

# 9. Retesting Strategy

After a defect is marked **Fixed**, QA should execute the original failed test case again.

For example:

```text
BUG-001
   ↓
Developer Fix
   ↓
Retest TC-PROD-006
   ↓
PASS → Close BUG-001
FAIL → Reopen BUG-001
```

Retesting confirms that the specific defect has been resolved.

Regression testing is then required to make sure the fix did not negatively affect related functionality.

---

# 10. Defect-to-Test Case Traceability

| Defect  | Failed Test Case | Retest Required |
| ------- | ---------------- | --------------- |
| BUG-001 | TC-PROD-006      | Yes             |
| BUG-002 | TC-FILTER-006    | Yes             |
| BUG-003 | TC-CART-007      | Yes             |
| BUG-004 | TC-AUTH-004      | Yes             |
| BUG-005 | TC-CHECKOUT-012  | Yes             |
| BUG-006 | TC-PROD-010      | Yes             |
| BUG-007 | TC-CART-011      | Yes             |
| BUG-008 | TC-CHECKOUT-010  | Yes             |
| BUG-009 | TC-DETAIL-009    | Yes             |
| BUG-010 | TC-SESSION-007   | Yes             |

---

# 11. QA Recommendation

The simulated defect set contains one critical defect and multiple high-priority functional defects affecting:

* Shopping cart
* Checkout
* Authentication
* Product navigation
* Application state

Therefore, the recommended action is:

**HOLD RELEASE**

The defects should be resolved, retested, and followed by regression testing before release approval.

---

