# Self-Designed Testing — Member D

## Testing Idea

Investigate whether the SauceDemo shopping cart updates correctly when multiple products are added and one product is removed.

## Reason

I want to check whether the shopping cart displays the correct number of products and whether the correct products remain in the cart after removing an item.

This is useful because users should be able to add and remove products without the cart displaying incorrect information.

## Test Basis

The investigation is based on the expected shopping cart behaviour.

The practical does not provide a specific acceptance criterion for this additional scenario. Therefore, the expected behaviour is treated as an assumption based on the visible shopping cart functionality.

## Approach

1. Log in using the standard demonstration account.
2. Add two different products to the shopping cart.
3. Observe the shopping cart badge.
4. Open the shopping cart and check the products displayed.
5. Remove one product.
6. Check whether the cart badge and product list update correctly.

## Test Cases

### Test ID: OWN-D-01

| Item | Details |
|---|---|
| Test type | Exploratory |
| Tester | member-d |
| Website | [SauceDemo](https://www.saucedemo.com/) |
| Status | Not run |

#### Purpose

To investigate whether the shopping cart correctly displays multiple added products and updates when one product is removed.

#### Preconditions

- The SauceDemo login page is open.
- The user is logged out.
- The standard demonstration account is available.

#### Test Data

| Field | Value |
|---|---|
| Username | `standard_user` |
| Password | `secret_sauce` |
| First product | Sauce Labs Backpack |
| Second product | Sauce Labs Bike Light |

#### Steps

1. Open the SauceDemo website.
2. Enter the username `standard_user`.
3. Enter the password `secret_sauce`.
4. Select Login.
5. Confirm that the inventory page is displayed.
6. Add Sauce Labs Backpack to the cart.
7. Add Sauce Labs Bike Light to the cart.
8. Observe the shopping cart badge.
9. Open the shopping cart.
10. Check whether both products are displayed.
11. Remove Sauce Labs Backpack.
12. Observe the shopping cart badge again.
13. Check whether only Sauce Labs Bike Light remains in the cart.

#### Expected Result

Based on the assumed shopping cart behaviour:

- Both products should appear in the cart after being added.
- The shopping cart badge should display `2`.
- After removing Sauce Labs Backpack, only Sauce Labs Bike Light should remain.
- The shopping cart badge should update to `1`.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

## Overall Observations

To be completed after executing the test.

Record whether the shopping cart badge and product list updated correctly after adding and removing products.

Also record any unexpected behaviour or unclear requirements.

## Next Question

To be completed after executing the test.

A possible follow-up question is whether the shopping cart retains its products when the user navigates back to the inventory page and then returns to the cart.