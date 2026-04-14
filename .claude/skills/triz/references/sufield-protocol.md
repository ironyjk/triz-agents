# Su-Field (Substance-Field) Analysis Protocol

## Core Concept

Every technical function requires a minimal complete system of three elements:

- **S1** (Object substance) — the element being acted upon
- **S2** (Tool substance) — the element performing the action
- **F** (Field) — the energy/interaction that drives the action

This triad is the smallest unit capable of performing a function. If any element is missing, the system is incomplete and the function cannot occur.

## Field Types

Fields represent the type of energy or interaction between substances:

| Field | Examples |
|-------|----------|
| Mechanical (Fme) | Force, pressure, vibration, acoustic waves |
| Thermal (Fth) | Heat, cold, temperature gradients |
| Chemical (Fch) | Reactions, catalysis, dissolution, pH |
| Electrical (Fe) | Current, electrostatic, piezoelectric |
| Magnetic (Fmg) | Permanent magnets, electromagnets, ferrofluid |
| Electromagnetic (Fem) | Light, UV, IR, RF, microwave, laser |
| Gravitational (Fg) | Weight, centrifugal, buoyancy |

When selecting fields, prefer fields already present in the system or supersystem before introducing new ones. Controllable fields (electrical, magnetic, electromagnetic) are generally preferred over less controllable ones (gravitational, mechanical).

## Su-Field Model Types

### 1. Complete (Functional)

All three elements present. The system works as intended.

```
F
|
S1 --- S2
```

No modification needed unless improvement is desired.

### 2. Incomplete

One or more elements are missing. The function cannot be performed.

```
S1    (no S2 or F)
```

**Resolution**: Identify and supply the missing element(s) to complete the triad.

### 3. Harmful (Unwanted Effect)

The interaction produces an undesired result alongside or instead of the useful function.

```
F
|
S1 -~~ S2   (wavy line = harmful action)
```

**Resolution**: Introduce S3 to block the harmful interaction, modify F, or restructure the model.

### 4. Insufficient

The interaction exists but is too weak to produce adequate results.

```
F (weak)
|
S1 --- S2
```

**Resolution**: Intensify F, add a second field F2, modify S1 or S2 to increase responsiveness.

### 5. Excessive

The interaction is too strong, causing damage or waste.

```
F (excessive)
|
S1 === S2
```

**Resolution**: Introduce a buffer substance, reduce F, add a damping field.

## The 76 Standard Solutions — 5 Classes

### Class 1: Building and Destroying Su-Field Models (13 standards)

**Purpose**: Create a working Su-Field where none exists, or eliminate a harmful one.

Key patterns:
- **1.1 Build a complete Su-Field**: When the system is incomplete, add the missing S2 and/or F. Example: A part needs inspection (S1 exists) — add magnetic particles (S2) and a magnetic field (F) to reveal cracks.
- **1.2 Introduce an internal additive**: Modify S1 or S2 by adding a substance inside them. Example: Add abrasive particles to a cleaning fluid to increase cutting action.
- **1.3 Introduce an external additive**: Place S3 between S1 and S2. Example: Insert a lubricant layer between sliding surfaces to reduce friction.
- **1.4 Use the environment as S3**: Instead of introducing new substances, use what already exists (air, water, ambient heat).
- **1.5 Destroy harmful Su-Field**: Introduce S3 to absorb or redirect harmful F. Example: Add a shock absorber between a vibrating machine and a sensitive instrument.

**When to use**: The system does not perform the required function at all, or an existing interaction causes harm.

### Class 2: Developing Existing Su-Field Models (23 standards)

**Purpose**: Improve an existing but insufficient Su-Field by intensifying interactions or adding controllability.

Key patterns:
- **2.1 Chain Su-Field**: Add an intermediate S3 between S1 and S2 to transmit or amplify the field. Example: Use a lever (S3) to amplify mechanical force between tool and workpiece.
- **2.2 Double Su-Field**: Add a second field F2 to an existing model for better controllability. Example: Add ultrasonic vibration to a thermal welding process.
- **2.3 Transition to ferromagnetic substances**: Replace S1 or S2 with ferromagnetic versions to enable magnetic control. This is one of TRIZ's most powerful standard solutions — magnetic fields offer remote, precise, programmable control.
- **2.4 Use capillary/porous structures**: Replace solid substances with porous versions to increase surface area and enable field penetration.
- **2.5 Dynamization**: Make rigid elements flexible, segmented, or fluid to increase adaptability.

**When to use**: The system works but not well enough, not controllably enough, or not reliably enough.

### Class 3: System Transitions (6 standards)

**Purpose**: Transform the system to a higher level of organization.

Key patterns:
- **3.1 Transition to bi-system or poly-system**: Combine two identical or different systems to gain emergent properties. Example: Two single-blade razors → multi-blade system with superior performance.
- **3.2 Transition to inverse system**: Reverse the roles of elements or the direction of action. Example: Instead of moving a tool across a workpiece, move the workpiece past a stationary tool.
- **3.3 Macro-to-micro transition**: Replace macro-level mechanical action with micro-level field action. Example: Replace mechanical cutting with laser ablation.

**When to use**: The system has reached the limits of improvement within its current architecture.

### Class 4: Detection and Measurement Standards (17 standards)

**Purpose**: Solve problems of detection, measurement, and information gathering by restructuring them as Su-Field problems.

Key patterns:
- **4.1 Indirect measurement**: Instead of measuring a difficult parameter directly, measure a related parameter that changes proportionally. Example: Measure temperature by measuring electrical resistance of a thermocouple.
- **4.2 Add a detectable substance**: Introduce a tracer substance whose presence or concentration can be easily measured. Example: Add fluorescent dye to detect leaks.
- **4.3 Use field changes for measurement**: Detect changes in a field passing through the object rather than measuring the object directly. Example: Ultrasonic flaw detection.
- **4.4 Use resonance**: Measure frequency/amplitude changes at resonance for high sensitivity detection.

**When to use**: The problem is about sensing, detecting, or measuring rather than acting or transforming.

### Class 5: Helpers — Strategies for Introducing Substances and Fields (17 standards)

**Purpose**: Practical strategies for cases where introducing new substances or fields seems impossible due to constraints.

Key patterns:
- **5.1 Introduce substances indirectly**: Use void (bubbles, foam), fields that create temporary substances, or decomposable substances that leave no residue.
- **5.2 Introduce fields from available resources**: Use existing fields in the environment, by-product fields from other processes, or fields generated by the substances themselves.
- **5.3 Use phase transitions**: Leverage solid-liquid, liquid-gas, or other phase transitions as sources of both substances and fields. Example: Use ice → water transition for controlled expansion force.
- **5.4 Use physical effects**: Exploit known physical effects (piezoelectric, magnetostrictive, shape memory, Curie point) as ready-made Su-Field building blocks.
- **5.5 Use micro-level structures**: Use particles, molecules, ions, or atoms as S2 instead of macro-level components.

**When to use**: Constraints appear to prevent adding new elements to the system.

For the complete enumeration of all 76 standards, see [76-standards.md](76-standards.md).

## Application Process

### Phase 1: Model the Current System

1. Identify the **main useful function** (MUF) — what the system is supposed to do
2. Identify **S1** — the object being processed or acted upon
3. Identify **S2** — the tool or component performing the action
4. Identify **F** — the energy or field driving the interaction
5. Draw the Su-Field diagram

### Phase 2: Identify the Problem Type

Classify as one of:
- **Incomplete**: Missing element(s) — function not performed
- **Harmful**: Unwanted secondary effect present
- **Insufficient**: Function performed too weakly
- **Excessive**: Function performed too strongly
- **Measurement**: Need to detect/measure rather than transform

### Phase 3: Select the Standard Solution Class

| Problem Type | Primary Class | Secondary Class |
|-------------|---------------|-----------------|
| Incomplete | Class 1 | Class 5 (if constrained) |
| Harmful | Class 1 (destroy) | Class 2 (shield) |
| Insufficient | Class 2 | Class 3 (architecture) |
| Excessive | Class 1 (buffer) | Class 2 (control) |
| Measurement | Class 4 | Class 2 (add detectability) |

### Phase 4: Generate Specific Solutions

1. Review the relevant standards within the selected class
2. Map each standard's abstract pattern onto the specific problem substances and fields
3. Generate 3-5 concrete solution concepts
4. Evaluate each against the Ideal Final Result (see ifr-protocol.md)
5. Select the most promising concepts for development

## Integration with Other TRIZ Tools

- **IFR**: After generating Su-Field solutions, evaluate how close each comes to the Ideal Final Result
- **Resources**: Use resource analysis to identify candidate substances and fields already available in the system
- **Trimming**: Su-Field analysis can reveal which components are essential (load-bearing in the Su-Field model) and which are candidates for trimming
- **Evolution**: Su-Field models evolve along predictable lines (mechanical → electromagnetic → micro-level), use evolution patterns to guide field selection

## Common Pitfalls

1. **Skipping the model step**: Jumping to solutions without first drawing the Su-Field diagram leads to incomplete analysis
2. **Ignoring existing fields**: Systems always contain multiple fields — map all of them before introducing new ones
3. **Over-specifying S2**: Keep S2 abstract initially (a "substance that does X") before committing to a specific material
4. **Neglecting harmful secondary effects**: Every new element introduced can create new harmful interactions — model those too
5. **Single-solution fixation**: The standards typically suggest multiple directions — generate several before evaluating
