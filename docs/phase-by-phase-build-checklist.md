# Project Tidus

## Phase-by-Phase Build Checklist

## 1. Purpose

This document turns the Tidus planning set into a practical execution checklist.

It is meant to be used alongside:

- `docs/prototype-build-plan.md`
- `docs/subsystem-procurement-sheet.md`
- `docs/safety-and-test-checklist.md`
- `docs/test-log-template.md`

The goal is to make progress visible, repeatable, and stable.

## 2. How To Use This Checklist

- Treat each phase as a gate, not a suggestion
- Do not skip to the next phase because parts arrived early
- Log meaningful tests as they happen
- If a stop condition appears, pause the checklist and stabilize the issue first
- Mark items complete only when the result is real and repeatable

## 3. Phase 0 - Procurement and Setup

### Objectives

- Establish the physical, electrical, and documentation foundations for the project

### Checklist

- [ ] Confirm donor-bike criteria before purchase
- [ ] Confirm rear-hub-motor target class stays near the locked power range
- [ ] Confirm 48V battery target and charger compatibility
- [ ] Confirm workshop safety basics are in place
- [ ] Confirm basic measurement tools are available
- [ ] Confirm mockup materials are available
- [ ] Confirm bench workspace exists and is usable
- [ ] Create a place to store test records and notes
- [ ] Create the first test record entry, even if it is only a setup/planning entry

### Done When

- You have enough hardware, tooling, and documentation structure to begin the battery-only build without guesswork

## 4. Phase 1 - Battery-Only Baseline Bike

### Objectives

- Build and verify a stable electric bicycle baseline before hydrogen complexity is introduced

### Checklist

- [ ] Acquire donor bike
- [ ] Inspect frame, brakes, wheels, and general condition
- [ ] Acquire rear hub motor kit
- [ ] Acquire compatible 48V battery and charger
- [ ] Install motor kit
- [ ] Install controller and rider controls
- [ ] Install temporary battery mounting solution
- [ ] Route wiring cleanly enough for safe low-speed testing
- [ ] Verify basic power-on behavior
- [ ] Verify basic shutoff behavior
- [ ] Perform first controlled powered wheel test
- [ ] Perform first low-speed battery-only ride test
- [ ] Log test results
- [ ] Fix any instability before moving on

### Done When

- The bike rides reliably on battery power alone and can serve as a trustworthy propulsion baseline

## 5. Phase 2 - Bench Hybrid Power Validation

### Objectives

- Prove that the future hybrid electrical architecture can behave predictably off-bike

### Checklist

- [ ] Define the first bench hybrid test objective
- [ ] Build organized bench wiring layout
- [ ] Add protection and controlled disconnect points
- [ ] Define startup pass/fail criteria before first run
- [ ] Define shutdown pass/fail criteria before first run
- [ ] Set up representative load approach
- [ ] Run initial bus-stability test
- [ ] Observe and record transient behavior
- [ ] Re-run the focused test until results are repeatable
- [ ] Log all major test outcomes
- [ ] Stop and investigate if oscillation or ambiguous instability appears

### Done When

- The shared electrical behavior is stable enough that integration onto the bicycle will not be blind experimentation

## 6. Phase 3 - Cartridge Dock and Packaging Mockup

### Objectives

- Prove the cartridge swap geometry and packaging direction before live hydrogen work

### Checklist

- [ ] Define initial cartridge placement zone on the bike
- [ ] Create first physical mockup for cartridge size and removal path
- [ ] Mock regulator and shutoff placement
- [ ] Check insertion and removal direction
- [ ] Check user access for swap behavior
- [ ] Check service access for shutoff and inspection
- [ ] Check frame-width and visual-discipline constraints
- [ ] Revise mockup if the package starts looking like a lab rig
- [ ] Log packaging decisions and unresolved issues

### Done When

- Cartridge handling, shutoff access, and packaging direction are believable enough to support integrated build planning

## 7. Phase 4 - Integrated Frame Package

### Objectives

- Move the validated subsystem directions into a real bicycle-mounted prototype package

### Checklist

- [ ] Finalize provisional subsystem placement
- [ ] Mount battery, controller, and electrical paths cleanly
- [ ] Mount fuel-cell placeholder or final unit as appropriate to the phase
- [ ] Mount cartridge dock structure
- [ ] Secure major routing paths
- [ ] Confirm ventilation and cooling path assumptions are not blocked
- [ ] Confirm nothing safety-critical requires hand support or improvised positioning
- [ ] Confirm the bike still reads visually as a bicycle
- [ ] Log packaging and mounting outcomes

### Done When

- The prototype is mechanically coherent and serviceable before hydrogen commissioning begins

## 8. Phase 5 - Controlled Hydrogen Commissioning

### Objectives

- Perform first live hydrogen integration under deliberate, documented conditions

### Checklist

- [ ] Define first commissioning objective
- [ ] Write startup checklist
- [ ] Write shutdown checklist
- [ ] Confirm commissioning environment is controlled
- [ ] Confirm shutoff path is known and reachable
- [ ] Inspect cartridge installation process before first live test
- [ ] Perform first live commissioning attempt
- [ ] Record outcome immediately
- [ ] Stop immediately if abnormal behavior appears
- [ ] Re-run only after the observed issue is understood

### Done When

- Startup, shutdown, and ready-state behavior under hydrogen are stable enough to permit controlled ride validation

## 9. Phase 6 - Low-Speed Ride Validation

### Objectives

- Validate integrated behavior under controlled riding load

### Checklist

- [ ] Define first ride-test objective
- [ ] Confirm stop and shutdown procedure is known before riding
- [ ] Perform first controlled low-speed ride
- [ ] Observe acceleration and transition behavior
- [ ] Inspect the bike immediately after the ride
- [ ] Log ride observations
- [ ] Correct instability before expanding ride scope
- [ ] Re-test the same focused scenario until it becomes repeatable

### Done When

- The bike can perform controlled low-speed riding with predictable behavior and no unresolved critical instability

## 10. Phase 7 - Demo Readiness

### Objectives

- Prepare a cleaner, safer, more coherent version of the prototype for external viewing

### Checklist

- [ ] Reduce visible temporary fixtures where practical
- [ ] Improve wire discipline without blocking service access
- [ ] Practice startup sequence
- [ ] Practice shutdown sequence
- [ ] Practice cartridge swap interaction
- [ ] Define no-demo conditions
- [ ] Confirm the demo does not rely on operator improvisation
- [ ] Log the final demo-readiness check

### Done When

- The prototype can be shown without hiding instability or depending on fragile workarounds

## 11. First Progress Milestones

The earliest meaningful milestones for Tidus are:

- [ ] Donor bike selected
- [ ] Electric baseline parts acquired
- [ ] First battery-only wheel spin test completed
- [ ] First battery-only ride test completed
- [ ] First test log entry created
- [ ] First packaging mockup created

If you complete those, the project is no longer just conceptual.

## 12. Weekly Focus Rule

At any point, try to keep the week focused on one primary bottleneck:

- drivetrain baseline
- bus stability
- packaging geometry
- commissioning behavior
- ride predictability

That will help protect the stability-first style you want.

## 13. Document Outcome

This checklist turns the Tidus planning documents into a concrete execution path that can be followed one phase at a time.
