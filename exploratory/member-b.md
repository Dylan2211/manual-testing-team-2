# Self-Designed Testing — Member B

## Testing Idea

How does the Test Pages validation form enforce **name lengths**, and does what it enforces match the published requirements?

I started with the surname length range. While setting up, the team's agreed baseline was rejected, so I changed direction to investigate the first-name rule as well (see *Change of Direction*).

## Reason

As Member B (requirements and baseline), my job is to check the published requirements and the baseline the team relies on. Name-length rules are easy to get wrong at the edges, and the site notes that the client-side and server-side checks may not match.

## Test Basis

Published requirements from the [validation instructions](https://testpages.eviltester.com/apps/client-server-form-validation/client-server-form-validation-instructions/), checked on 8 November 2026:

- First name must be filled and must be less than 90 characters.
- Surname should be between 11 and 79 characters.

Assumptions and questions:

- Assumption: "between 11 and 79" is inclusive, the same way the age range 18–80 is treated in this practical.
- Question: the requirements give no minimum first-name length beyond "must be filled", so any first name of 1 character or more should be accepted.

## Approach

- Change one field at a time and keep every other field at a value that the form accepts.
- Surname: 2-point boundary testing at both transitions (10/11 and 79/80). Surnames are built by repeating `Testingstudent` and cutting to the exact length.
- First name: start from the baseline `Alex`, then try shorter and longer names to find where the form changes its decision.
- Record whether a rejection came from the browser (message under the field, no page change) or from the server (the `Validation Report` on the `/submit` page).

## Change of Direction

My planned surname tests used the team baseline first name `Alex`. A baseline check rejected it on the server with **"Firstname too short"**, even though the published requirement only says the first name must be filled. I paused the surname tests, investigated the first-name rule (OWN-B-05 to OWN-B-09), then ran the surname tests with the 5-character first name `Alexa`, which the form accepts.

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-b |
| Date and time | 8 November 2026, 16:45–16:55 (UTC+8) |
| Browser and version | Chromium 152 (Claude desktop built-in browser) |
| Operating system | Windows 11 |

## Test Cases

### Test ID: OWN-B-01

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Pass |

#### Purpose

Check that a surname one character below the minimum of 11 is rejected.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alexa` |
| Surname | `Testingstu` (10 characters) |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the surname is `Testingstu`.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

The surname is rejected because 10 characters is below the minimum of 11.

#### Actual Result

The browser blocked the submission. The message **"Surname provided is too short"** appeared under the Last name field and the page did not change to the results page.

#### Evidence

Not captured. Written result only.

---

### Test ID: OWN-B-02

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Pass |

#### Purpose

Check that a surname at the minimum of 11 characters is accepted.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alexa` |
| Surname | `Testingstud` (11 characters) |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the surname is `Testingstud`.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

The surname is accepted, assuming the range is inclusive.

#### Actual Result

The form submitted. The Validation Report showed **"Valid Input — Your Input passed validation"** and listed the surname `Testingstud`.

#### Evidence

Not captured. Written result only.

---

### Test ID: OWN-B-03

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Pass |

#### Purpose

Check that a surname at the maximum of 79 characters is accepted.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alexa` |
| Surname | `TestingstudentTestingstudentTestingstudentTestingstudentTestingstudentTestingst` (79 characters) |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the surname is the 79-character value.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

The surname is accepted, assuming the range is inclusive.

#### Actual Result

The form submitted. The Validation Report showed **"Valid Input — Your Input passed validation"** and listed the full 79-character surname.

#### Evidence

Not captured. Written result only.

---

### Test ID: OWN-B-04

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Pass |

#### Purpose

Check that a surname one character above the maximum of 79 is rejected.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alexa` |
| Surname | `TestingstudentTestingstudentTestingstudentTestingstudentTestingstudentTestingstu` (80 characters) |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the surname is the 80-character value.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

The surname is rejected because 80 characters is above the maximum of 79.

#### Actual Result

The browser blocked the submission. The message **"Surname provided is too long"** appeared under the Last name field. The field still contained all 80 characters, so the field itself does not cut the input short.

#### Evidence

Not captured. Written result only.

---

### Test ID: OWN-B-05

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Status | Fail |

#### Purpose

Check the team's agreed baseline, which uses the first name `Alex`.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alex` (4 characters) |
| Surname | `TestingStudent` |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the first name is `Alex`.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

Accepted. The published requirement only says the first name must be filled and be under 90 characters.

#### Actual Result

The browser allowed the submission, but the server rejected it. The Validation Report showed **"Firstname Error — Firstname too short"**. I repeated this once and got the same result.

#### Evidence

[View screenshot](../evidence/member-b/own-b-05-firstname-alex.jpg)

---

### Test ID: OWN-B-06

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Status | Pass |

#### Purpose

Check whether a 5-character first name is accepted.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alexa` |
| Surname | `TestingStudent` |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the first name is `Alexa`.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

Accepted, based on the published requirement.

#### Actual Result

The form submitted. The Validation Report showed **"Valid Input — Your Input passed validation"**.

#### Evidence

[View screenshot](../evidence/member-b/own-b-06-firstname-alexa.jpg)

---

### Test ID: OWN-B-07

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Status | Fail |

#### Purpose

Check whether the shortest filled first name (1 character) is accepted.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `A` (1 character) |
| Surname | `TestingStudent` |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the first name is `A`.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

Accepted, because the requirement only says the first name must be filled.

#### Actual Result

The browser blocked the submission. The message **"Firstname provided is too short"** appeared under the First name field and the page did not change to the results page.

#### Evidence

[View screenshot](../evidence/member-b/own-b-07-firstname-a.jpg)

---

### Test ID: OWN-B-08

| Item | Details |
|---|---|
| Test type | Exploratory |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Status | Observation only |

#### Purpose

Find where the browser's first-name check changes its decision.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Al` (2 characters) |
| Surname | `TestingStudent` |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the first name is `Al`.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

Unclear. This test locates the browser's minimum, so it is recorded as an observation.

#### Actual Result

The browser blocked the submission with **"Firstname provided is too short"**.

#### Evidence

Not captured. Written result only.

---

### Test ID: OWN-B-09

| Item | Details |
|---|---|
| Test type | Exploratory |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Status | Observation only |

#### Purpose

Find where the browser's first-name check changes its decision.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Ale` (3 characters) |
| Surname | `TestingStudent` |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the first name is `Ale`.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

Unclear. This test locates the browser's minimum, so it is recorded as an observation.

#### Actual Result

The browser allowed the submission, but the server rejected it with **"Firstname Error — Firstname too short"**.

#### Evidence

Not captured. Written result only.

---

### Test ID: OWN-B-10

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Pass |

#### Purpose

Follow-up: re-run my guided age-18 test with a first name the server accepts.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alexa` |
| Surname | `TestingStudent` |
| Age | `18` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the age is `18`.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

Age 18 is accepted because it is the minimum of the 18–80 range.

#### Actual Result

The form submitted. The Validation Report showed **"Valid Input — Your Input passed validation"** with age `18`.

#### Evidence

Not captured. Written result only.

---

### Test ID: OWN-B-11

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 3-point boundary testing |
| Status | Pass |

#### Purpose

Follow-up: re-run my guided age-19 test with a first name the server accepts.

#### Preconditions

- The validation form is open in a fresh page load.
- Every field not listed as changed uses the values below.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alexa` |
| Surname | `TestingStudent` |
| Age | `19` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Type the values from the test data table into each field.
3. Check that the age is `19`.
4. Select `Submit`.
5. Observe the message shown and the page reached.

#### Expected Result

Age 19 is accepted because it is inside the 18–80 range.

#### Actual Result

The form submitted. The Validation Report showed **"Valid Input — Your Input passed validation"** with age `19`.

#### Evidence

Not captured. Written result only.

---

## Overall Observations

- **Surname:** the 11–79 range is inclusive. 10 and 80 characters were blocked in the browser, and 11 and 79 were accepted. This matches the published requirement.
- **First name:** the form enforces a minimum length that the published requirements do not mention, and the browser and server disagree about it:

| First name length | Browser check | Server check |
|---:|---|---|
| 1–2 | Blocked: "Firstname provided is too short" | Not reached |
| 3–4 | Allowed | Rejected: "Firstname too short" |
| 5 | Allowed | Accepted |

- **Impact on the team:** the agreed baseline first name `Alex` (4 characters) is rejected by the server. Any test that used `Alex` was rejected for the first name, whatever the age. My guided records for ages 18 and 19 show this in their screenshots, and OWN-B-10 and OWN-B-11 re-ran those ages with `Alexa`.
- I am not calling this a confirmed defect. The 5-character minimum may be an intended rule that is missing from the published requirements. Either way, the browser and server rules do not match each other.

## Next Question

- What is the first-name maximum? The requirement says under 90 characters, so 89 and 90 characters are the next tests.
- Should the team change the baseline first name to one with 5 or more characters, then re-run the other members' accepted-age tests (30, 80 and 79)?
