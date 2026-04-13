# TRIZ — Core Theory Reference

## Origin

Genrich Saulovich Altshuller (1926-1998), Soviet engineer, inventor, and scientist.
Core insight: **Inventive problems follow patterns, and solutions can be found systematically by studying those patterns across domains.**

### Historical Timeline

| Period | Milestone |
|--------|-----------|
| 1946 | Altshuller (age 20) begins analyzing Soviet patent archives while working at the Caspian Sea Navy patent office |
| 1946-1971 | Studies ~40,000 patents to extract patterns of inventive solutions |
| 1956 | First TRIZ publication: "On the Psychology of Inventive Creativity" |
| 1961 | "How to Learn to Invent" published — TRIZ enters Soviet engineering education |
| 1969 | Algorithm of Inventive Problem Solving (ARIZ) first formalized |
| 1970s | TRIZ schools established across USSR; ~100 schools by 1980 |
| 1979 | "Creativity as an Exact Science" — mature theoretical statement |
| 1984 | 40 Inventive Principles and Contradiction Matrix reach mature form |
| 1985 | Laws of Technical System Evolution codified |
| 1989-91 | TRIZ begins spreading outside USSR after glasnost |
| 1990s | Ideation International, Invention Machine Corp bring TRIZ to the West |
| 1998 | Altshuller dies; community continues development |
| 2000s | Samsung, Intel, P&G, Boeing adopt TRIZ systematically |
| 2010s+ | TRIZ combined with Six Sigma, Lean, Design Thinking; MATRIZ certification |

### Patent Study Foundation

Altshuller's key methodological choice: instead of studying creative people, **study creative solutions**. He classified patents not by domain but by the **type of problem they solved** and the **type of solution they applied**. This revealed:

- The same inventive principles appeared repeatedly across unrelated fields
- Problems in electronics had been solved decades earlier in mechanics
- Only ~2% of patents contained truly novel solutions; the rest used known patterns
- The difficulty of a problem correlated with how far the solver looked for analogies

---

## Core Philosophy

### Three Axioms

1. **Problems have patterns.** Inventive problems across all fields share structural similarities — contradictions, resource constraints, system evolution paths.
2. **Solutions have patterns.** The same ~40 principles resolve contradictions in chemistry, mechanics, electronics, software, and business.
3. **Evolution has patterns.** Technical systems evolve along predictable paths (8 Laws of Evolution), enabling forecasting.

### TRIZ vs. Trial-and-Error

| Aspect | Trial-and-Error | TRIZ |
|--------|----------------|------|
| Direction | Random search | Directed by contradiction analysis |
| Domain | Stay within your field | Cross-domain analogies |
| Tradeoffs | Accept compromise | Eliminate contradiction |
| Solution space | Near existing solution | Entire solution landscape |
| Repeatability | Luck-dependent | Systematic, teachable |

---

## Key Concepts

### 1. Contradiction

The central concept. Every inventive problem contains a contradiction — improving one parameter worsens another.

**Technical Contradiction (TC):** Improving parameter A worsens parameter B.
- "Making the wing stronger (weight of stationary object) makes it heavier (weight of moving object)"
- Addressed by the Contradiction Matrix + 40 Inventive Principles

**Physical Contradiction (PC):** A single element must have two opposite properties simultaneously.
- "The wing must be rigid (to bear load) AND flexible (to reduce drag in turbulence)"
- Addressed by Separation Principles (in time, space, condition, scale)

Physical contradictions are deeper than technical contradictions. Sharpening a TC into a PC often reveals the real inventive problem.

### 2. Ideality

**Ideal Final Result (IFR):** The system performs its function without existing — zero cost, zero harm, zero complexity.

```
Ideality = Sum of Useful Functions / (Sum of Harmful Functions + Sum of Costs)
```

The IFR is not a fantasy target but a **thinking tool**: it forces you to ask "what if the problem solved itself?" This eliminates psychological inertia and reveals solutions that use existing resources.

**Example:** The ideal paint is one that doesn't exist — the surface itself has the desired color. (This led to anodizing, surface texturing, and colored alloys.)

### 3. Resources

Everything in and around the system that can be used to solve the problem without adding new elements:

| Resource Type | Examples |
|---------------|----------|
| Substance | Air, water, waste products, the object itself |
| Field/Energy | Gravity, thermal gradients, vibration, existing EM fields |
| Space | Empty space, surfaces, edges, interior volumes |
| Time | Pre-action, pauses between operations, parallel processing |
| Information | Existing signals, byproducts, measurements |
| Functional | Unused capabilities of existing components |

**Principle:** The best solutions use resources already present in the system. Adding new elements reduces ideality.

### 4. System Evolution (Laws of Technical System Evolution)

Technical systems evolve along predictable paths:

| # | Law | Description |
|---|-----|-------------|
| 1 | Completeness | A system needs engine, transmission, tool, and control |
| 2 | Energy conductivity | Energy must flow efficiently through the system |
| 3 | Harmonization of rhythms | Components must synchronize in frequency/period |
| 4 | Increasing ideality | Systems evolve toward higher ideality over time |
| 5 | Uneven development | Components evolve at different rates, creating contradictions |
| 6 | Transition to super-system | Exhausted systems merge into larger systems |
| 7 | Transition to micro-level | Systems evolve from macro to micro mechanisms |
| 8 | Increasing dynamism | Rigid systems become flexible, then adaptive |

These laws enable **technology forecasting**: predicting the next evolutionary stage of a product or process.

---

## The TRIZ Hierarchy: Levels of Inventiveness

Altshuller classified inventive solutions into 5 levels based on how far from the original domain the solver had to search:

| Level | % of Patents | Description | Search Space | Example |
|-------|-------------|-------------|--------------|---------|
| **1** | 32% | Apparent solution — routine design | ~10 solutions within the specialty | Choose standard bolt size |
| **2** | 45% | Minor improvement — small invention | ~100 solutions within the industry | Add a spring to reduce vibration |
| **3** | 19% | Major improvement — resolve contradiction | ~1,000 solutions across industries | Use shape-memory alloy instead of mechanism |
| **4** | 4% | New concept — use different science | ~100,000 solutions across all sciences | Replace mechanical cutting with laser |
| **5** | <1% | Discovery — new phenomenon | All knowable solutions | Superconductivity, nanotube materials |

**Key insight:** TRIZ is most powerful at Levels 2-4. Level 1 doesn't need TRIZ. Level 5 requires scientific discovery. TRIZ tools systematically direct the solver to search at the right level.

---

## TRIZ Toolkit Overview

| Tool | Purpose | Input | Output |
|------|---------|-------|--------|
| Contradiction Matrix | Map technical contradictions to principles | Two conflicting parameters | 3-4 recommended principles |
| 40 Inventive Principles | Resolve technical contradictions | Contradiction + suggested principles | Solution concepts |
| Separation Principles | Resolve physical contradictions | Physical contradiction | Separation strategy |
| Su-Field Analysis | Model problems as substance-field interactions | System with insufficient/harmful function | 76 Standard Solutions |
| ARIZ | Algorithmic problem solving | Complex inventive problem | Step-by-step solution path |
| Trimming | Simplify systems by removing components | System with excess complexity | Reduced system with maintained function |
| Function Analysis | Map useful and harmful functions | System description | Function model |
| Evolution Patterns | Predict system development | Current system state | Next evolutionary stages |
| Resources Analysis | Find hidden solution resources | System + environment | Available resources |
| Effects Database | Apply scientific effects | Required function | Physical/chemical/geometric effects |

### Tool Selection Guide

```
Problem Type                    → Start With
─────────────────────────────────────────────
"Two things conflict"           → Contradiction Matrix + 40 Principles
"It must be X and not-X"        → Separation Principles
"Something doesn't work well"   → Su-Field Analysis + 76 Standards
"Too complex, too many parts"   → Trimming
"What will this evolve into?"   → Evolution Patterns
"Really stuck, tried everything"→ ARIZ (full algorithm)
"Need a specific physical effect"→ Effects Database
```

---

## Key Books

| Book | Author | Year | Focus |
|------|--------|------|-------|
| And Suddenly the Inventor Appeared | G. Altshuller | 1994 (English) | Accessible introduction, stories of inventions analyzed through TRIZ |
| Creativity as an Exact Science | G. Altshuller | 1984 | Mature theoretical statement; contradiction, ideality, evolution laws |
| TRIZ: Keys to Technical Innovation | G. Altshuller (trans. Shulyak) | 1999 | ARIZ algorithm, advanced tools, 40 principles with examples |
| Innovation Algorithm | G. Altshuller | 1973/1999 | ARIZ-71, systematic invention methodology |
| 40 Principles: TRIZ Keys to Innovation | G. Altshuller (Shulyak/Rodman) | 2002 | Focused reference for the 40 principles with modern examples |
| Systematic Innovation | J. Terninko, A. Zusman, B. Zlotin | 1998 | Western-audience introduction to TRIZ tools |
| TRIZ for Engineers | K. Gadd | 2011 | Comprehensive practical guide for engineering application |

---

## Key Terminology

| Term | Definition |
|------|-----------|
| **Technical Contradiction (TC)** | Improving one system parameter worsens another |
| **Physical Contradiction (PC)** | One element must have two mutually exclusive properties |
| **Ideal Final Result (IFR)** | The function is achieved without the system existing |
| **Su-Field** | Substance-Field model: minimum system = 2 substances + 1 field |
| **ARIZ** | Algorithm of Inventive Problem Solving — structured step-by-step method |
| **Inventive Principle** | One of 40 general solution strategies extracted from patents |
| **Contradiction Matrix** | 39x39 lookup table mapping parameter conflicts to principles |
| **Separation Principle** | Resolve physical contradictions by separating in time, space, condition, or scale |
| **Trimming** | Removing a component while redistributing its functions to remaining components |
| **Psychological Inertia** | Mental fixation on existing solutions that blocks inventive thinking |
| **Operator STC** | Size-Time-Cost thought experiment: imagine parameter at 0 and infinity |
| **76 Standard Solutions** | Catalog of standard transformations for Su-Field models |
| **Resources** | Substances, fields, space, time, and information available in/around the system |
| **Functional Model** | Diagram of components and their useful/harmful interactions |
| **S-Curve** | Performance-over-time curve showing birth, growth, maturity, decline of a system |

---

## TRIZ in Modern Context

TRIZ principles apply beyond mechanical engineering:

- **Software:** Contradictions in performance vs. memory, security vs. usability, flexibility vs. simplicity
- **Business:** Market share vs. profitability, standardization vs. customization, speed vs. quality
- **Operations:** Throughput vs. quality, utilization vs. flexibility, cost vs. responsiveness
- **Product Design:** Features vs. simplicity, durability vs. weight, safety vs. convenience

The 40 principles and contradiction analysis are domain-independent thinking tools. The key is translating domain-specific parameters into TRIZ's abstract parameter language, solving at the abstract level, then translating back.
