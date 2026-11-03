# Member B - Manual Testing Results

**Tester:** Member B  
**Branch:** `testing/member-b`  
**Testing Type:** Manual Testing

---

## Test Case 1: LOGIN-N01 - Incorrect Password

| Attribute | Details |
|---|---|
| Test ID | LOGIN-N01 |
| Test Type | Negative Testing |
| Test Objective | Verify that the login page rejects an incorrect password. |
| Website | https://www.saucedemo.com/ |
| Username | standard_user |
| Password | wrong_password |
| Preconditions | User is logged out and the login page is open. |

### Test Steps
1. Navigate to https://www.saucedemo.com/.
2. Enter `standard_user` as the username.
3. Enter `wrong_password` as the password.
4. Click the Login button.
5. Observe the response.

**Expected Result:**  
The login attempt should be rejected. An error message should appear, and the user should not gain access to the product inventory.

**Actual Result:**  
The login attempt rejected. Error message displayed, and acces to product inventory not granted.

**Status:**  RUN

**Evidence:** `evidence/member-b/login-n01.png

---

## Test Case 2: AGE-EP-10-B - Equivalence Partitioning

| Attribute | Details |
|---|---|
| Test ID | AGE-EP-10-B |
| Test Type | Equivalence Partitioning |
| Test Objective | Verify that ages below the minimum permitted age are rejected. |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Field Tested | Age |
| Test Data | 10 |
| Valid Age Range | 18–80 (inclusive) |
| Input Category | Invalid - Below minimum |

### Test Preconditions
The validation form is open, and all other fields contain valid information.

### Test Data

| Field | Input |
|---|---|
| First name | Alex |
| Surname | TestingStudent |
| Age | 10 |
| Country | Any available country |
| Notes | Manual testing classroom exercise |

### Test Steps
1. Open the validation form.
2. Enter the test data shown above.
3. Click Submit.
4. Observe the validation response.

**Expected Result:**  
The form should reject the submission because age 10 is below the minimum permitted age of 18.

**Actual Result:**  
The submission is rejected and an error message is displayed saying the age must be equal to or greater than 18.

**Status:** RUN

**Evidence:** `evidence/member-b/age-ep-10-b.png`

---

## Test Case 3: AGE-2P-18-B - 2-Point Boundary Value Analysis

| Attribute | Details |
|---|---|
| Test ID | AGE-2P-18-B |
| Test Type | 2-Point Boundary Value Analysis |
| Test Objective | Verify that the minimum permitted age is accepted. |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Field Tested | Age |
| Test Data | 18 |
| Minimum Boundary | 18 |
| Maximum Boundary | 80 |

### Test Preconditions
The validation form is open, and all other fields contain valid information.

### Test Data

| Field | Input |
|---|---|
| First name | Alex |
| Surname | TestingStudent |
| Age | 18 |
| Country | Any available country |
| Notes | Manual testing classroom exercise |

### Test Steps
1. Open the validation form.
2. Enter the test data shown above.
3. Click Submit.
4. Observe the validation response.

**Expected Result:**  
The form should accept age 18 because it is the minimum permitted age (inclusive).

**Actual Result:**  
The submission is accepted

**Status:** RUN

**Evidence:** `evidence/member-b/age-2p-18-b.png`

---

## Test Case 4: AGE-3P-19-B - 3-Point Boundary Value Analysis

| Attribute | Details |
|---|---|
| Test ID | AGE-3P-19-B |
| Test Type | 3-Point Boundary Value Analysis |
| Test Objective | Verify that an age immediately above the minimum boundary is accepted. |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Field Tested | Age |
| Test Data | 19 |
| Minimum Boundary | 18 |
| Maximum Boundary | 80 |

### Test Preconditions
The validation form is open, and all other fields contain valid information.

### Test Data

| Field | Input |
|---|---|
| First name | Alex |
| Surname | TestingStudent |
| Age | 19 |
| Country | Any available country |
| Notes | Manual testing classroom exercise |

### Test Steps
1. Open the validation form.
2. Enter the test data shown above.
3. Click Submit.
4. Observe the validation response.

**Expected Result:**  
The form should accept age 19 because it is within the permitted age range of 18–80.

**Actual Result:**  
The form is accepted

**Status:** RUN

**Evidence:** `evidence/member-b/age-3p-19-b.png`

---

## Test Execution Summary

| Test ID | Test Type | Test Input | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| LOGIN-N01 | Negative Testing | Incorrect password | Reject | Pending | NOT RUN |
| AGE-EP-10-B | Equivalence Partitioning | Age: 10 | Reject | Pending | NOT RUN |
| AGE-2P-18-B | 2-Point Boundary Testing | Age: 18 | Accept | Pending | NOT RUN |
| AGE-3P-19-B | 3-Point Boundary Testing | Age: 19 | Accept | Pending | NOT RUN |

---

## Overall Observations

## Overall Observations

All four test cases were executed successfully, and all test cases passed.

The SauceDemo login test (LOGIN-N01) correctly rejected the login attempt when an incorrect password was entered, displaying an appropriate error message and preventing access to the product inventory.

For the validation form, the equivalence partitioning test (AGE-EP-10-B) correctly rejected age 10 because it was below the minimum permitted age of 18.

The 2-point boundary test (AGE-2P-18-B) successfully accepted age 18, confirming that the minimum age limit is inclusive. Similarly, the 3-point boundary test (AGE-3P-19-B) accepted age 19, confirming that values immediately above the minimum boundary are valid.

Overall, both websites behaved as expected during testing. The results demonstrate that negative testing, equivalence partitioning and boundary value analysis are useful techniques for identifying whether applications correctly handle valid and invalid inputs.

No unexpected behaviour was observed during the execution of these test cases.

**Final Result: 4 out of 4 test cases passed (100% pass rate).**

Record:
- Whether the websites behaved as expected.
- Any unexpected behaviour encountered.
- Any validation errors or inconsistencies.
- The overall outcome of the four test cases.


