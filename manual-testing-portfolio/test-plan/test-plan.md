# Test Plan: Manual Testing Portfolio

| Field | Value |
|---|---|
| Author | Mohammed Inayathulla |
| Document status | Draft v1.0 |
| Test cases covered | 137 (see `test-cases/`) |

## 1. Introduction

This plan describes how manual testing was designed for five consumer apps (Ola, Zomato, MakeMyTrip, Facebook, Discord) and Microsoft Word, as part of hands-on training in software testing.

## 2. Objectives

- Verify that the core user journeys of each app behave as a user would expect.
- Verify that cross-module and cross-account flows stay consistent (for example, a ride booked by a rider is visible and completable by a driver).
- Check usability of key screens such as registration, home and search.
- Probe negative, boundary and interruption scenarios that normal use rarely hits.

## 3. Scope

**In scope**

| Area | Apps |
|---|---|
| Integration testing | Ola, Zomato, MakeMyTrip |
| Functional testing | Facebook (login, post creation, comments), Discord (authentication, servers and channels, messaging, voice and video) |
| Usability testing | Ola and Uber, Swiggy and Zomato, MakeMyTrip and Goibibo |
| Ad hoc testing | Ola, Zomato, Microsoft Word |

**Out of scope**: performance, load, security and penetration testing; automation; backend and API testing; real payments beyond what each scenario needs.

## 4. Test approach

| Type | Approach |
|---|---|
| Integration | End-to-end flows across modules, using User A and User B accounts where the flow crosses roles (rider and driver, customer and partner side). |
| Functional | One check per field or behaviour: positive, negative, empty and special-character inputs. |
| Usability | Heuristic review of layout, labels, accessibility of key controls and information clarity. |
| Ad hoc | Experience-based scenarios: network loss, permissions off, expired data, idle sessions, forced close. |

## 5. Test design techniques

Equivalence partitioning, boundary value analysis, state transition testing and error guessing (examples in `README.md`).

## 6. Severity and priority

Severity describes impact on the product; priority describes how soon it should be fixed. Definitions below follow the classification practice in `docs/defect-severity-exercise.md`.

| Severity | Meaning | Example (digital watch) |
|---|---|---|
| Blocker | Product or feature is unusable; testing cannot continue | Watch does not work even after fitting a new cell |
| Critical | Core function works but gives seriously wrong results | Watch runs but skips 15 minutes |
| Major | Important feature impaired; workaround may exist | Watch does not beep every hour |
| Minor | Cosmetic or low-impact | Spelling mistake in the name on the watch |

Test case priority (High / Medium / Low) in the CSVs is a proposed ordering for execution: High covers money, authentication and core booking or ordering flows.

## 7. Test environment

Fill in before publishing results:

| Item | Value |
|---|---|
| Devices / OS | [add] |
| App versions | [add] |
| Browsers (web checks) | [add] |
| Network | [add] |
| Accounts | Two accounts per app where a flow needs User A and User B |

## 8. Entry and exit criteria

- **Entry**: app installed and accounts available; test cases reviewed; test data prepared.
- **Exit**: all High priority cases executed; every failed case has a logged defect; results recorded in `Actual` and `Status`.

## 9. Deliverables

Test plan, test case CSVs, requirement traceability matrix, defect reports (when defects are found), screenshots as evidence.

## 10. Defect reporting

Defects follow `bug-reports/TEMPLATE.md`: title, environment, steps to reproduce, expected versus actual, severity, priority, screenshot.

## 11. Risks and assumptions

- Apps change frequently, so expected results may drift from current behaviour.
- Some flows (payments, refunds, driver-side screens) depend on second accounts or live services and may not be reproducible every time.
- Features such as upload size limits and channel naming rules are provider-defined and should be re-verified against the current app before results are recorded.
