### Test ID: LOGIN-N01

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-b |
| Website | SauceDemo |
| Status | Not run |

#### Purpose
Verify that the login page rejects a user who enters an incorrect password.

#### Preconditions
The SauceDemo login page is open, and the user is logged out.

#### Test Data

| Field | Value |
|---|---|
| Username | `standard_user` |
| Password | `wrong_password` |

#### Steps
1. Open the SauceDemo login page.
2. Enter `standard_user` as the username.
3. Enter `wrong_password` as the password.
4. Click Login.
5. Observe the error message and the page displayed.

#### Expected Result
The login attempt is rejected, an error message appears, and the product inventory is not displayed.

#### Actual Result
The login attempt is rejected and an error message is displayed. No product inventory is displayed.

#### Evidence
<img width="919" height="365" alt="image" src="https://github.com/user-attachments/assets/95ca960f-7fd8-4252-9aa9-517cfcb6b895" />
