# Team Plan

## Team Identifier
Team 2

## Members
### Member A
- GitHub username: Dylan2211
- Coordination responsibility:Team-Coordination, Repository Integration

### Member B
- GitHub username: doublejlee
- Coordination responsibility: Requirements and Baseline

### Member C
- GitHub username: Petroalio
- Coordination responsibility: Guided Test Coverage

### Member D
- GitHub username: mareeppo
- Coordination responsibility: Evidence Organisation, Repository Integration

## Guided Test Allocation
### 1. Login Testing — SauceDemo

Member D: Login with a missing username (LOGIN-N03)

### 2. Age Validation Testing — Test Pages

Member D: Blank age, non-numeric age (abc), 2-point boundary value (81), and 3-point boundary value (82)

## Agreed Baseline Data
### SauceDemo Login

| Item | Baseline Data |
|---|---|
| Website | https://www.saucedemo.com/ |
| Username | `standard_user` |
| Password | `secret_sauce` |
| Starting state | Logged out |
| Login fields | Both fields cleared before testing |

### Test Pages Validation Form

| Item | Baseline Data |
|---|---|
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| First name | `Alex` |
| Surname | `TestingStudent` |
| Age | `30` |
| Country | Zimbabwe |
| Notes | `Manual testing classroom exercise` |

### Baseline Issue Found by Member B (8 November 2026)

The server now rejects the baseline first name `Alex` with "Firstname too short". A first name needs at least 5 characters to be accepted, although the published requirements only say it must be filled. `Alexa` is accepted. Age tests run with `Alex` were rejected for the first name, not the age. Details: [Member B self-designed tests](exploratory/member-b.md).

### Testing Rules

| Rule | Agreement |
|---|---|
| Initial baseline test | Submit all baseline data and confirm successful submission first. |
| Age testing | Change only the age value for each age test. |
| Other fields | Keep all other fields unchanged and valid. |
| Country | All members use the same agreed country. |
| Results | Record the actual behaviour observed during testing. |
| Evidence | Store screenshots in the appropriate member evidence folder. |
| Reused results | Identify the original tester, test ID and result file. |

## Open-Ended Testing Allocation

### Member B — Open-Ended Testing

- Chosen area: Test Pages validation form, surname field.
- Question to investigate: Does the form treat the stated surname length of "between 11 and 79" characters as inclusive, and does it reject 10 and 80?

### Member D — Open-Ended Testing

- Chosen area: SauceDemo shopping cart.
- Question to investigate: Does the shopping cart display the correct products and item count when products are added and removed?

## Repository Integration Arrangements
- Each member works on their own Git branch.
- Each member commits and pushes their own testing work.
- Each member creates a pull request from their branch into main.
- Member A and Member D share repository integration responsibilities.
- The team checks that files are in the correct folders.
- Use a merge method that preserves individual commits.
- Do not overwrite another member's work when resolving conflicts.
- After merging, verify the contributions on the main branch.