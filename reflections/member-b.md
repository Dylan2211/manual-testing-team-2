# Individual Reflection — Member B

## 1. What makes a test positive or negative?

The input decides it. A positive test uses valid input that should be accepted, such as age `18`, and a negative test uses invalid input that should be rejected, such as `wrong_password` or age `10`.

## 2. Why can a negative test pass?

A negative test passes when the application rejects the invalid input as expected. In LOGIN-N01 the login was refused with an error message, so the test passed even though the login itself failed.

## 3. How did equivalence partitioning help you select data?

It split age into three groups (below 18, 18–80 and above 80), so one value from each group was enough. My value `10` stood for the whole below-18 group.

## 4. What did boundary testing help you investigate?

It focused my tests on the edges where mistakes are most likely, such as 18 and 19 for age, and 10, 11, 79 and 80 characters for surname. The surname tests showed that "between 11 and 79" is inclusive.

## 5. What did you choose to test during the open-ended activity, and why?

I tested name-length rules on the validation form, because my role was to check the requirements and baseline. I wanted to know whether the surname range was inclusive and whether the form matched the published rules.

## 6. Did your observations lead to follow-up tests?

Yes. The baseline first name `Alex` was rejected by the server, so I tested shorter and longer first names and found that the browser needs 3 characters while the server needs 5. I then re-ran my age 18 and 19 tests with `Alexa`, because my original runs had been blocked by the first name without my noticing.

## 7. How does your Git history show your contribution?

My commits on `testing/member-b` show my guided results, the planned self-designed tests committed before they were run, the executed results with evidence, and a correction to my earlier statuses. The correction is kept as its own commit rather than hidden, so the history shows what changed and why.
