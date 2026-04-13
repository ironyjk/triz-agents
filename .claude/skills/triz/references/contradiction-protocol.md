# Contradiction Protocol

Identifies and formulates Technical and Physical Contradictions — the core problem-modeling step in TRIZ. Every TRIZ solution begins with a well-formulated contradiction.

Based on Altshuller's contradiction analysis methodology from "Creativity as an Exact Science" (1984) and ARIZ-85C.

## When This Tool Applies

- A system improvement creates a new problem or worsens another parameter
- A tradeoff seems unavoidable ("we can't have both X and Y")
- Optimization has plateaued — incremental improvement no longer works
- A design parameter needs to be both large and small, hot and cold, present and absent
- A system is being designed and the designer wants to find the real inventive problem

## Core Concepts

### Technical Contradiction (TC)

Two system parameters are coupled: improving one worsens the other.

**Template:** "If we improve [Parameter A], then [Parameter B] worsens."

A TC always has TWO forms (the contradiction pair):
- TC-1: "If we increase X, then Y worsens"
- TC-2: "If we decrease X (to protect Y), then X-dependent function suffers"

**Both forms must be stated.** The contradiction pair reveals the full problem space.

### Physical Contradiction (PC)

A single system element must possess two mutually exclusive properties.

**Template:** "[Element] must be [Property] in order to [useful function], AND must be [anti-Property] in order to [another useful function or avoid harm]."

A PC is **always sharper** than a TC. Every TC can be deepened into a PC by asking: "What specific element is responsible for both the improvement and the worsening?"

### TC → PC Sharpening

```
TC: "Increasing wall thickness improves strength but worsens weight"
     ↓ Ask: what element causes both?
     ↓ The WALL must be thick AND thin
PC: "The wall must be THICK to bear load AND THIN to minimize weight"
     ↓ This directly suggests separation solutions
```

---

## Phase 1: System Analysis

Before identifying contradictions, understand the system.

### Step 1.1 — Define the System

| Question | Answer |
|----------|--------|
| What is the system? | Name and brief description |
| What is its primary useful function (PUF)? | The main reason the system exists |
| What is the super-system? | The larger system it belongs to |
| What is the sub-system? | Key internal components |
| Who/what is the object? | What the system acts upon |

### Step 1.2 — Component Analysis

List all components and their roles:

```
COMPONENT LIST:
  1. [Component A] — delivers function X to [object]
  2. [Component B] — supports Component A
  3. [Component C] — provides energy/field to system
  ...
```

### Step 1.3 — Function Analysis

For each component pair, identify interactions:

| Subject | Action | Object | Type |
|---------|--------|--------|------|
| Drill bit | removes material from | Workpiece | Useful (primary) |
| Drill bit | heats | Workpiece | Harmful |
| Coolant | cools | Drill bit | Useful (auxiliary) |
| Coolant | washes away | Chips | Useful (auxiliary) |
| Coolant | corrodes | Workpiece surface | Harmful |

Function types: **Useful** (primary, auxiliary), **Harmful**, **Insufficient**, **Excessive**

### Step 1.4 — Identify the Problem Area

From the function analysis, identify where problems cluster:

- Which functions are insufficient or excessive?
- Which harmful functions are most damaging?
- Which useful functions conflict with each other?
- Where is the system failing to meet requirements?

---

## Phase 2: Technical Contradiction Identification

### Step 2.1 — Formulate TC Pairs

From the problem area, identify the conflicting parameters.

**Process:**
1. What parameter do we want to improve? (Map to one of the 39 engineering parameters)
2. What parameter worsens as a result? (Map to another of the 39 parameters)
3. State both TC forms

**Format:**
```
TC-1 (improving action):
  IF we [action to improve Parameter A]
  THEN [Parameter B worsens]
  BECAUSE [causal mechanism]

TC-2 (counter-action):
  IF we [action to protect Parameter B]
  THEN [Parameter A suffers / original problem returns]
  BECAUSE [causal mechanism]
```

### Step 2.2 — Map to 39 Parameters

Identify the improving and worsening parameters from the standard 39-parameter list. This enables Contradiction Matrix lookup.

**Example:**
```
Improving: #9 Speed
Worsening: #1 Weight of moving object
→ Matrix lookup: Principles 2, 28, 13, 38
```

If the problem doesn't map cleanly to engineering parameters, use **analogical mapping**: find the closest abstract parameter that captures the essence.

### Step 2.3 — Validate the TC

Checklist:
- [ ] Both TC-1 and TC-2 are stated
- [ ] The conflict is REAL, not just assumed (evidence exists)
- [ ] The parameters are correctly mapped to the 39-parameter list
- [ ] The causal mechanism is understood (not just "it happens")
- [ ] The TC is at the right level of abstraction — not too specific, not too vague

**Common error:** Stating a TC that is actually a tradeoff accepted by the industry. A real TC should describe a situation where existing solutions are unsatisfactory.

### Step 2.4 — Multiple TCs

Complex problems often contain multiple technical contradictions. List all of them, then prioritize:

1. **Primary TC** — the one most directly blocking the goal
2. **Secondary TCs** — other conflicts that contribute to the problem
3. **Derived TCs** — contradictions that emerge from attempts to solve the primary TC

Solve the primary TC first. Often, secondary TCs dissolve when the primary is resolved.

---

## Phase 3: Physical Contradiction Formulation

### Step 3.1 — Identify the Critical Element

Ask: "What single physical element is at the center of both the improvement and the worsening?"

This element must perform (or possess) two opposing properties.

**Probing questions:**
- What part of the system directly creates the useful effect?
- What part of the same system directly creates the harmful effect?
- Is it the same part? The same material? The same surface?

### Step 3.2 — State the Physical Contradiction

**Template:**
```
[Element] must be [Property X]
  in order to [Function/Benefit requiring X]
AND
[Element] must be [NOT Property X / anti-X]
  in order to [Function/Benefit requiring anti-X]
```

**Validation:**
- [ ] The element is specific (not "the system" — a specific component, surface, material, parameter)
- [ ] The properties are genuinely opposite (not merely different)
- [ ] Both requirements are necessary (not just desirable)
- [ ] The contradiction is at the PHYSICAL level (size, temperature, state, position, etc.)

### Step 3.3 — Identify Separation Strategy

Physical contradictions are resolved by **separation**:

| Separation Type | When to Use | Example |
|-----------------|-------------|---------|
| **In Time** | Requirements occur at different times | Retractable landing gear: extended for landing, retracted in flight |
| **In Space** | Requirements apply to different locations | Knife: sharp at edge, thick at spine |
| **In Condition** | Requirements depend on different conditions | Thermostat bimetallic strip: bends when hot, straight when cold |
| **In Scale** | Requirements apply at different system levels | Bicycle chain: rigid links (macro) + flexible assembly (macro-structure) |

**Probing questions for each:**
- Does the element need Property X at ALL times, or only sometimes? → Separation in Time
- Does the element need Property X EVERYWHERE, or only in certain zones? → Separation in Space
- Does the element need Property X under ALL conditions? → Separation in Condition
- Does the element need Property X at ALL scales (micro/macro)? → Separation in Scale

### Step 3.4 — Generate Solution Directions

Each separation strategy suggests specific solution approaches:

**In Time:** phase change, pre-action, periodic action, rushing through
**In Space:** composite materials, local quality, nesting, thin films
**In Condition:** smart materials, responsive systems, self-adjusting mechanisms
**In Scale:** micro-structure, nano-coatings, porous materials, foams

---

## Phase 4: Output

### Diagram

Render the contradiction analysis using the templates from `output-format.md`.

For Technical Contradictions: TC diagram with parameter mapping and suggested principles.
For Physical Contradictions: PC diagram with element, opposing requirements, and separation strategy.

### Summary

```
═══ CONTRADICTION ANALYSIS SUMMARY ═══

SYSTEM: [system name]
PRIMARY USEFUL FUNCTION: [PUF]

TECHNICAL CONTRADICTIONS:
  TC-1: IF [improve A] THEN [B worsens]
  TC-2: IF [protect B] THEN [A suffers]
  Improving Parameter: #[N] [name]
  Worsening Parameter: #[N] [name]

PHYSICAL CONTRADICTION:
  Element: [element]
  Must be: [X] for [reason]
  Must be: [anti-X] for [reason]

SEPARATION STRATEGY: [time/space/condition/scale]

SUGGESTED PRINCIPLES: [from matrix lookup]

NEXT STEP:
  → Apply principles: /triz:40p [contradiction]
  → Full matrix lookup: /triz:matrix [improving] [worsening]
  → Deep solve: /triz:ariz [problem]
```

---

## Anti-Patterns

| Anti-Pattern | Why It's Wrong | Fix |
|-------------|---------------|-----|
| TC is vague: "quality vs cost" | Too abstract to solve | Specify: "surface roughness < 0.8um requires slower feed rate, reducing throughput" |
| PC element is "the system" | Not specific enough to separate | Drill down: which component? Which surface? Which dimension? |
| Only one TC form stated | Missing half the problem space | Always state BOTH TC-1 and TC-2 |
| Properties aren't truly opposite | Not a real physical contradiction | Test: can you have both simultaneously? If yes, not a PC |
| Jumping to separation without full PC | May pick wrong separation type | Complete the PC formulation first, then analyze which separation fits |
| Accepting the tradeoff | TRIZ rejects compromise — seek elimination | Ask: "What if we could have BOTH? What assumption makes that impossible?" |
| Confusing TC with optimization | Optimization = improve within current concept; TC = concept limit reached | If incremental improvement works, it's not a TC — just optimize |

---

## Domain-Specific Guidance

### Mechanical/Structural Engineering
- Parameters map naturally to the 39-parameter list
- Physical contradictions often involve material properties (strength/weight, hardness/flexibility)
- Separation in space and scale are most common (composites, variable cross-sections)

### Chemical/Process Engineering
- TCs often involve reaction rate vs selectivity, temperature vs catalyst life
- PCs involve concentrations, pH, temperatures that need to be high AND low
- Separation in time (batch sequencing) and condition (catalysts, membranes) dominate

### Software Engineering
- TCs: performance vs memory, security vs usability, coupling vs cohesion, flexibility vs simplicity
- PCs: "The API must be stable (for consumers) AND change frequently (for new features)"
- Map to abstract parameters: speed → #9, complexity → #36, adaptability → #35
- Separation in time (versioning), space (modules), condition (feature flags), scale (microservices)

### Business / Operations
- TCs: cost vs quality, speed vs reliability, customization vs standardization
- PCs: "Price must be HIGH (for margins) AND LOW (for market share)"
- Separation in space (market segments), condition (value tiers), time (introductory pricing)

### Electronics / Embedded
- TCs: power vs performance, size vs heat dissipation, frequency vs noise
- PCs: "Signal must be STRONG (for range) AND WEAK (for interference compliance)"
- Separation in time (duty cycle), space (directional antenna), scale (frequency spreading)

---

## Handoff

### Receives From
- Direct user problem statement
- Function analysis output
- ARIZ Part 1 (mini-problem formulation)

### Passes To
- **40 Principles** (`/triz:40p`): TC with improving/worsening parameter numbers
- **Matrix** (`/triz:matrix`): Parameter pair for principle lookup
- **ARIZ** (`/triz:ariz`): PC formulation for deep algorithmic solving
- **Su-Field** (`/triz:sufield`): Function model for standard solutions

Output format for handoff:
```
CONTRADICTION FOR NEXT TOOL:
  Type: TC | PC
  TC Improving: #[N] [name]
  TC Worsening: #[N] [name]
  PC Element: [element]
  PC Property: [X] vs [anti-X]
  Separation Hint: [time/space/condition/scale if identified]
  Context: [brief problem context for solution generation]
```
