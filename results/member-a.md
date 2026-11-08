# Manual Testing Results — Member A

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-a |
| Date and time |03/11/26 |
| Browser and version |Firefox158.0(64-bit) |
| Operating system |Linux Mint 22.3 - Cinnamon 64-bit |

## Login Tests
### Test ID: LOGIN-P01

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-a |
| Website |https://www.saucedemo.com/  |
| Status | Pass|

#### Purpose

This test verifies that basic login works

#### Preconditions

The validation form is open, and the input is valid

#### Test Data

| Field | Value |
|---|---|
| Input standard_user | Input secret_sauce|

#### Steps

1.Input "standard_user" in username
2.Input "secret_sauce" in password
3.Click on the green "Login" button

#### Expected Result

Successful login

#### Actual Result

Successful login

#### Evidence

Captured in evidence folder "LOGIN-P01.png"

# Login Tests
### Test ID: LOGIN-R01

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-a |
| Website |https://www.saucedemo.com/  |
| Status | Pass|

#### Purpose

This test verifies that wrong password does not allow login

#### Preconditions

The validation form is open, and the input is valid

#### Test Data

| Field | Value |
|---|---|
| Input standard_user | Input wrong_password|

#### Steps

1. Input "standard_user" in username
2. Input "wrong_password" in password
3. Click on the green "Login" button
4. Delete the previous incorrect password
5. Input "secret_sauce" in password
6. Click on the green "Login" button

#### Expected Result

Unsuccessful login, followed by successful login by using correct password

#### Actual Result

Unsuccessful login, followed by successful login by using correct password

#### Evidence

Captured in evidence folder "LOGIN-R01.png"


## Equivalence Partitioning
### Test ID: AGE-EP-30-A

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-a |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status |pass |

#### Purpose

This test checks the default case passes.

#### Preconditions

The validation form is open, and all fields contain correct information

#### Test Data

| Field | Value |
|First name|Alex|
|Surname|TestingStudent |
|Age|30|
|Country|Zimbabwe|
|Notes|Manual testing classroom exercise|

#### Steps
1. Open the validation form
2. Input "Alex" in first name
3. Input "TestingStudent" in surname
4. Input "30" in age
5. Input "Zimbabwe" 
6. Input "Manual testing classroom exercise"
7. Click on submit

#### Expected Result

Submission is successful.

#### Actual Result

Submission happened, same as expected.

#### Evidence

Captured in "Evidence" folder "AGE-EP-30-A.png"

---


## 2-Point Boundary Tests
### Test ID: AGE-2P-17-A

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-a |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status |pass |

#### Purpose

This test inputting 17 for age case passes (Doesn't work).

#### Preconditions

The validation form is open, and all other fields will use the agreed valid baseline

#### Test Data

| Field | Value |
|First name|Alex|
|Surname|TestingStudent |
|Age|"17"|
|Country|Zimbabwe|
|Notes|Manual testing classroom exercise|

#### Steps
1. Open the validation form
2. Input "Alex" in first name
3. Input "TestingStudent" in surname
4. Input "17" in age
5. Input "Zimbabwe"
6. Input "Manual testing classroom exercise"
7. Click on submit

#### Expected Result

The form does not allow the submission and returns an error/popup

#### Actual Result

Expected result happened, form submission failed and returned a popup

#### Evidence

Captured in "Evidence" folder "AGE-2P-17-A.mp4"

---


## 3-Point Boundary Tests

### Test ID: AGE-3P-16-A

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-a |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status |pass |

#### Purpose

This test inputting 16 for age case passes (Doesn't work).

#### Preconditions

The validation form is open, and all other fields will use the agreed valid baseline

#### Test Data

| Field | Value |
|First name|Alex|
|Surname|TestingStudent |
|Age|"17"|
|Country|Zimbabwe|
|Notes|Manual testing classroom exercise|

#### Steps
1. Open the validation form
2. Input "Alex" in first name
3. Input "TestingStudent" in surname
4. Input "16" in age
5. Input "Zimbabwe"
6. Input "Manual testing classroom exercise"
7. Click on submit

#### Expected Result

The form does not allow the submission and returns an error/popup

#### Actual Result

Expected result happened, form submission failed and returned a popup

#### Evidence

Captured in "Evidence" folder "AGE-3P-16-A"

---


