# Manual Testing Results — Member D

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-d |
| Date and time | 3 November 2026, 2:58 pm |
| Browser and version | Firefox, 159.0 (64-bit) |
| Operating system | Windows |

## Login Tests
### Test ID: LOGIN-N03

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-d |
| Website | SauceDemo |
| Status | Pass |

#### Purpose

Check whether the application rejects a login attempt with a missing username.

#### Preconditions

The SauceDemo login page is open.

#### Test Data

| Field | Value |
|---|---|
| Username: Empty | Password: secret_sauce |

#### Steps

1. Open SauceDemo.
2. Leave the username empty.
3. Enter the password.
4. Select Login.
5. Observe the feedback.

#### Expected Result

The attempt is rejected with validation feedback. The inventory is not reached.

#### Actual Result

Login is rejected with validation feedback, "Epic sadface: Username is required". The inventory is not reached.

#### Evidence

!#### Evidence
[View screenshot](../evidence/member-d/login-n03.png)

---

## Equivalence Partitioning

## 2-Point Boundary Tests
### Test ID: YOUR-TEST-ID

| Item | Details |
|---|---|
| Test type | Positive / Negative / Recovery |
| Tester | Your member identifier |
| Website | Website name |
| Status | Not run |

#### Purpose

What does this test check?

#### Preconditions

What must be true before the test starts?

#### Test Data

| Field | Value |
|---|---|
| Input name | Input value |

#### Steps

1.
2.
3.

#### Expected Result

Write this before executing the test.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

## 3-Point Boundary Tests
### Test ID: YOUR-TEST-ID

| Item | Details |
|---|---|
| Test type | Positive / Negative / Recovery |
| Tester | Your member identifier |
| Website | Website name |
| Status | Not run |

#### Purpose

What does this test check?

#### Preconditions

What must be true before the test starts?

#### Test Data

| Field | Value |
|---|---|
| Input name | Input value |

#### Steps

1.
2.
3.

#### Expected Result

Write this before executing the test.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---