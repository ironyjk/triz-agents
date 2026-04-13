# Contradiction Matrix Protocol

Maps technical contradictions to recommended inventive principles using Altshuller's 39x39 Contradiction Matrix. The matrix encodes statistical patterns from ~40,000 patents: for each pair of conflicting engineering parameters, it recommends the 2-4 principles most frequently used to resolve that conflict.

## When This Tool Applies

- A technical contradiction has been identified with specific improving/worsening parameters
- The user wants principle recommendations based on statistical patent analysis
- Systematic exploration of solution space (vs. intuitive principle selection)
- As the standard intermediate step between contradiction identification and principle application

---

## The 39 Engineering Parameters

These parameters abstract all physical and engineering characteristics. Map your specific problem parameters to the closest match.

### Group 1: Physical Parameters (1-10)

| # | Parameter | Description |
|---|-----------|-------------|
| 1 | **Weight of moving object** | Mass of the object in motion, including contained substances. Gravitational force the object exerts on its support. |
| 2 | **Weight of stationary object** | Mass of the object at rest. Includes objects whose function is performed while stationary. |
| 3 | **Length of moving object** | Any linear dimension (length, width, height, diameter) of a moving object. |
| 4 | **Length of stationary object** | Any linear dimension of a stationary object. |
| 5 | **Area of moving object** | External or internal surface area of a moving object. Cross-sectional area. |
| 6 | **Area of stationary object** | External or internal surface area of a stationary object. |
| 7 | **Volume of moving object** | Cubic measure of space occupied by a moving object. |
| 8 | **Volume of stationary object** | Cubic measure of space occupied by a stationary object. |
| 9 | **Speed** | Rate of change of position. Velocity of an object. Process speed or throughput rate. |
| 10 | **Force (intensity)** | Mechanical force, interaction intensity. Capacity to do work per unit action. |

### Group 2: Physical Parameters (11-18)

| # | Parameter | Description |
|---|-----------|-------------|
| 11 | **Stress or pressure** | Force per unit area. Tension, compression, or shear stress. |
| 12 | **Shape** | External contour or profile. Appearance of the object. |
| 13 | **Stability of composition** | Integrity of the system. Resistance to changes in internal structure or chemical composition. |
| 14 | **Strength** | Resistance to breaking, deformation, or failure under load. Structural integrity. |
| 15 | **Duration of action of moving object** | Service life, durability, mean time between failures — for a moving object. |
| 16 | **Duration of action of stationary object** | Service life, durability, mean time between failures — for a stationary object. |
| 17 | **Temperature** | Thermal condition. Temperature of the object or process. Thermal gradient. |
| 18 | **Illumination intensity** | Light flux per unit area. Luminous energy. Includes any radiation quality. |

### Group 3: Performance Parameters (19-26)

| # | Parameter | Description |
|---|-----------|-------------|
| 19 | **Use of energy by moving object** | Energy consumed by the moving object to perform its function. |
| 20 | **Use of energy by stationary object** | Energy consumed by the stationary object. |
| 21 | **Power** | Rate of energy usage. Work done per unit time. Output capacity. |
| 22 | **Loss of energy** | Wasted energy. Energy that does not contribute to the function. Efficiency loss. |
| 23 | **Loss of substance** | Material waste. Leakage, evaporation, erosion, wear of material. |
| 24 | **Loss of information** | Data loss, signal degradation, information entropy. Partial or total. |
| 25 | **Loss of time** | Wasted time. Idle time, setup time, waiting time, delays. |
| 26 | **Quantity of substance/matter** | Amount of material used. Number of items. Material consumption. |

### Group 4: System Parameters (27-35)

| # | Parameter | Description |
|---|-----------|-------------|
| 27 | **Reliability** | Probability that the system performs its function under stated conditions. MTBF. Failure rate. |
| 28 | **Measurement accuracy** | Precision of measurement. Closeness of measured value to true value. Resolution. |
| 29 | **Manufacturing precision** | Tolerance. Accuracy of fabrication. Closeness to specified dimensions. |
| 30 | **Object-affected harmful factors** | Susceptibility to external harmful effects (environmental, operational). |
| 31 | **Object-generated harmful factors** | Harmful outputs: noise, vibration, pollution, radiation, side-effects. |
| 32 | **Ease of manufacture** | Simplicity and convenience of fabrication. Number of operations, skill level required. |
| 33 | **Ease of operation** | Usability. Simplicity of use. Convenience for the operator. Accessibility. |
| 34 | **Ease of repair** | Maintainability. Speed and simplicity of fault diagnosis and correction. |
| 35 | **Adaptability or versatility** | Ability to respond to external changes. Flexibility. Multi-functionality. |

### Group 5: System Parameters (36-39)

| # | Parameter | Description |
|---|-----------|-------------|
| 36 | **Device complexity** | Number and diversity of elements. Sophistication of system structure. |
| 37 | **Difficulty of detecting and measuring** | Complexity of inspection, monitoring, testing. Observability of system state. |
| 38 | **Extent of automation** | Degree of autonomous operation without human intervention. |
| 39 | **Productivity** | Number of functions or operations per unit time. Output rate. Throughput. |

---

## Parameter Mapping Guide

### Direct Mapping

When the problem parameter directly matches a listed parameter:
- "The product is too heavy" → #1 or #2 (moving or stationary)
- "It's too slow" → #9 Speed
- "It breaks under load" → #14 Strength
- "Manufacturing is too complex" → #32 Ease of manufacture

### Analogical Mapping

When the problem is non-mechanical, find the closest abstract analogy:

| Domain Problem | Maps To |
|---------------|---------|
| Software latency | #9 Speed |
| Code complexity | #36 Device complexity |
| Memory consumption | #26 Quantity of substance |
| Bug rate / defects | #27 Reliability |
| Security vulnerabilities | #30 Object-affected harmful factors |
| Resource leaks | #23 Loss of substance |
| Scalability | #35 Adaptability |
| Build time | #25 Loss of time |
| API surface area | #5 or #6 Area |
| Power consumption | #19 or #20 Use of energy |
| Data loss | #24 Loss of information |
| Noise / log spam | #31 Object-generated harmful factors |
| Test coverage | #28 Measurement accuracy |
| Deployment difficulty | #33 Ease of operation |
| Maintenance burden | #34 Ease of repair |
| Feature count | #36 Device complexity |
| Automation level | #38 Extent of automation |
| Throughput / requests/sec | #39 Productivity |

### Business / Operations Mapping

| Business Problem | Maps To |
|-----------------|---------|
| Revenue / output volume | #39 Productivity |
| Cost / expense | #19 or #20 Use of energy |
| Quality defects | #27 Reliability |
| Time-to-market | #9 Speed |
| Customer satisfaction | #33 Ease of operation |
| Employee count needed | #26 Quantity of substance |
| Organizational complexity | #36 Device complexity |
| Market adaptability | #35 Adaptability |
| Waste / scrap | #23 Loss of substance |
| Downtime | #25 Loss of time |
| Compliance burden | #30 Object-affected harmful factors |
| Environmental impact | #31 Object-generated harmful factors |

---

## The Matrix Lookup Process

### Full 39x39 Matrix

The complete Contradiction Matrix is a 39-row x 39-column table where:
- **Rows** = Improving parameter (what you want to make better)
- **Columns** = Worsening parameter (what degrades as a result)
- **Cells** = 2-4 recommended inventive principle numbers

Since embedding the full 1,521-cell matrix is impractical in this format, the LLM uses its trained knowledge of the matrix contents. The matrix is well-documented in TRIZ literature and the LLM has been exposed to it extensively.

### LLM-Assisted Lookup

When given an improving/worsening parameter pair, the process is:

1. **Verify parameter mapping** — confirm the parameters are correctly identified
2. **Recall matrix recommendations** — use knowledge of the matrix to identify the statistically most-recommended principles
3. **Cross-validate** — check recommendations against domain knowledge and known solutions
4. **Supplement if needed** — if the matrix cell is empty or the recommendations feel incomplete, add principles from adjacent cells or domain expertise

**Confidence levels:**
- **High confidence:** Classic parameter pairs (speed vs weight, strength vs weight, etc.) — matrix recommendations well-established
- **Medium confidence:** Less common pairs or analogical mappings — principles likely correct but verify
- **Low confidence:** Highly abstract or non-engineering mappings — treat as starting points, not definitive

---

## Application Process

### Step 1 — Identify Parameter Pair

From the technical contradiction:
```
TC: "If we improve [A], then [B] worsens"
  Improving parameter: [identify from 39 list]
  Worsening parameter: [identify from 39 list]
```

If the TC has two forms (TC-1 and TC-2), look up BOTH pairs — they may yield different principles.

### Step 2 — Matrix Lookup

For each parameter pair, retrieve the recommended principles.

**Format:**
```
MATRIX LOOKUP:
  Improving: #[N] [name]
  Worsening: #[M] [name]
  Recommended: P#[a], P#[b], P#[c], P#[d]

  (If TC-2 exists)
  Improving: #[M] [name]
  Worsening: #[N] [name]
  Recommended: P#[e], P#[f], P#[g], P#[h]
```

### Step 3 — Merge and Prioritize

Combine principles from both lookups. Principles appearing in BOTH lookups are highest priority.

```
MERGED PRINCIPLES (by priority):
  1. P#[x] — appears in both lookups
  2. P#[y] — appears in both lookups
  3. P#[a] — from TC-1 lookup
  4. P#[e] — from TC-2 lookup
  5. P#[b] — from TC-1 lookup
```

### Step 4 — Apply Top Principles

Hand off to the 40 Principles protocol (`/triz:40p`) with the prioritized list, or apply directly:

For each of the top 3-5 principles:
1. Read the full principle description (including sub-principles)
2. Generate a **specific solution idea** for the given problem context
3. Assess feasibility and contradiction resolution quality

### Step 5 — Output

```
═══ CONTRADICTION MATRIX ANALYSIS ═══

TECHNICAL CONTRADICTION:
  TC-1: IF [improve A] THEN [B worsens]
  TC-2: IF [improve B] THEN [A suffers]

PARAMETER MAPPING:
  Improving: #[N] [name]
  Worsening: #[M] [name]
  Confidence: [High/Medium/Low]

MATRIX RECOMMENDATIONS:
  TC-1 (#N → #M): P#[a], P#[b], P#[c], P#[d]
  TC-2 (#M → #N): P#[e], P#[f], P#[g], P#[h]

PRIORITY PRINCIPLES:
  1. P#[x] [name] — [why this is most relevant]
  2. P#[y] [name] — [why this is relevant]
  3. P#[z] [name] — [why this is relevant]

SOLUTION IDEAS:
  (see 40p-protocol output format)

NEXT STEP:
  → Apply principles in detail: /triz:40p [principle list]
  → Sharpen to physical contradiction: /triz:contradiction
  → Full algorithmic solve: /triz:ariz
```

---

## Common Parameter Pairs and Typical Principles

These are the most frequently encountered pairs with their typical matrix recommendations. Use as quick reference and validation.

| Improving | Worsening | Typical Principles |
|-----------|-----------|-------------------|
| #9 Speed | #1 Weight (moving) | 2, 28, 13, 38 |
| #14 Strength | #1 Weight (moving) | 1, 8, 15, 40 |
| #9 Speed | #14 Strength | 13, 14, 8 |
| #39 Productivity | #27 Reliability | 10, 35, 17, 7 |
| #14 Strength | #12 Shape | 33, 1, 18, 4 |
| #9 Speed | #25 Loss of time | 10, 20, 26, 5 |
| #1 Weight (moving) | #14 Strength | 26, 35, 18, 19 |
| #27 Reliability | #36 Complexity | 13, 35, 1 |
| #33 Ease of use | #36 Complexity | 15, 34, 1, 16 |
| #39 Productivity | #31 Harmful factors | 35, 22, 1, 39 |
| #32 Ease of mfg | #14 Strength | 1, 35, 11, 10 |
| #35 Adaptability | #36 Complexity | 15, 29, 37, 28 |

---

## Anti-Patterns

| Anti-Pattern | Why It's Wrong | Fix |
|-------------|---------------|-----|
| Wrong parameter mapping | Garbage in, garbage out — wrong principles | Take time to map correctly; use analogical mapping guide above |
| Only looking up TC-1 | Missing half the solution space | Always look up BOTH TC forms |
| Treating matrix as oracle | Matrix gives starting points, not final answers | Use principles as inspiration, not prescription |
| Forcing non-engineering problems | Not everything maps to 39 parameters | For highly abstract problems, skip matrix and go direct to principles or ARIZ |
| Ignoring empty cells | ~15% of matrix cells are empty (no statistical pattern) | Use adjacent cells, domain knowledge, or physical contradiction approach |
| Applying all 4 recommended principles equally | Usually 1-2 are highly relevant, others are marginal | Prioritize by domain fit and cross-reference with TC-2 results |

---

## Handoff

### Receives From
- Contradiction Protocol: TC with parameter descriptions (to be mapped and looked up)
- Direct invocation with improving/worsening parameter numbers

### Passes To
- 40 Principles Protocol: Prioritized principle list with problem context
- ARIZ: If matrix yields no satisfactory solution direction
- Contradiction Protocol: If parameters need re-analysis (wrong mapping)
