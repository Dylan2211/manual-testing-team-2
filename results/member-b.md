# Manual Testing Results — Member B

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-b |
| Date and time | 3 November 2026, afternoon (from the commit history) |
| Browser and version | Not recorded at the time |
| Operating system | Windows |

> **Correction, 8 November 2026:** I checked my screenshots again. The age 18 and age 19 submissions were rejected because of the first name, so I had recorded them wrongly as accepted. Both records are now marked `Blocked`, and the original screenshots are linked. The ages were re-run with a valid first name in [my self-designed tests](../exploratory/member-b.md) (OWN-B-10 and OWN-B-11).

## Login Tests

### Test ID: LOGIN-N01

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-b |
| Website | [SauceDemo](https://www.saucedemo.com/) |
| Status | Pass |

#### Purpose

Check that the login page rejects an incorrect password.

#### Preconditions

The user is logged out and the login page is open with both fields cleared.

#### Test Data

| Field | Value |
|---|---|
| Username | `standard_user` |
| Password | `wrong_password` |

#### Steps

1. Open https://www.saucedemo.com/.
2. Enter `standard_user` as the username.
3. Enter `wrong_password` as the password.
4. Select `Login`.
5. Observe the page and feedback.

#### Expected Result

Login is rejected, error feedback appears, and the inventory is not reached.

#### Actual Result

Login was rejected. The message "Epic sadface: Username and password do not match any user in this service" appeared, both fields were marked with an error icon, and the inventory page was not reached.

#### Evidence

[View screenshot](../evidence/member-b/login-n01.png)

---

## Equivalence Partitioning

### Test ID: AGE-EP-10-B

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | Equivalence partitioning (EP-01, below 18) |
| Status | Pass |

#### Purpose

Check that an age from the below-18 partition is rejected.

#### Preconditions

The validation form is open. All other fields use the agreed baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alex` |
| Surname | `TestingStudent` |
| Age | `10` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Enter the agreed baseline.
3. Replace the age with `10`.
4. Select `Submit`.
5. Observe the response.

#### Expected Result

Age 10 is rejected because it is below the minimum of 18.

#### Actual Result

The browser prevented the submission and showed the message "Value must be greater than or equal to 18." next to the Age field. The form was not sent to the server.

#### Evidence

[View screenshot](../evidence/member-b/age-ep-10-b.png)

---

## 2-Point Boundary Tests

### Test ID: AGE-2P-18-B

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 2-point boundary testing |
| Status | Blocked |

#### Purpose

Check that the minimum permitted age of 18 is accepted.

#### Preconditions

The validation form is open. All other fields use the agreed baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alex` |
| Surname | `TestingStudent` |
| Age | `18` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Enter the agreed baseline.
3. Replace the age with `18`.
4. Select `Submit`.
5. Observe the response.

#### Expected Result

Age 18 is accepted because the range 18–80 is inclusive.

#### Actual Result

The form reached the server, but the Validation Report showed "Firstname Error — Firstname too short" for `Alex`. No age error was listed, but the submission was not successful, so this run cannot show whether age 18 is accepted.

Re-run on 8 November 2026 with the first name `Alexa`: age 18 was accepted. See OWN-B-10 in [my self-designed tests](../exploratory/member-b.md).

#### Evidence

[View screenshot](../evidence/member-b/age-2p-18-b.png)

---

## 3-Point Boundary Tests

### Test ID: AGE-3P-19-B

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | [Test Pages Validation Form](https://testpages.eviltester.com/apps/client-server-form-validation/) |
| Technique | 3-point boundary testing |
| Status | Blocked |

#### Purpose

Check that an age immediately above the minimum boundary is accepted.

#### Preconditions

The validation form is open. All other fields use the agreed baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | `Alex` |
| Surname | `TestingStudent` |
| Age | `19` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

#### Steps

1. Open the validation form.
2. Enter the agreed baseline.
3. Replace the age with `19`.
4. Select `Submit`.
5. Observe the response.

#### Expected Result

Age 19 is accepted because it is inside the range 18–80.

#### Actual Result

The form reached the server, but the Validation Report showed "Firstname Error — Firstname too short" for `Alex`. No age error was listed, but the submission was not successful, so this run cannot show whether age 19 is accepted.

Re-run on 8 November 2026 with the first name `Alexa`: age 19 was accepted. See OWN-B-11 in [my self-designed tests](../exploratory/member-b.md).

#### Evidence

[View screenshot](../evidence/member-b/age-3p-19-b.png)

---

## Summary

| Test ID | Test type | Input | Expected | Status |
|---|---|---|---|---|
| LOGIN-N01 | Negative | Incorrect password | Reject | Pass |
| AGE-EP-10-B | Negative | Age 10 | Reject | Pass |
| AGE-2P-18-B | Positive | Age 18 | Accept | Blocked (first name rejected) |
| AGE-3P-19-B | Positive | Age 19 | Accept | Blocked (first name rejected) |

Two tests passed and two were blocked by the baseline first name. The age 10 rejection came from the browser's own number check, not from the server. The blocked ages were re-run successfully in OWN-B-10 and OWN-B-11.
