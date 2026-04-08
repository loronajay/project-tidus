# Project Tidus

## Test Log Template

## 1. Purpose

This template is the standard format for recording Tidus test activity.

It is designed to support a test-driven, stability-first workflow where each meaningful test has:

- A defined objective
- A pass/fail condition set before the test
- A written result
- A clear next action

## 2. Usage Rules

- Use one entry per discrete test session or focused validation step
- Do not combine unrelated tests into one record
- If the result is ambiguous, record it as incomplete rather than pass
- If a stop condition is triggered, record it explicitly
- Re-run the same test with a new entry whenever the setup or implementation changes in a meaningful way

## 3. Blank Template

```md
# Test Record: [Short Test Name]

- Test ID:
- Date:
- Build Phase:
- Owner:
- Status: Planned / In Progress / Pass / Fail / Incomplete / Blocked

## Objective

- What behavior, interface, or failure mode is being tested?

## Why This Test Matters

- Which bottleneck, safety gate, or integration risk does this test address?

## Pre-Test Pass/Fail Criteria

- Pass:
- Fail:
- Stop Condition:

## Setup

- Hardware involved:
- Software/firmware involved:
- Environment:
- Preconditions:

## Procedure

1. 
2. 
3. 

## Observations

- 

## Result

- Outcome:
- Was the result repeatable?
- Did any stop condition occur?

## Follow-Up Actions

- 

## Next Test

- What is the next focused test that should happen because of this result?
```

## 4. Recommended Status Meanings

- `Planned`: Test is defined but not yet run
- `In Progress`: Test session is active and not yet concluded
- `Pass`: Pass criteria met clearly and repeatably
- `Fail`: Fail criteria triggered clearly
- `Incomplete`: Test was run but did not produce a clear conclusion
- `Blocked`: Test could not proceed because a prerequisite was missing

## 5. Example Entry

```md
# Test Record: DC Bus Startup Stability Under Bench Load

- Test ID: T-002
- Date: 2026-04-08
- Build Phase: Phase 2 - Bench Hybrid Power Integration
- Owner: Jay
- Status: Incomplete

## Objective

- Verify that the shared DC bus reaches a stable ready state during startup with the buffer battery connected and a representative load attached.

## Why This Test Matters

- This test addresses the highest-priority bottleneck of shared DC bus stability before frame integration.

## Pre-Test Pass/Fail Criteria

- Pass: Bus reaches stable ready state without oscillation or protection trips across three consecutive startup attempts.
- Fail: Bus oscillates, protection trips repeatedly, or startup cannot complete.
- Stop Condition: Any unexpected heat, smell, noise, or uncontrolled voltage behavior.

## Setup

- Hardware involved: Fuel cell bench output, 48V battery, DC bus wiring, representative load
- Software/firmware involved: Basic startup logic if present
- Environment: Bench setup in controlled workspace
- Preconditions: Wiring inspected, disconnect path known, startup sequence written down

## Procedure

1. Verify wiring and disconnect access.
2. Apply startup sequence once and observe bus behavior.
3. Repeat startup sequence two more times if no stop condition occurs.

## Observations

- First startup reached target state but showed brief instability before settling.
- Second startup produced a similar transient.
- No stop condition occurred.

## Result

- Outcome: Incomplete
- Was the result repeatable? Partially
- Did any stop condition occur? No

## Follow-Up Actions

- Review transient behavior around startup.
- Narrow the next test to the battery-support portion of the startup sequence.

## Next Test

- Isolate startup transient behavior with a tighter battery-support bench test.
```

## 6. Suggested ID Pattern

Use a simple sequential ID format:

- `T-001`
- `T-002`
- `T-003`

If later needed, the ID can be extended by phase, but simple numbering is enough at this stage.

## 7. Recommended Storage

When real testing begins, store completed records in a dedicated location such as:

- `tests/logs/`

Keep this file as the reusable source template in:

- `docs/test-log-template.md`

## 8. Document Outcome

This template gives Tidus a consistent way to capture focused test work, reduce ambiguity, and prevent unstable behavior from being normalized.
