# Manual Testing Results — Member C

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-c |
| Date and time | 3 Nov 2026, 2:45 pm SGT |
| Browser and version | Chrome 142.0.xxxx |
| Operating system | Windows 11 |

---

## Login Tests

### Test ID: LOGIN-N02

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-c |
| Website | SauceDemo |
| Status | Not run |

#### Purpose

Check that a login attempt with a valid username and an empty password is rejected.

#### Preconditions

- The SauceDemo login page is open: https://www.saucedemo.com/
- The user is logged out.
- Both input fields are empty.

#### Test Data

| Field | Value |
|---|---|
| Username | `standard_user` |
| Password | Empty |

#### Steps

1. Open the login page, log out if already logged in, and clear both fields.
2. Enter `standard_user` in the username field.
3. Leave the password field empty.
4. Select `Login`.
5. Observe the feedback and the page shown.

#### Expected Result

The attempt is rejected with validation feedback. The inventory page is not reached.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

## Equivalence Partitioning

### Test ID: AGE-EP-90-C

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-c |
| Website | Test Pages validation form |
| Technique | Equivalence partitioning (EP-03: above 80) |
| Status | Not run |

#### Purpose

Check that an age from the "above 80" partition is rejected.

#### Preconditions

- The validation form is open: https://testpages.eviltester.com/apps/client-server-form-validation/
- All other fields will use the agreed valid baseline.
- The baseline (age 30) has been confirmed to submit successfully.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alex` |
| Surname | `TestingStudent` |
| Age | `90` |
| Country | Team-agreed country: |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `90`.
4. Submit.
5. Observe whether the form submits or shows a validation error.

#### Expected Result

Age 90 is rejected because it is above the maximum age of 80.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

## 2-Point Boundary Tests

### Test ID: AGE-2P-80-C

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-c |
| Website | Test Pages validation form |
| Technique | 2-point boundary testing |
| Status | Not run |

#### Purpose

Check that the maximum valid age (the upper boundary) is accepted.

#### Preconditions

- The validation form is open.
- All other fields will use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| Age | `80` |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `80`.
4. Submit.
5. Observe the response and, where displayed, check that the submitted age is 80.

#### Expected Result

Age 80 is accepted because the valid range is 18 to 80 inclusive. The form submits successfully with age 80.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

## 3-Point Boundary Tests

Convention used: ISTQB CTFL v4.0 eight-value convention (16, 17, 18, 19, 79, 80, 81, 82).

### Test ID: AGE-3P-79-C

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-c |
| Website | Test Pages validation form |
| Technique | 3-point boundary testing |
| Status | Not run |

#### Purpose

Check that the age immediately below the maximum boundary is accepted.

#### Preconditions

- The validation form is open.
- All other fields will use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| Age | `79` |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `79`.
4. Submit.
5. Observe the response and, where displayed, check that the submitted age is 79.

#### Expected Result

Age 79 is accepted because it is within the range 18 to 80 inclusive.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

### Age 80 — Own Earlier Execution

- Original test: `AGE-2P-80-C`
- Tester: `member-c`
- Record: [above](#test-id-age-2p-80-c)
- Reason for reuse: The baseline, environment, and procedure remain applicable.

### Reused Executions From Other Members

Fill in once the other members have recorded their results.

| Age | Original test | Tester | Record |
|---:|---|---|---|
| 16 | `AGE-3P-16-A` | member-a | [Member A’s results](member-a.md) |
| 17 | `AGE-2P-17-A` | member-a | [Member A’s results](member-a.md) |
| 18 | `AGE-2P-18-B` | member-b | [Member B’s results](member-b.md) |
| 19 | `AGE-3P-19-B` | member-b | [Member B’s results](member-b.md) |
| 81 | `AGE-2P-81-D` | member-d | [Member D’s results](member-d.md) |
| 82 | `AGE-3P-82-D` | member-d | [Member D’s results](member-d.md) |

Reason for reuse: The baseline, environment, and procedure remain applicable.

---

## Guided Test Coverage Check (Member C coordination role)

Tick each item only when the result is actually recorded in a member’s file.

### Login
- [ ] LOGIN-P01 — valid credentials (A)
- [ ] LOGIN-N01 — incorrect password (B)
- [ ] LOGIN-N02 — missing password (C)
- [ ] LOGIN-N03 — missing username (D)
- [ ] LOGIN-R01 — recovery (A, four-member team)

### Equivalence partitioning
- [ ] Age 30 (A)
- [ ] Age 10 (B)
- [ ] Age 90 (C)
- [ ] Blank age observation (D)
- [ ] `abc` observation (D, four-member team)

### 2-point boundaries
- [ ] 17 (A)
- [ ] 18 (B)
- [ ] 80 (C)
- [ ] 81 (D)

### 3-point boundaries
- [ ] 16 (A)
- [ ] 19 (B)
- [ ] 79 (C)
- [ ] 82 (D)

Missing or unexecuted cases:

-
