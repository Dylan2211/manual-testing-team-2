# Self-Designed Testing — Member B

## Testing Idea

Investigate how the Test Pages validation form handles surname length at the edges of its stated range.

## Reason

As Member B (requirements and baseline), I noticed the published requirement says the surname "should be between 11 and 79 chars". "Between" does not say whether 11 and 79 themselves are allowed, so the boundaries are worth checking. The surname field also has no HTML `minlength` or `maxlength` attribute, unlike age (`min=18`, `max=80`), so any length check must come from JavaScript or the server.

## Test Basis

- Requirement from the [validation instructions](https://testpages.eviltester.com/apps/client-server-form-validation/client-server-form-validation-instructions/): surname should be between 11 and 79 characters.
- Assumption: the range is inclusive (11 ≤ length ≤ 79), the same way the age range 18–80 is treated as inclusive in this practical.
- Requirement question: is the range inclusive or exclusive? The tests below should show how the form actually treats it.

## Approach

- Apply 2-point boundary testing to surname length: 10 and 11 at the lower transition, 79 and 80 at the upper transition.
- Use the agreed baseline from `team-plan.md` for every other field and change only the surname.
- Surnames are built by repeating `Testingstudent` and cutting it to the exact length, so the character count is easy to check.

## Test Cases

### Test ID: OWN-B-01

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Not run |

#### Purpose

Check how a surname of 10 characters is handled: one character below the minimum of 11.

#### Preconditions

- The validation form is open in a new page load.
- All other fields use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alex` |
| Surname | `Testingstu` (10 characters) |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Enter the agreed baseline.
3. Replace the surname with the 10-character value above.
4. Select `Submit`.
5. Observe any feedback and the page reached.

#### Expected Result

The surname is rejected with surname-length feedback.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

### Test ID: OWN-B-02

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Not run |

#### Purpose

Check how a surname of 11 characters is handled: the minimum of 11, if the range is inclusive.

#### Preconditions

- The validation form is open in a new page load.
- All other fields use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alex` |
| Surname | `Testingstud` (11 characters) |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Enter the agreed baseline.
3. Replace the surname with the 11-character value above.
4. Select `Submit`.
5. Observe any feedback and the page reached.

#### Expected Result

The surname is accepted, and the submitted surname is shown.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

### Test ID: OWN-B-03

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Not run |

#### Purpose

Check how a surname of 79 characters is handled: the maximum of 79, if the range is inclusive.

#### Preconditions

- The validation form is open in a new page load.
- All other fields use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alex` |
| Surname | `TestingstudentTestingstudentTestingstudentTestingstudentTestingstudentTestingst` (79 characters) |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Enter the agreed baseline.
3. Replace the surname with the 79-character value above.
4. Select `Submit`.
5. Observe any feedback and the page reached.

#### Expected Result

The surname is accepted, and the submitted surname is shown.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

### Test ID: OWN-B-04

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Not run |

#### Purpose

Check how a surname of 80 characters is handled: one character above the maximum of 79.

#### Preconditions

- The validation form is open in a new page load.
- All other fields use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alex` |
| Surname | `TestingstudentTestingstudentTestingstudentTestingstudentTestingstudentTestingstu` (80 characters) |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Enter the agreed baseline.
3. Replace the surname with the 80-character value above.
4. Select `Submit`.
5. Observe any feedback and the page reached.

#### Expected Result

The surname is rejected with surname-length feedback.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

## Overall Observations

Not recorded — tests have not been executed.

## Next Question

To be decided after execution.
