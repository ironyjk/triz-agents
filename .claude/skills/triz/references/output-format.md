# Output Format Specification

All TRIZ tools render their output in two formats: Mermaid (default) and ASCII.

## Format Selection

- Default: `mermaid` — renders in GitHub, VS Code, and most Markdown viewers
- Alternative: `ascii` — universal text fallback, works everywhere
- Controlled by `--format mermaid|ascii` argument

## Color Conventions (Mermaid)

| Element | Color | Style Code |
|---------|-------|-----------|
| Problem / Contradiction | Coral red | `fill:#e17055,color:#fff` |
| Root Contradiction | Dark red, thick border | `fill:#d63031,color:#fff,stroke-width:3px` |
| Inventive Principle | Green, thick border | `fill:#00b894,color:#fff,stroke-width:3px` |
| Solution / IFR | Teal | `fill:#00cec9,color:#fff` |
| Harmful Effect / Function | Yellow warning | `fill:#fdcb6e,color:#000` |
| Resource | Purple | `fill:#6c5ce7,color:#fff` |
| Substance | Light blue | `fill:#74b9ff,color:#fff` |
| Field | Orange | `fill:#e17055,color:#fff` |
| Useful Function | Default | (no special styling) |
| Evolution Stage (current) | Dark blue | `fill:#0984e3,color:#fff` |
| Evolution Stage (past) | Light gray-blue | `fill:#b2bec3,color:#fff` |
| Evolution Stage (future) | Teal, dashed | `fill:#00cec9,color:#fff,stroke-dasharray:5` |
| AND connector | Gray diamond | `fill:#b2bec3,color:#fff` |
| Trimmed component | Red, dashed border | `fill:#fff,color:#d63031,stroke:#d63031,stroke-dasharray:5` |

## Mermaid Templates

### Technical Contradiction Diagram

Direction: `graph LR` (left-to-right — improving parameter on left, worsening on right)

```mermaid
graph LR
    SYS["<b>SYSTEM</b><br/>Wing design"]
    IP["<b>IMPROVING</b><br/>#9 Speed"]
    WP["<b>WORSENING</b><br/>#1 Weight of moving object"]
    TC["<b>TECHNICAL<br/>CONTRADICTION</b><br/>Faster wing requires<br/>heavier structure"]
    P1["<b>P#1</b> Segmentation"]
    P2["<b>P#15</b> Dynamization"]
    P3["<b>P#29</b> Pneumatics/Hydraulics"]

    SYS --> TC
    TC --> IP
    TC --> WP
    TC -.-> P1
    TC -.-> P2
    TC -.-> P3

    style TC fill:#d63031,color:#fff,stroke-width:3px
    style IP fill:#e17055,color:#fff
    style WP fill:#e17055,color:#fff
    style P1 fill:#00b894,color:#fff,stroke-width:3px
    style P2 fill:#00b894,color:#fff,stroke-width:3px
    style P3 fill:#00b894,color:#fff,stroke-width:3px
```

### Physical Contradiction Diagram

Direction: `graph TB` (top-to-bottom — element at top, opposing requirements below)

```mermaid
graph TB
    ELEM["<b>ELEMENT</b><br/>Wing surface"]
    REQ_A["Must be <b>RIGID</b><br/>to bear aerodynamic load"]
    REQ_B["Must be <b>FLEXIBLE</b><br/>to adapt to turbulence"]
    PC["<b>PHYSICAL<br/>CONTRADICTION</b>"]
    SEP["<b>SEPARATION</b><br/>In structure: rigid core +<br/>flexible skin"]
    SOL["<b>SOLUTION</b><br/>Composite wing with<br/>morphing trailing edge"]

    ELEM --> REQ_A
    ELEM --> REQ_B
    REQ_A <-. "CONFLICT" .-> REQ_B
    PC --> SEP
    SEP --> SOL

    style ELEM fill:#74b9ff,color:#fff
    style REQ_A fill:#e17055,color:#fff
    style REQ_B fill:#e17055,color:#fff
    style PC fill:#d63031,color:#fff,stroke-width:3px
    style SEP fill:#00b894,color:#fff,stroke-width:3px
    style SOL fill:#00cec9,color:#fff
```

### Su-Field Model

Direction: `graph TB` (top-to-bottom — field at top, substances below)

```mermaid
graph TB
    F1["<b>FIELD</b><br/>Mechanical"]
    S1["<b>S1</b><br/>Tool (drill bit)"]
    S2["<b>S2</b><br/>Object (workpiece)"]

    F1 --> S1
    S1 -->|"useful action"| S2
    S1 -.->|"harmful: heat"| S2

    style F1 fill:#e17055,color:#fff
    style S1 fill:#74b9ff,color:#fff
    style S2 fill:#74b9ff,color:#fff
```

Incomplete Su-Field (problem):
```mermaid
graph TB
    F1["<b>FIELD</b><br/>???"]
    S1["<b>S1</b><br/>Tool"]
    S2["<b>S2</b><br/>Object"]

    F1 -.->|"missing"| S1
    S1 -.->|"insufficient"| S2

    style F1 fill:#e17055,color:#fff,stroke-dasharray:5
    style S1 fill:#74b9ff,color:#fff
    style S2 fill:#74b9ff,color:#fff
```

### Evolution S-Curve

Direction: `graph LR` (left-to-right — time progression)

```mermaid
graph LR
    S1["<b>BIRTH</b><br/>Invention<br/>Low performance"]
    S2["<b>GROWTH</b><br/>Rapid improvement<br/>Many patents"]
    S3["<b>MATURITY</b><br/>Diminishing returns<br/>Optimization patents"]
    S4["<b>DECLINE</b><br/>Replaced by<br/>next S-curve"]
    CURR["<b>YOU ARE HERE</b>"]

    S1 --> S2 --> S3 --> S4
    CURR -.-> S3

    style S1 fill:#b2bec3,color:#fff
    style S2 fill:#b2bec3,color:#fff
    style S3 fill:#0984e3,color:#fff
    style S4 fill:#00cec9,color:#fff,stroke-dasharray:5
    style CURR fill:#d63031,color:#fff,stroke-width:3px
```

### Trimming — Before and After

Direction: `graph LR` (left-to-right — before on left, after on right)

```mermaid
graph LR
    subgraph BEFORE["Before Trimming"]
        A1["Component A"]
        B1["Component B<br/>(to be trimmed)"]
        C1["Component C"]
        A1 -->|"function 1"| C1
        B1 -->|"function 2"| C1
    end
    subgraph AFTER["After Trimming"]
        A2["Component A<br/>(absorbs function 2)"]
        C2["Component C"]
        A2 -->|"function 1 + 2"| C2
    end

    BEFORE --> AFTER

    style B1 fill:#fff,color:#d63031,stroke:#d63031,stroke-dasharray:5
    style A2 fill:#00b894,color:#fff,stroke-width:3px
```

### Ideal Final Result (IFR)

Direction: `graph BT` (bottom-to-top — current state at bottom, IFR at top)

```mermaid
graph BT
    CURR["<b>CURRENT STATE</b><br/>System with 5 components<br/>3 harmful effects"]
    GAP1["<b>GAP</b><br/>Excessive complexity"]
    GAP2["<b>GAP</b><br/>Harmful vibration"]
    IFR["<b>IDEAL FINAL RESULT</b><br/>The part ITSELF eliminates vibration<br/>using only available resources"]
    PC["<b>PHYSICAL CONTRADICTION</b><br/>Must be rigid AND flexible"]
    SOL["<b>SOLUTION</b><br/>Viscoelastic damper<br/>integrated into mount"]

    CURR --> GAP1
    CURR --> GAP2
    GAP1 --> IFR
    GAP2 --> IFR
    IFR --> PC
    PC --> SOL

    style CURR fill:#e17055,color:#fff
    style GAP1 fill:#fdcb6e,color:#000
    style GAP2 fill:#fdcb6e,color:#000
    style IFR fill:#00cec9,color:#fff,stroke-width:3px
    style PC fill:#d63031,color:#fff,stroke-width:3px
    style SOL fill:#00b894,color:#fff,stroke-width:3px
```

### ARIZ Flow

Direction: `graph TB` (top-to-bottom — sequential phases)

```mermaid
graph TB
    P1["<b>Part 1</b><br/>Analyze the problem<br/>Mini-problem, TC, IFR"]
    P2["<b>Part 2</b><br/>Analyze resources<br/>Substance-field resources"]
    P3["<b>Part 3</b><br/>Define IFR &<br/>Physical Contradiction"]
    P4["<b>Part 4</b><br/>Mobilize resources<br/>Apply separation principles"]
    P5["<b>Part 5</b><br/>Apply knowledge base<br/>Effects, standards"]
    P6["<b>Part 6</b><br/>Change the problem<br/>if unsolved"]
    P7["<b>Part 7</b><br/>Evaluate solution"]

    P1 --> P2 --> P3 --> P4 --> P5
    P5 -->|"solved"| P7
    P5 -->|"unsolved"| P6
    P6 -.->|"reformulate"| P1

    style P1 fill:#e17055,color:#fff
    style P3 fill:#d63031,color:#fff,stroke-width:3px
    style P4 fill:#00b894,color:#fff,stroke-width:3px
    style P7 fill:#00cec9,color:#fff
```

### Resource Map

Direction: `graph TB` (top-to-bottom — system at center, resources around)

```mermaid
graph TB
    SYS["<b>SYSTEM</b><br/>Drilling operation"]
    RS1["<b>SUBSTANCE</b><br/>Coolant already<br/>in system"]
    RS2["<b>FIELD</b><br/>Vibration from<br/>motor"]
    RS3["<b>SPACE</b><br/>Hollow drill<br/>shaft interior"]
    RS4["<b>TIME</b><br/>Idle time between<br/>drilling cycles"]
    RS5["<b>INFO</b><br/>Temperature signal<br/>from bit wear"]

    SYS --- RS1
    SYS --- RS2
    SYS --- RS3
    SYS --- RS4
    SYS --- RS5

    style SYS fill:#0984e3,color:#fff,stroke-width:3px
    style RS1 fill:#6c5ce7,color:#fff
    style RS2 fill:#6c5ce7,color:#fff
    style RS3 fill:#6c5ce7,color:#fff
    style RS4 fill:#6c5ce7,color:#fff
    style RS5 fill:#6c5ce7,color:#fff
```

## ASCII Templates

### Technical Contradiction
```
═══ TECHNICAL CONTRADICTION ═══

SYSTEM: Wing design

  IMPROVING: #9 Speed ──────┐
                             ├──→ [TC] Faster wing requires heavier structure
  WORSENING: #1 Weight ─────┘
                               │
                    ┌──────────┴──────────┐
                    ↓          ↓          ↓
               [P#1]      [P#15]     [P#29]
            Segmentation  Dynamize   Pneumatics

Contradiction Pair: #9 vs #1
Suggested Principles: 1, 15, 29
```

### Physical Contradiction
```
═══ PHYSICAL CONTRADICTION ═══

ELEMENT: Wing surface

  Must be RIGID ──────┐
                      ├──→ CONFLICT
  Must be FLEXIBLE ───┘

SEPARATION: In structure
  → Rigid core + flexible skin

SOLUTION: Composite wing with morphing trailing edge
```

### Su-Field Model
```
═══ SU-FIELD MODEL ═══

       [F] Mechanical
        │
        ↓
   [S1] Drill bit ──→ [S2] Workpiece
        │    useful action
        └ ─ ─ ─ ─ ─ → [S2]
             harmful: heat

Type: Complete, with harmful side-effect
Standard Solution: Introduce S3 to absorb harmful effect
```

### Evolution S-Curve
```
═══ EVOLUTION S-CURVE ═══

Performance
    │            ___________
    │           /           \  ← DECLINE
    │          / ← MATURITY  \
    │         /  ★ YOU ARE    \
    │        /    HERE         \
    │       / ← GROWTH          \
    │      /                     \
    │_____/ ← BIRTH               \___
    └──────────────────────────────────→ Time

Stage: MATURITY — diminishing returns, optimize or transition
```

### Trimming
```
═══ TRIMMING ═══

BEFORE:                          AFTER:
┌─────────┐  func1  ┌─────┐    ┌─────────┐  func1+2  ┌─────┐
│    A     │──────→│  C  │    │ A (new) │─────────→│  C  │
└─────────┘        └─────┘    └─────────┘          └─────┘
┌ ─ ─ ─ ─ ┐ func2    ↑
│    B     │──────────┘       B removed — function 2 absorbed by A
└ ─ ─ ─ ─ ┘
  (trimmed)

Components: 3 → 2 (trimmed 1)
Functions preserved: 2/2
```

### Ideal Final Result
```
═══ IDEAL FINAL RESULT ═══

CURRENT STATE: System with 5 components, 3 harmful effects

  [GAP] Excessive complexity
  [GAP] Harmful vibration
       ↓
  [IFR] The part ITSELF eliminates vibration
        using only available resources
       ↓
  [PC]  Must be RIGID and FLEXIBLE
       ↓
  [SOLUTION] Viscoelastic damper integrated into mount

Ideality: +45% (2 components removed, 1 harm eliminated)
```

### ARIZ Flow
```
═══ ARIZ FLOW ═══

Part 1: Analyze Problem
  → Mini-problem → TC → IFR
      ↓
Part 2: Analyze Resources
  → Substance/field resources in zone
      ↓
Part 3: Define IFR + Physical Contradiction
  → "X-element must be ___ and not-___"
      ↓
Part 4: Mobilize Resources
  → Apply separation principles
      ↓
Part 5: Apply Knowledge Base
  → Effects database, 76 standards
      ↓
  solved? ──→ Part 7: Evaluate Solution
  unsolved? → Part 6: Reformulate → back to Part 1
```

### Resource Map
```
═══ RESOURCE MAP ═══

              ┌─────────────────┐
              │     SYSTEM      │
              │  Drilling op.   │
              └───────┬─────────┘
       ┌──────────┬───┴───┬──────────┐
       ↓          ↓       ↓          ↓
  [SUBSTANCE]  [FIELD]  [SPACE]   [TIME]
   Coolant     Vibration  Hollow   Idle
   in system   from motor shaft    cycles

  [INFO] Temperature signal from bit wear

Resources found: 5
Unused resources: 3 (vibration, hollow shaft, idle cycles)
```

## Rendering Rules

1. **Always include a title** — `═══ TOOL NAME ═══` for ASCII, `%% Tool: NAME` comment for Mermaid
2. **Always include a summary** after the diagram with key counts (contradictions, principles, resources, etc.)
3. **Mermaid node IDs** — use short, semantic names (TC1, PC1, IP1, WP1, P1, S1, F1, SOL1, etc.)
4. **Mermaid line breaks** — use `<br/>` for multi-line node text
5. **Bold labels** — use `<b>LABEL</b>` in Mermaid for entity type labels
6. **Conflict arrows** — always dotted: `<-. "CONFLICT" .->`
7. **Harmful function arrows** — always dotted: `-.->|"harmful: description"|`
8. **Suggested principle arrows** — dotted from contradiction to principle: `-.->` 
9. **Normal arrows** — solid: `-->` (confirmed function, causal link)
10. **Missing/incomplete elements** — use `stroke-dasharray:5` for dashed borders
11. **Maximum nodes per diagram** — shallow: 8-12, deep: 15-25. Split into sub-diagrams if needed.
12. **Principle cards** — when listing principles in detail, use this format:

```
┌─────────────────────────────────────┐
│ P#15 DYNAMIZATION                   │
│─────────────────────────────────────│
│ Make object/environment adaptive    │
│ so performance is optimal at        │
│ each operating stage.               │
│                                     │
│ Applied: Variable-geometry wing     │
│ adjusts sweep angle to flight speed │
└─────────────────────────────────────┘
```

13. **Solution evaluation** — always include feasibility, novelty, and ideality delta:

```
SOLUTION ASSESSMENT:
  Inventive Level: 3 (major improvement)
  Ideality Change: +40% (fewer parts, same function)
  Feasibility: High — existing materials
  Domain Source: Aerospace → applied to HVAC
```
