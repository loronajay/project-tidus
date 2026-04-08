# Project Tidus

## Safety and Test Checklist

## 1. Purpose

This document defines the safety and validation gates for the first Tidus prototype.

It is designed to support a test-driven, bottleneck-first workflow where each subsystem must prove stable behavior before the next layer of integration begins.

This is not a full compliance document. It is an internal prototype safety and test discipline document.

## 2. Operating Rules

The following rules apply across all phases:

- No subsystem moves forward without a defined test or validation objective
- No live hydrogen work begins until the related non-hydrogen checks are complete
- No unstable subsystem is treated as acceptable just to maintain schedule
- One variable should change at a time during troubleshooting
- Each meaningful test should produce a written result, even if brief
- If a result is ambiguous, the test is not complete

## 3. Test-Driven Workflow

Each integration step should follow this sequence:

1. Define the behavior, interface, or failure mode to be tested
2. Define the pass/fail condition before running the test
3. Run the smallest practical bench, mockup, or ride test that exposes the issue
4. Record the result
5. Only then make the next change
6. Re-run the focused test until the result is repeatable

This applies to software logic, electrical integration, mechanical fit, and hydrogen handling.

## 4. Test Record Minimum

Each test entry should capture at least:

- Test ID or short name
- Date
- Build phase
- Objective
- Setup
- Pass/fail criteria
- Result
- Follow-up action

## 5. Global Stop Conditions

Work should pause immediately if any of the following occur:

- Unexplained electrical instability on the shared DC bus
- Repeated startup or shutdown behavior that is not yet understood
- Evidence of unsafe hydrogen routing, leakage risk, or improvised handling
- Packaging that blocks shutoff, isolation, or service access
- A subsystem that passes only intermittently
- Pressure-bearing or safety-critical hardware without clear rating or traceability

The response to a stop condition is to stabilize and understand the issue before continuing.

## 6. Phase-Gated Checklist

### Phase 0 - Procurement and Integration Prep

Objective:

- Ensure all planned hardware and fixtures are suitable for safe prototype work

Checklist:

- [ ] All pressure-bearing hydrogen hardware is commercially rated
- [ ] All major subsystem classes are identified before procurement
- [ ] Bench testing needs are defined before frame integration work begins
- [ ] Temporary fixture needs are identified for electrical and mechanical tests
- [ ] Safety-critical unknowns are listed explicitly
- [ ] No component is being selected on convenience alone if it adds risk to a critical interface

Go/No-Go gate:

- Do not purchase or fabricate around pressure-bearing assumptions that are not yet verified

### Phase 1 - Electric Baseline Bike

Objective:

- Prove the propulsion platform is stable without hydrogen in the loop

Checklist:

- [ ] Motor, controller, and battery are electrically compatible
- [ ] Power-on and shutoff behavior is repeatable
- [ ] Brake function is confirmed before powered ride testing
- [ ] Wiring is secured well enough to survive normal vibration
- [ ] Battery-only riding behavior is predictable at low speed
- [ ] Any software or control changes are tested first before live ride checks

Go/No-Go gate:

- Do not add hydrogen subsystem complexity until the battery-only bike rides reliably

### Phase 2 - Bench Hybrid Power Integration

Objective:

- Prove stable electrical coexistence between the fuel cell, battery, and shared DC bus

Checklist:

- [ ] Bench setup is physically stable and organized before power testing
- [ ] Fuel cell output path is understood before connecting to the shared bus
- [ ] Battery support behavior under transient load is tested
- [ ] Startup sequence is defined before repeated power cycling
- [ ] Shutdown sequence is defined before repeated power cycling
- [ ] Bus behavior under changing load is observed and recorded
- [ ] Protection and disconnect assumptions are reviewed before higher-stress testing
- [ ] No recurring oscillation or unstable power-sharing behavior is ignored

Go/No-Go gate:

- Do not move to integrated frame packaging until hybrid electrical behavior is stable on the bench

### Phase 3 - Cartridge Dock and Hydrogen Path Mockup

Objective:

- Prove the cartridge interface and service layout before live hydrogen use

Checklist:

- [ ] Cartridge insertion path is repeatable
- [ ] Cartridge removal path is repeatable
- [ ] Latch or retention concept resists accidental movement
- [ ] User-facing swap action does not require tools
- [ ] Shutoff access remains reachable
- [ ] Regulator and gas-path routing fit within packaging constraints
- [ ] Service access is preserved for future inspection and troubleshooting
- [ ] Mockup does not force obvious lab-rig compromises

Go/No-Go gate:

- Do not introduce live hydrogen until the cartridge dock and gas path can be handled predictably in mockup form

### Phase 4 - Integrated Frame Package

Objective:

- Install the subsystems into bicycle form without losing safety or serviceability

Checklist:

- [ ] Fuel cell, battery, controller, and dock are securely mounted
- [ ] Cable routing is mechanically stable
- [ ] Cooling and ventilation paths are not obviously blocked
- [ ] Shutoff and isolation points remain accessible
- [ ] No subsystem depends on temporary hand-held positioning
- [ ] Packaging still resembles a bicycle and not an exposed bench rig
- [ ] Module removal paths remain possible for maintenance and debugging

Go/No-Go gate:

- Do not begin hydrogen commissioning if the integrated frame package is not mechanically stable and serviceable

### Phase 5 - Controlled Hydrogen Commissioning

Objective:

- Safely perform first live hydrogen integration and first hydrogen-assisted power-up

Checklist:

- [ ] Commissioning environment is controlled and deliberate
- [ ] Startup checklist exists before introducing hydrogen
- [ ] Shutdown checklist exists before introducing hydrogen
- [ ] Cartridge installation process is reviewed before first live test
- [ ] Shutoff path is known and reachable
- [ ] Regulation stage is checked before fuel-cell startup attempt
- [ ] First power-up result is recorded in writing
- [ ] Any abnormal smell, sound, pressure behavior, or fault response stops the test immediately
- [ ] No ride testing occurs during the first unstable commissioning session

Go/No-Go gate:

- Do not ride the bike under hydrogen power until startup, shutdown, and ready-state behavior are repeatable

### Phase 6 - Low-Speed Ride Validation

Objective:

- Confirm the integrated system behaves predictably under controlled riding loads

Checklist:

- [ ] Initial rides are low-speed and controlled
- [ ] Rider has a clear shutdown and stop procedure
- [ ] Acceleration behavior is observed for instability or lag
- [ ] Power transitions remain predictable during starts and moderate load changes
- [ ] Post-ride inspection checks mounting, routing, and visible subsystem condition
- [ ] Each ride test produces notes and follow-up actions
- [ ] Unresolved commissioning issues are not normalized during ride testing

Go/No-Go gate:

- Do not expand ride envelope until low-speed behavior is stable and repeatable

### Phase 7 - Demo Readiness Pass

Objective:

- Prepare a coherent prototype that can be shown safely and consistently

Checklist:

- [ ] Startup demonstration sequence is scripted
- [ ] Shutdown demonstration sequence is scripted
- [ ] Cartridge swap interaction is practiced and repeatable
- [ ] Temporary fixtures are reduced where practical
- [ ] Visible wiring and mounting clutter are reduced without hiding safety access
- [ ] Demo does not depend on unstable workarounds
- [ ] A no-demo condition is defined in case the prototype is not stable on the day

Go/No-Go gate:

- Do not present the prototype if the demo depends on operator improvisation to hide instability

## 7. Priority Test Areas

The highest-priority test areas for Tidus are:

1. Shared DC bus stability
2. Fuel-cell startup and shutdown behavior
3. Battery support during peak and transient loads
4. Cartridge seating and retention
5. Shutoff access and operator control clarity
6. Low-speed ride predictability

These should receive repeated focused testing before secondary polish work.

## 8. Minimum Evidence Required Before Investor Demo

Before any serious external demonstration, the project should be able to show:

- A repeatable startup sequence
- A repeatable shutdown sequence
- Stable low-speed ride behavior
- A repeatable cartridge insertion and removal interaction
- A written record of the most recent relevant test sessions

If one of these is missing, the demo risk is too high.

## 9. Document Outcome

This document defines the practical safety and validation discipline for the Tidus prototype.

The next useful supporting artifacts are:

- A subsystem procurement sheet
- A phase-by-phase build checklist
- A simple test log template
