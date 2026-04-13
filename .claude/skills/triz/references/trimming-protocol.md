# Trimming Analysis Protocol

## Core Concept

Trimming is TRIZ's method for increasing system ideality by removing components while preserving or redistributing their useful functions. Rather than adding complexity to solve problems, trimming asks: "What can we remove?"

Every removed component eliminates its cost, failure modes, maintenance burden, and harmful side effects. The challenge is ensuring the useful function it provided is still delivered — either by another component already in the system, by the supersystem, or by recognizing the function is no longer needed.

Trimming is the most direct path to the Ideal Final Result: the system that performs its function without existing.

## Trimming Rules

### Rule A: Function Reassigned to Existing Component

The component is removed. Its useful function is performed by another component already present in the system.

```
Before:  Component X performs Function F on Object O
After:   Component Y (already in system) performs Function F on Object O
```

**Criteria for applying Rule A**:
- Component Y has physical access to Object O (proximity)
- Component Y can generate the required field/action (capability)
- Component Y is not overloaded (capacity)
- The modification to Y is feasible and economical

**Example**: A coffee machine has a separate hot water spout. Trimming: the main brewing head (already heats water, already has a spout) delivers hot water directly. The separate spout is removed.

### Rule B: Function No Longer Needed

The component is removed. Its function was only necessary because of another component or condition that has also been removed or changed.

```
Before:  Component X performs Function F to compensate for Problem P
After:   Problem P is eliminated, Function F is unnecessary, Component X is removed
```

**Criteria for applying Rule B**:
- The function exists only to counteract a side effect
- The root cause of the side effect can be eliminated
- Removing the function does not create a new problem

**Example**: A cooling fan exists because the motor overheats. Switching to a more efficient motor that does not overheat eliminates the need for the fan entirely.

### Rule C: Function Transferred to Supersystem

The component is removed. Its function is performed by something outside the system boundary — a supersystem element, the user, or the environment.

```
Before:  Component X performs Function F within the system
After:   Supersystem element Z performs Function F for the system
```

**Criteria for applying Rule C**:
- The supersystem element reliably provides the function
- The system does not need to be self-contained for this function
- The transfer does not create dependency risks that outweigh the benefit

**Example**: A portable device includes a GPS receiver. Trimming: the device uses the smartphone's GPS (supersystem) via Bluetooth. The internal GPS module is removed.

## Process

### Step 1: Build the Function Model

Create a complete inventory of the system:

**1a. List all components**

Include every physical component, substance, and field in the system. Do not omit "obvious" components — they are often the best trimming candidates.

Format:
```
Component | Main Function | Acts On | Field/Action Type
----------|--------------|---------|------------------
Motor     | Rotates      | Shaft   | Mechanical
Housing   | Contains     | All components | Mechanical
Bearing   | Supports     | Shaft   | Mechanical
Sensor    | Measures     | Temperature | Thermal→Electrical
...       | ...          | ...     | ...
```

**1b. Map all functions**

For each component, identify:
- **Useful functions** (the reason it exists)
- **Auxiliary functions** (secondary benefits it provides)
- **Harmful functions** (negative side effects it causes)

**1c. Draw the function diagram**

Show components as nodes. Draw arrows for each function:
- Solid arrows for useful functions
- Dashed arrows for harmful functions
- Arrow labels describe the function (verb + qualifier)

### Step 2: Rank Components

Score each component on two dimensions:

**Cost** (broadly defined):
- Purchase/manufacturing cost
- Installation complexity
- Maintenance requirements
- Failure rate and consequences
- Space/weight consumed
- Energy consumed

**Functional importance**:
- How many useful functions does it perform?
- Are those functions critical or peripheral?
- How many other components depend on it?

**Trimming priority** = High Cost + Low Functional Importance

Components with high cost and few/weak useful functions are the primary trimming candidates. Components with many critical functions and low cost should be preserved and potentially assigned additional functions from trimmed components.

### Step 3: Apply Trimming Rules

Starting from the highest-priority trimming candidate:

1. **Attempt Rule B first**: Is the function actually needed? If it only compensates for another problem, can that problem be eliminated?

2. **Attempt Rule A second**: Which remaining component could perform this function? Check proximity, capability, and capacity.

3. **Attempt Rule C third**: Can the supersystem provide this function? Is the user, environment, or adjacent system a viable provider?

4. **If none apply**: The component cannot be trimmed at this time. Move to the next candidate.

For each successful trim, update the function model — the reassigned function may enable or require further trims.

### Step 4: Cascade Analysis

Trimming one component often enables trimming others:

- Component X was removed; its function moved to Component Y
- Component Z existed only to connect X to Y — Z is now unnecessary (Rule B)
- Component W was a fastener for Z — W is now unnecessary (Rule B)

Follow the cascade until no further trims are possible. This cascade effect is where trimming delivers its greatest value — a single initial trim can eliminate a chain of dependent components.

### Step 5: Verify System Integrity

After all proposed trims, verify:

- [ ] The main useful function of the system is still delivered
- [ ] All critical secondary functions are still delivered
- [ ] No new harmful effects have been introduced
- [ ] The trimmed system is physically feasible
- [ ] The function reassignments do not overload remaining components
- [ ] Reliability has not decreased unacceptably

### Step 6: Document Before/After

Present the trimming results:

```
BEFORE (Original System)
========================
Components: [count]
Functions: [count useful] / [count harmful]
Key cost drivers: [list]

TRIMMING ACTIONS
================
1. Trim [Component] — Rule [A/B/C]: [explanation]
2. Trim [Component] — Rule [A/B/C]: [explanation]
...

AFTER (Trimmed System)
======================
Components: [count] (reduced by N)
Functions: [count useful] / [count harmful]
Cost reduction: [estimate]
Complexity reduction: [qualitative assessment]
```

## Advanced Trimming Techniques

### Inverse Trimming

Instead of removing a component and redistributing its function, ask: "What if this component took on ALL the functions?" This identifies potential supersystem-level simplifications where one powerful component replaces many.

### Feature Transfer

When trimming a component, look for opportunities to transfer not just its primary function but also its beneficial secondary functions to the receiving component. This increases the ideality of the receiving component.

### Trimming Across System Boundaries

Consider trimming components by transferring their functions to:
- The object being processed (the workpiece does it to itself)
- The raw material (the input arrives pre-processed)
- The output (the product self-assembles after delivery)
- The environment (gravity, ambient heat, atmospheric pressure)

### Temporal Trimming

A component needed only during one phase of operation may be replaced by a temporary substance or field that exists only when needed:
- Phase-change materials (ice as a temporary mold)
- Sacrificial substances (dissolving support structures)
- Self-destructing mechanisms (one-time packaging)

## Anti-Patterns

### 1. Trimming Load-Bearing Components Without Redistribution

Removing a structurally critical component without a viable function recipient collapses the system. Always verify that Rule A, B, or C genuinely applies before trimming.

### 2. Ignoring Secondary Functions

A component may have a primary function (obvious) and several secondary functions (non-obvious). Trimming based only on the primary function can cause unexpected failures.

Example: A housing "contains" components (primary) but also "shields" from EMI (secondary), "conducts" heat away (secondary), and "dampens" vibration (secondary). Removing the housing requires handling all four functions, not just containment.

### 3. Overloading the Survivor

Transferring too many functions to a single remaining component can make it the new bottleneck — too complex, too expensive, or too failure-prone. Trimming should distribute load, not concentrate it.

### 4. Trimming for Cost Alone

A cheap, reliable component that performs a critical function well should not be trimmed simply because the exercise calls for removing things. Trimming serves ideality, not minimalism for its own sake.

### 5. Ignoring the Human Component

Users, operators, and maintainers are components in the supersystem. Transferring functions to them (Rule C) must account for their skill level, cognitive load, and error rate. "The user will just remember to do it" is not a robust function transfer.

## Trimming and Other TRIZ Tools

- **IFR**: The ultimate trim is the Ideal Final Result — the entire system is trimmed, only the function remains
- **Su-Field**: Trimming a substance from a Su-Field model must be compensated by restructuring the remaining Su-Field (applying Standard Solutions)
- **Resources**: Resource analysis identifies what is available to receive transferred functions
- **Evolution**: Systems naturally evolve toward trimming (Law of Increasing Ideality) — trimming accelerates this natural trajectory
- **Contradiction**: When trimming creates a contradiction (component must be present AND absent), resolve it using separation principles
