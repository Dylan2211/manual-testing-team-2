# Team Summary

## Guided Testing Coverage

### Login Testing

Required coverage:
- Valid credentials.
- Incorrect password.
- Missing password.
- Missing username.
- Recovery after an invalid attempt.

Results:
|Test purpose|Test Results link|
|This test verifies that basic login works|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-a.md|
|Check that the login page rejects an incorrect password.|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-b.md|
||https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-c.md|
|Check whether the application rejects a login attempt with a missing username.|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-d.md|

### Equivalence Partitioning

Required coverage:
- Age below the accepted range.
- Age within the accepted range
- Age above the accepted range.

Results:
|Test purpose|Test Results link|
|This test checks the default case passes.|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-a.md |
|Check that an age from the below-18 partition is rejected.|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-b.md|
||https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-c.md|
|To observe how the form handles an empty age field when all other fields contain valid data.|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-d.md|


### Input-Format Observations

Required observations:
- Blank age.
- Non-numeric age input.

Results:


### 2-Point Boundary Testing

Required values:
17, 18, 80, 81.

Results:
|Test purpose|Test Results link|
|This test inputting 17 for age case passes (Doesn't work).|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-a.md |
|Check that the minimum permitted age of 18 is accepted.|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-b.md|
||https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-c.md|
|To check whether the form rejects age 81, which is immediately above the maximum accepted age of 80.|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-d.md|


### 3-Point Boundary Testing

Required values:
16, 17, 18, 19, 79, 80, 81, 82.

Results:
  activity for Development Operations week 3.
|Test purpose|Test Results link|
|This test inputting 16 for age case passes (Doesn't work).|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-a.md |
|Check that an age immediately above the minimum boundary is accepted.|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-b.md|
||https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-c.md|
|To check whether the form rejects age 82, which is the immediate value above boundary value 81 and is outside the maximum accepted age of 80.|https://github.com/Dylan2211/manual-testing-team-2/blob/main/results/member-d.md|

## Member Contributions

### Member A

- Guided results: [View results](results/member-a.md)
- Self-designed tests: [View tests](exploratory/member-a.md)
- Reflection: [View reflection](reflections/member-a.md)
- Chosen investigation:
- Main observation:
- Pull request: https://github.com/Dylan2211/manual-testing-team-2/pull/5

### Member B

- Guided results: [View results](results/member-b.md)
- Self-designed tests: [View tests](exploratory/member-b.md)
- Reflection: [View reflection](reflections/member-b.md)
- Chosen investigation:
- Main observation:
- Pull request: https://github.com/Dylan2211/manual-testing-team-2/pull/4

### Member C

- Guided results: [View results](results/member-c.md)
- Self-designed tests: [View tests](exploratory/member-c.md)
- Reflection: [View reflection](reflections/member-c.md)
- Chosen investigation:
- Main observation:
- Pull request: Add the actual pull-request link.

### Member D

- Guided results: [View results](results/member-d.md)
- Self-designed tests: [View tests](exploratory/member-d.md)
- Reflection: [View reflection](reflections/member-d.md)
- Chosen investigation:
- Main observation:
- Pull request: https://github.com/Dylan2211/manual-testing-team-2/pull/3
