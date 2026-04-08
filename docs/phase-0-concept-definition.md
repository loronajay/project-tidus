# Project Tidus

## Phase 0 - Broad Scope and Bottleneck Strategy

## 1. Core Definition

Project Tidus is a research and development initiative focused on building a consumer-viable hydrogen-powered bicycle system. The system uses hydrogen as the primary energy carrier, with water treated only as an indirect source material upstream of hydrogen production.

The project does not attempt to violate physical constraints. All usable energy in the system originates from external electrical input.

## 2. Locked System Model

### Energy Flow

```text
External Energy (grid / renewable)
        |
        v
Hydrogen Production (offboard)
        |
        v
Hydrogen Storage (cartridge / tank)
        |
        v
Fuel Cell (on vehicle)
        |
        v
Electric Motor
        |
        v
Motion
```

### Byproducts

- Water
- Heat

## 3. Product Target

Project Tidus targets a consumer-facing hydrogen bicycle that:

- Operates similarly to an e-bike
- Uses hydrogen cartridges instead of conventional battery charging as the primary refueling interaction
- Prioritizes ease of use, fast refueling, and practical ownership

## 4. Explicit Non-Goals

The following are out of scope for this phase:

- Onboard water-to-hydrogen generation as the primary energy source
- Self-sustaining or closed-loop propulsion claims
- Reinventing electrolysis technology
- Large-scale hydrogen infrastructure development
- Custom fuel-cell science as an initial differentiator

## 5. Core Bottlenecks

### 5.1 Refueling Infrastructure

Current hydrogen mobility systems typically depend on centralized refueling stations or fleet-style deployment. That model does not translate cleanly to individual consumer ownership.

Impact: This is the primary barrier to consumer adoption.

### 5.2 Storage Constraints

Hydrogen storage systems are currently limited by tanks that are:

- Bulky
- Expensive
- Perception-sensitive because of safety concerns

Impact: Storage constrains form factor, price, and user trust.

### 5.3 Consumer Usability

Hydrogen has no clear consumer mental model equivalent to plugging in a battery or filling a gas tank.

Impact: Even a technically functional system may fail due to user friction.

### 5.4 Cost Structure

Fuel cells and hydrogen storage remain expensive, and there is no obvious low-cost entry point for consumer-scale ownership.

Impact: Cost is a direct blocker to market viability.

## 6. Strategic Focus Areas

### 6.1 Swappable Hydrogen Cartridge System

This is the primary differentiation focus for Tidus.

Concept:

- Small, removable hydrogen tanks
- User swaps cartridges rather than directly refilling the vehicle

Analogues:

- Propane tanks
- CO2 canisters

Goals:

- Standardized form factor
- Tool-less removal and insertion
- Fast swap, ideally under one minute

### 6.2 Mail-Based Exchange System

This is the secondary refueling model under consideration.

Concept:

- Users receive pre-filled hydrogen cartridges through delivery
- Empty cartridges are returned for refill and redistribution

Commercial model:

- Subscription
- Pay-per-use

Advantages:

- Avoids dependence on local hydrogen stations at the start
- Centralizes handling while decentralizing consumer use
- Creates a plausible early adoption path before local infrastructure exists

### 6.3 Hybrid System Architecture

The on-vehicle system should follow a practical hybrid architecture:

- Hydrogen fuel cell for primary energy conversion
- Buffer battery for transient loads and load balancing
- Electric motor using standard e-bike integration patterns

Purpose:

- Smooth power delivery
- Handle acceleration and peak demand
- Prevent erratic system behavior

### 6.4 Consumer-Oriented Packaging

The product direction must remain visually and physically close to a standard bicycle.

Constraints:

- Minimal exposed components
- Integrated tank placement
- Clean wiring and structure
- No obvious lab-rig presentation

## 7. Prototype Philosophy

The first prototype is not intended to be a final product. Its purpose is to validate the direction, not to maximize performance.

The prototype must prove:

- Hydrogen-to-motion is reliable
- Cartridge-based refueling is understandable and viable
- System behavior under load is stable and predictable
- Form factor trends toward consumer acceptability

## 8. Success Criteria for Phase 1 Readiness

An early prototype is considered successful enough to move into deeper architecture and planning work when it demonstrates:

- Functional hydrogen-powered propulsion
- Safe and repeatable cartridge insertion and removal
- Stable ride behavior without severe power fluctuation
- A coherent system layout rather than a loose technical assembly

## 9. Positioning Statement

Project Tidus is not attempting to beat current e-bikes on today's cost, simplicity, or infrastructure conditions.

It is building toward a model in which hydrogen becomes a viable energy system for small personal vehicles by improving the refueling experience and tightening system integration for consumer ownership.

## 10. Hard Constraints

The following constraints are locked:

- Energy must originate externally
- Hydrogen is the fuel; water is not the onboard energy source
- Onboard electrolysis is not the primary propulsion method
- The system must be physically buildable with current technology

## 11. Document Outcome

This document locks the broad scope for Project Tidus and defines the bottlenecks the project is explicitly trying to solve.

The architecture follow-on is documented in `docs/phase-1-prototype-architecture-definition.md`, which locks:

- Exact component classes
- Initial power targets
- Physical layout constraints

Scope should not expand beyond those architecture decisions until the prototype baseline is fixed.
