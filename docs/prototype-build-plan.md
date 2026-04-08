# Project Tidus

## Prototype Build Plan

## 1. Purpose

This document defines the build sequence for the first Tidus prototype.

The plan is organized around retiring the highest-risk interfaces first:

- Standard e-bike propulsion baseline
- Fuel-cell-to-electrical-bus integration
- Cartridge and regulation integration
- Bicycle packaging and ride validation

The intent is to avoid committing to full-frame integration before the core subsystems behave predictably.

## 2. Planning Principles

The build plan follows these rules:

- Use a test-driven development mindset for both software and subsystem integration
- Validate subsystems on the bench before installing them on the bike
- Attack the highest-leverage bottlenecks before optimizing secondary features
- Delay irreversible fabrication until core interfaces are proven
- Use off-the-shelf components wherever possible in the first build
- Prefer stable, repeatable behavior over rapid iteration speed
- Keep the first integrated prototype focused on stable function, not visual perfection
- Treat hydrogen handling as a gated commissioning activity, not a casual workshop step

## 3. Development Posture

Project Tidus should be executed with a bottleneck-first, test-driven workflow.

That means:

- Before implementing a subsystem change, define the behavior or failure mode being tested
- Add the smallest meaningful test, check, fixture, or validation step that proves that behavior
- Only then change the subsystem, controls, or packaging needed to satisfy the test
- Re-test after each change before moving further into integration

In software-heavy areas, this should follow normal TDD:

- Write the test first
- Implement the minimum change needed
- Re-run tests until behavior is stable

In hardware and integration-heavy areas, the equivalent is:

- Define the interface or failure case first
- Build the smallest bench or mockup test that can expose it
- Change one variable at a time
- Do not move to full integration until the focused test passes repeatably

This project should also prefer stability over speed:

- A slower but repeatable subsystem is better than a fast-moving unstable integration effort
- New complexity should only be introduced after the current layer behaves consistently
- If a subsystem is flaky, the correct response is to stop and stabilize it, not build around it

## 4. Build Sequence Summary

| Phase | Goal | Primary Output |
| --- | --- | --- |
| 0 | Lock procurement assumptions and fixtures | Parts-class shortlist and integration checklist |
| 1 | Create a rideable electric baseline | Working 48V motor/controller/battery bike |
| 2 | Prove hybrid power behavior off-bike | Bench-tested DC bus with battery and fuel-cell integration logic |
| 3 | Develop cartridge dock and hydrogen path packaging | Mechanical mockup and regulated gas-path layout |
| 4 | Build integrated frame package | Mounted subsystems in bicycle form factor |
| 5 | Commission hydrogen system in controlled conditions | First safe hydrogen-powered power-up |
| 6 | Perform low-speed ride validation | Initial ride data and integration fixes |
| 7 | Prepare investor-facing prototype pass | Stable demo-ready prototype direction |

## 5. Phase Details

### Phase 0 - Procurement and Integration Prep

Objective:

- Confirm the exact part classes needed to execute the locked architecture without reopening scope

Main work:

- Select target classes for cartridge, regulator, PEM fuel cell, battery, motor, and controller
- Define connector, mounting, and enclosure assumptions at a system level
- Identify what requires a mockup first versus what can be bought immediately
- Decide what temporary bench fixtures are needed before bicycle integration

Outputs:

- Procurement shortlist by subsystem
- Bench test fixture list
- Frame packaging assumptions

Exit criteria:

- No unresolved architecture questions that block subsystem procurement
- Clear list of what can be tested without hydrogen

### Phase 1 - Electric Baseline Bike

Objective:

- Build a conventional rideable 48V e-bike baseline before adding hydrogen complexity

Main work:

- Install rear hub motor and controller
- Install temporary buffer battery as the sole initial energy source
- Verify throttle and pedal-assist behavior if used
- Confirm braking, wiring routing, and general rideability

Outputs:

- Rideable electric baseline platform
- Known-good traction system
- Baseline power behavior reference

Exit criteria:

- Bike starts, runs, and rides reliably on battery alone
- Electrical layout is clean enough to serve as the integration foundation

Why this phase matters:

- If the propulsion platform is unstable before hydrogen integration, later debugging becomes ambiguous

### Phase 2 - Bench Hybrid Power Integration

Objective:

- Prove that the fuel cell, battery, and electrical bus can coexist before installing them on the bicycle

Main work:

- Create bench setup for fuel cell output, battery path, and controller-equivalent load
- Validate startup behavior and power sharing assumptions
- Observe DC bus stability under changing load conditions
- Define basic system logic for startup, ready, and fault states

Outputs:

- Bench-validated hybrid electrical architecture
- Preliminary startup and shutdown sequence
- Early fault list

Exit criteria:

- Fuel cell can support the bus without unstable oscillation
- Battery can absorb peak or transient demand as intended
- Major electrical protection gaps are identified before bike integration

Why this phase matters:

- This is the most important technical de-risking step in the whole build plan

### Phase 3 - Cartridge Dock and Hydrogen Path Mockup

Objective:

- Develop the cartridge interface and gas-path packaging before live hydrogen commissioning

Main work:

- Build or mock the cartridge dock geometry
- Define latch, insertion path, and user-access direction
- Package regulator and shutoff positions relative to the cartridge and fuel cell
- Check routing against frame space, service access, and visual constraints

Outputs:

- Cartridge dock mockup
- Hydrogen path packaging concept
- Service-access layout

Exit criteria:

- Cartridge can be inserted and removed repeatably in the intended orientation
- Packaging does not force obvious lab-rig compromises
- Shutoff and service points remain accessible

Why this phase matters:

- The swap experience is part of the product thesis, not a detail to patch in later

### Phase 4 - Integrated Frame Package

Objective:

- Mount the proven electrical architecture and validated packaging concept onto the bicycle

Main work:

- Install fuel cell, battery, controller, and major wiring into the frame package
- Install cartridge dock and regulation assembly
- Secure cooling, ventilation, and cable routing paths
- Replace temporary mounts with cleaner prototype-grade brackets or enclosures

Outputs:

- Full integrated prototype without live hydrogen commissioning yet
- Packaged subsystem mounting solution
- Serviceable subsystem access plan

Exit criteria:

- All major subsystems are physically mounted
- Routing is organized and mechanically stable
- The build still presents as a bicycle rather than an exposed bench assembly

### Phase 5 - Controlled Hydrogen Commissioning

Objective:

- Perform the first live hydrogen integration under controlled conditions

Main work:

- Verify shutoff, isolation, and inspection procedures before introducing hydrogen
- Perform first cartridge installation in a controlled environment
- Validate regulation stage and fuel-cell startup behavior
- Check for obvious fault conditions before any ride testing

Outputs:

- First confirmed hydrogen-assisted power-up
- Commissioning log
- Immediate issue list

Exit criteria:

- No unacceptable leak, shutdown, or startup behavior
- System can enter a stable ready state
- Safe repeatable startup and shutdown sequence exists

Why this phase matters:

- This is the highest-consequence gate in the build plan and should not be rushed

### Phase 6 - Low-Speed Ride Validation

Objective:

- Confirm that the integrated prototype behaves predictably under real riding loads

Main work:

- Perform controlled low-speed rides in a restricted environment
- Observe acceleration, transition behavior, and power stability
- Inspect packaging after vibration and motion exposure
- Adjust control behavior and mounting details based on observed issues

Outputs:

- Initial ride-validation notes
- Integration issue backlog
- Revised routing, mounting, or control requirements

Exit criteria:

- Bike remains rideable and stable under normal demo-level use
- No recurring subsystem failure makes the prototype unsuitable for further development

### Phase 7 - Demo Readiness Pass

Objective:

- Produce a more coherent investor-facing prototype from the validated integrated build

Main work:

- Improve enclosure cleanliness and cable discipline
- Refine cartridge swap presentation
- Reduce visible temporary fixtures where possible
- Prepare a clear startup, ride, and shutdown demonstration script

Outputs:

- Demo-ready prototype pass
- Operator checklist
- Investor demo flow

Exit criteria:

- Prototype can be shown without requiring excessive explanation of temporary workarounds
- Core product story is visible in the object itself

## 6. Workstreams That Can Run in Parallel

The following can overlap once the architecture is locked:

- Electric baseline bike assembly
- Bench hybrid power integration setup
- Cartridge dock mockup design
- Frame packaging study using cardboard, foam, or temporary fixtures

The following should not be rushed in parallel:

- Live hydrogen commissioning before bench electrical behavior is understood
- Final enclosure fabrication before packaging geometry is validated

## 7. Suggested Early Deliverables

Before live hydrogen work begins, the project should already have:

- A working electric baseline bike
- A bench-tested hybrid power architecture
- A cartridge dock mockup that demonstrates insertion and removal
- A frame packaging mockup that shows subsystem placement

If those do not exist, the project is not ready for integrated hydrogen commissioning.

## 8. Stop Conditions

Work should pause and be reassessed if any of the following occur:

- The fuel cell and battery cannot share the electrical bus stably
- The cartridge dock cannot be packaged without compromising bicycle usability
- The hydrogen path requires improvised unsafe handling
- The integrated build becomes visually or mechanically closer to a bench rig than a bike
- The team is skipping focused validation steps in order to move integration faster
- A known unstable subsystem is being treated as "good enough for now"

These are architecture-level warnings, not just minor build issues.

## 9. Immediate Next Actions

The next actionable planning step after this document is to convert the phases above into:

- A subsystem procurement sheet
- A build checklist by phase
- A safety and test checklist tied to the commissioning gates

## 10. Document Outcome

This document defines the sequence for building the first Tidus prototype in a way that reduces ambiguity, protects time and money, and keeps the project aligned with the locked product thesis.
