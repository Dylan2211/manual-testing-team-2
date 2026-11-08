# Self-Designed Testing — Member A

## Testing Idea

To investigate the input form's notes input

## Reason

Since different people could be doing the form in different languages, there could be an argument to allow different languages to be input in the notes field (or in more extreme cases wingdings, etc)

## Test Basis

This tests validity of other languages input and other weird inputs

## Approach

The Notes in input form field will use different languages and wierd online characters to test other languages validity in the notes section

## Test Cases

### Test ID: OWN-A-01

| Item | Details |
|---|---|
| Test type | Exploratory |
| Tester | member-a |
| Status | pass |

#### Purpose

This tests input field's validity of other languages and other input types

#### Preconditions

The agreed upon baseline other than in the notes section

#### Test Data

"
❄︎⍓︎◻︎♏︎ ⍓︎□︎◆︎❒︎ ⧫︎♏︎⌧︎⧫︎ ♒︎♏︎❒︎♏︎📬︎ 🕆︎⬧︎♏︎ ✌︎☹︎☹︎ 👍︎✌︎🏱︎💧︎ ♐︎□︎❒︎ 🕈︎ 👎︎ ☝︎♋︎⬧︎⧫︎♏︎❒︎🕯︎⬧︎ ●︎♋︎■︎♑︎◆︎♋︎♑︎♏︎ 🖳︎✆︎
会意; 會意;
ÿ
 देवनागरी
(˚ д˚ ≡˚ д˚ ) 
" Is the input for the Notes field
#### Steps

1. Input all the other fields based on the agreed baseline (Other than Notes)
2. Input "❄︎⍓︎◻︎♏︎ ⍓︎□︎◆︎❒︎ ⧫︎♏︎⌧︎⧫︎ ♒︎♏︎❒︎♏︎📬︎ 🕆︎⬧︎♏︎ ✌︎☹︎☹︎ 👍︎✌︎🏱︎💧︎ ♐︎□︎❒︎ 🕈︎ 👎︎ ☝︎♋︎⬧︎⧫︎♏︎❒︎🕯︎⬧︎ ●︎♋︎■︎♑︎◆︎♋︎♑︎♏︎ 🖳︎✆︎
会意; 會意;
ÿ
 देवनागरी
(˚ д˚ ≡˚ д˚ ) 
" For the notes
3. Click on submit query

#### Expected Result

The form goes through and the input is correctly captured

#### Actual Result

The Notes input is captured and displayed in one line

#### Evidence

Evidence is in the evidence folder "OWN-A-01.png"

---

## Overall Observations

The test shows that other language characters are correctly captured

## Next Question

Probably validity of other fields
