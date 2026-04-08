# Project Tidus

## Phase 1 - Prototype Architecture Definition

## 1. Purpose

This document locks the baseline architecture for the first credible Project Tidus prototype.

The goal of this phase is not to optimize performance, range, or cost. The goal is to define a buildable architecture that can demonstrate a believable consumer product direction and support later planning and implementation work.

## 2. Locked Prototype Configuration

The first Tidus prototype is locked as a hydrogen-electric hybrid bicycle with the following baseline configuration:

- One removable compressed-hydrogen cartridge as the onboard fuel source
- One low-temperature PEM fuel cell as the primary energy conversion device
- One lithium-ion buffer battery for transient load support and startup stability
- One standard electric bicycle motor and controller set

This prototype is explicitly not a pure battery e-bike and not a fuel-cell-only bike. It is a hybrid architecture intended to make hydrogen usable in a bicycle form factor.

## 3. Architecture Summary

### 3.1 Energy Path

```text
Hydrogen cartridge
        |
        v
Pressure regulation
        |
        v
PEM fuel cell
        |
        v
DC power bus
   |           |
   v           v
Buffer battery Motor controller
                |
                v
              Motor
```

### 3.2 Operating Philosophy

The fuel cell provides the baseline continuous electrical supply.

The battery handles:

- Startup support
- Acceleration spikes
- Grade changes
- Short-duration power instability

The motor system remains a standard e-bike drive solution so the prototype effort stays focused on hydrogen integration rather than custom drivetrain development.

## 4. Locked Component Classes

### 4.1 Hydrogen Storage

Locked class:

- Removable compressed-hydrogen cartridge
- Refillable offboard
- Consumer-swappable
- Commercially rated pressure vessel only

Constraints:

- No custom tank fabrication in this phase
- No onboard refill operation
- No onboard hydrogen generation
- Cartridge interface must support repeatable insertion and removal without tools

### 4.2 Fuel Cell

Locked class:

- Low-temperature PEM fuel cell
- Air-cooled preferred for prototype simplicity
- Sized for continuous baseline propulsion support rather than peak output

Reason for lock:

- PEM is the most practical fit for low-temperature mobile use
- It aligns with the need for compact packaging and predictable integration

### 4.3 Buffer Battery

Locked class:

- Lithium-ion e-bike battery pack
- 48V nominal system class
- Sized for peak shaving and short fallback operation rather than long standalone range

Reason for lock:

- The battery is required for ride quality, startup stability, and peak-load smoothing
- Removing it would create a less credible and less controllable prototype

### 4.4 Motor and Drive System

Locked class:

- Standard 48V e-bike motor system
- Rear hub motor for prototype simplicity
- Standard off-the-shelf controller

Reason for lock:

- Rear hub integration reduces mechanical complexity during the first build
- It avoids unnecessary custom work in the drivetrain while the hydrogen subsystem is still being proven

## 5. Locked Power Targets

The prototype is locked to the following first-pass power targets:

- Fuel cell continuous output target: 400W class
- Motor nominal output target: 500W class
- Motor peak output target: 750W class
- Electrical architecture target: 48V nominal

Interpretation:

- The fuel cell supports cruise and steady-state riding loads
- The battery covers short peak demands above the fuel cell's steady output
- The motor remains strong enough to demonstrate real bicycle propulsion without requiring an oversized hydrogen system

These targets are intentionally conservative. They are meant to produce a stable demonstration platform, not a maximum-performance vehicle.

## 6. Locked Vehicle Behavior Assumptions

The first prototype is intended to behave like a practical assisted bicycle, not a lightweight motorcycle.

The prototype should support:

- Predictable assisted riding behavior
- Stable power delivery during starts and moderate acceleration
- Short refueling interaction through cartridge swapping
- Familiar rider controls consistent with a normal e-bike

The prototype is not required in this phase to prove:

- Maximum range leadership
- High-speed performance
- Heavy cargo capability
- Extreme hill-climb performance

## 7. Physical Layout Constraints

### 7.1 Packaging Direction

The system must preserve the visual identity of a bicycle.

Locked packaging rules:

- The hydrogen cartridge must be mounted within or closely integrated to the main frame triangle or downtube zone
- The fuel cell and power electronics must remain within the bicycle's central mass area
- The battery must be integrated as part of the frame package, not hung externally as a temporary block
- The motor must remain in the rear wheel as a standard hub unit

### 7.2 Visual Discipline

The prototype must avoid presenting as a lab rig.

Locked constraints:

- No loose external wiring runs where shielding or routing is possible
- No oversized exposed plumbing if a compact routing option exists
- No side-mounted modules that significantly exceed normal bicycle width
- No requirement for tools to perform the normal cartridge swap interaction

### 7.3 Service Access

The prototype must remain maintainable while still resembling a product direction.

Locked access rules:

- Cartridge removal must be accessible from a user-facing position
- Safety-critical shutoff and isolation points must be reachable without major disassembly
- Core electrical and hydrogen subsystems must be modular enough to remove independently during development

## 8. Refueling Interaction Definition

The prototype will model refueling as cartridge exchange, not direct consumer hydrogen filling.

Locked assumptions:

- The user's primary interaction is removing an empty cartridge and inserting a filled one
- Hydrogen filling occurs offboard by trained or controlled handling processes
- The mail-based exchange concept remains compatible with this hardware direction

This means the hardware must be designed around swap behavior first, even if actual early testing uses manually prepared cartridges.

## 9. Safety Baseline

The prototype must be designed around commercially credible safety language from the beginning.

Locked safety principles:

- Use only commercially rated hydrogen storage hardware
- Include pressure regulation between cartridge and fuel cell
- Treat leak management, ventilation, and shutoff access as first-order design requirements
- Avoid any architecture that depends on users handling exposed improvised hydrogen connections

This phase does not finalize a full compliance strategy, but it does lock the expectation that the prototype must be explainable in product and investor terms without hand-waving.

## 10. Explicit Exclusions

The following are not part of the Phase 1 prototype architecture:

- Custom fuel-cell development
- Custom motor development
- Onboard electrolysis
- Consumer direct refill from a home hydrogen system
- Multi-cartridge automatic switching systems
- Full production industrial design

These can be revisited only after the baseline prototype architecture has been validated.

## 11. What This Architecture Must Prove

If built correctly, this architecture should be able to demonstrate:

- Hydrogen-supported propulsion in a bicycle form factor
- Stable hybrid power behavior
- A believable cartridge-swap ownership model
- A product direction that investors can compare against ordinary e-bike expectations

## 12. Document Outcome

This document locks the baseline prototype architecture for Project Tidus.

The next planning documents should build from this baseline rather than reopen core architecture choices. The system-level follow-on is documented in `docs/system-block-diagram-and-interface-map.md`.

The next useful documents are:

- System block diagram and interface map
- Prototype build plan
- Safety and test checklist
- Investor demo criteria
