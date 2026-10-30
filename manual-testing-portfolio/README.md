# Manual Testing Portfolio

Test documentation I authored while training in manual software testing: **137 test cases** across five widely used apps (Ola, Zomato, MakeMyTrip, Facebook, Discord) plus Microsoft Word, covering integration, functional, usability and ad hoc testing.

> **Disclaimer.** This is a learning portfolio. It is not affiliated with, endorsed by or sponsored by any of the companies named. Test cases are written from publicly visible app behaviour. Expected results reflect what I expected at the time and may differ from current app behaviour.

## What is inside

| App | File | Test cases | Types |
|---|---|---|---|
| Ola (and Uber for usability) | [`ola.csv`](test-cases/ola.csv) | 30 | Integration (10), Usability (10), Ad hoc (10) |
| Zomato (and Swiggy for usability) | [`zomato.csv`](test-cases/zomato.csv) | 30 | Integration (10), Usability (10), Ad hoc (10) |
| MakeMyTrip (and Goibibo for usability) | [`makemytrip.csv`](test-cases/makemytrip.csv) | 20 | Integration (10), Usability (10) |
| Facebook | [`facebook.csv`](test-cases/facebook.csv) | 20 | Functional (20) |
| Discord | [`discord.csv`](test-cases/discord.csv) | 27 | Functional (27) |
| Microsoft Word | [`ms-word.csv`](test-cases/ms-word.csv) | 10 | Ad hoc (10) |
| **Total** | | **137** | Integration (30), Usability (30), Ad hoc (30), Functional (47) |

```
test-plan/test-plan.md                          scope, approach, techniques, severity definitions
test-cases/*.csv                                one file per app
rtm/requirement-traceability-matrix.csv         30 feature areas mapped to test case IDs
bug-reports/TEMPLATE.md                         defect report template
docs/defect-severity-exercise.md                severity classification practice (watch, pen drive, A4 paper)
screenshots/                                    evidence (to be added)
```

## Test types

- **Integration** (Ola, Zomato, MakeMyTrip): multi-step flows that cross modules and often two accounts, for example rider books, driver accepts, payment and receipt are verified on both sides.
- **Functional** (Facebook, Discord): component-level checks of login, posting, comments, servers, channels, messaging, voice and video.
- **Usability** (Ola/Uber, Swiggy/Zomato, MakeMyTrip/Goibibo): clarity, accessibility and layout checks on the key screens.
- **Ad hoc** (Ola, Zomato, MS Word): negative, edge and interruption scenarios such as expired promo codes, airplane mode mid-ride, forced close and AutoRecover.

## Techniques applied

- **Equivalence partitioning**: valid and invalid email, password and UPI ID classes.
- **Boundary value analysis**: 10-digit phone number (9 / 10 / 11), zero and negative wallet amounts, maximum item quantity, upload size limit.
- **State transition testing**: booking, cancellation, reschedule and refund flows, and order and ride lifecycles.
- **Error guessing / ad hoc**: connectivity loss, missing permissions, idle sessions, crash recovery.

## Test case format

`ID, Module, Scenario, Preconditions, Steps, Test Data, Expected, Actual, Status, Priority, Type`

## Status

Test cases are authored and reviewed. Execution results (`Actual` and `Status`) are being recorded; cases still show `Not Run` until executed. Defects will be added under `bug-reports/` only when a real defect is reproduced.

## Author

Mohammed Inayathulla | [LinkedIn](https://linkedin.com/in/mohammed-inayathulla711) | [GitHub](https://github.com/MohammadInayathulla)
