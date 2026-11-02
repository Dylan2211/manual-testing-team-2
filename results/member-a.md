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

Captured in evidence folder "Evidence Member-a.png"

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

1.Input "standard_user" in username
2.Input "wrong_password" in password
3.Click on the green "Login" button
4.Delete the previous incorrect password
5.Input "secret_sauce" in password
6.Click on the green "Login" button

#### Expected Result

Unsuccessful login, followed by successful login by using correct password

#### Actual Result

Unsuccessful login, followed by successful login by using correct password

#### Evidence

Captured in evidence folder "Evidence Member-a.png"


## Equivalence Partitioning

## 2-Point Boundary Tests

## 3-Point Boundary Tests
