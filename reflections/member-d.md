# Individual Reflection — Member D

## 1. What makes a test positive or negative?

A positive test checks whether the system accepts valid input and behaves as expected.

A negative test checks whether the system correctly handles invalid input, such as missing information, incorrect passwords or values outside the allowed range.

For example, entering a valid age of `30` is a positive test because it should be accepted. Entering an age of `90` is a negative test because it is above the allowed maximum of `80` and should be rejected.

## 2. Why can a negative test pass?

A negative test can pass when the system correctly rejects invalid input and displays the expected error message.

For example, in my `LOGIN-N03` test, I left the username field empty and entered a valid password.

The system rejected the login attempt and displayed the message `Epic sadface: Username is required`.

The test passed because the actual result matched the expected result, even though the login attempt was unsuccessful.

## 3. How did equivalence partitioning help you select data?

Equivalence partitioning helped me divide the age input into groups that should behave similarly.

The age requirement was between `18` and `80`, inclusive.

I identified three partitions:

- Below 18: Invalid partition, represented by `10`.
- Between 18 and 80: Valid partition, represented by `30`.
- Above 80: Invalid partition, represented by `90`.

Instead of testing every possible age, I could select representative values from each partition.

I also investigated blank and non-numeric inputs such as `abc` to observe how the form handled different input formats.

## 4. What did boundary testing help you investigate?

Boundary testing helped me investigate what happens at the limits of the allowed age range.

The valid age range was `18` to `80`, inclusive.

The important boundary values were:

- `17`: Immediately below the minimum.
- `18`: Minimum valid age.
- `80`: Maximum valid age.
- `81`: Immediately above the maximum.

I performed the test for age `81` and also tested `82` as an additional value for 3-point boundary testing.

The form rejected both `81` and `82` and displayed the message `Please select a value that is no more than 80.`

This helped me understand how boundary testing checks values around the limits, rather than only testing a normal valid value.

## 5. What did you choose to test during the open-ended activity, and why?

For the self-designed testing activity, I chose to investigate the SauceDemo shopping cart.

My test was whether the shopping cart correctly displays multiple products when they are added and updates when one product is removed.

I chose this because shopping carts are an important part of online shopping. Users should be able to add and remove products while seeing the correct products and item count.

I added Sauce Labs Backpack and Sauce Labs Bike Light. I then removed Sauce Labs Backpack and checked whether the remaining product and cart badge were displayed correctly.

## 6. Did your observations lead to follow-up tests?

Yes. During my shopping cart investigation, the cart badge and product list updated correctly after adding and removing products.

This made me think of another question: Does the shopping cart retain its products when the user navigates back to the inventory page and then returns to the cart?

I identified this as a possible follow-up test. It would help investigate whether the cart maintains its contents when navigating between pages.

This follow-up test has not yet been executed.

## 7. How does your Git history show your contribution?

My Git history shows my individual contribution through the commits I made to the team's repository.

I contributed my assigned login test, age validation results, boundary testing results, self-designed shopping cart test, screenshots and individual reflection.

I worked on my own branch and pushed my changes to GitHub through commits and a pull request.

This allows the team to identify my changes and see the work I contributed to the project.