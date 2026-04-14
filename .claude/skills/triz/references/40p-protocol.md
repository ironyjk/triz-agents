# 40 Inventive Principles Protocol

Applies Altshuller's 40 Inventive Principles to resolve technical contradictions. These principles were extracted from analysis of ~40,000 patents and represent the most frequently used solution patterns across all engineering domains.

## When This Tool Applies

- A technical contradiction has been identified (improving/worsening parameter pair)
- The Contradiction Matrix has suggested specific principles
- Direct principle browsing for creative idea generation
- A physical contradiction needs resolution (principles map to separation strategies)

---

## The 40 Inventive Principles

### Principle 1 — Segmentation
**Sub-principles:** (a) Divide object into independent parts. (b) Make object sectional/easy to assemble-disassemble. (c) Increase degree of segmentation.

- *Engineering:* Sectional furniture that ships flat-pack, assembled on site
- *Software:* Monolith → microservices; split a large function into composable units

### Principle 2 — Taking Out (Extraction)
**Sub-principles:** (a) Extract the disturbing part or property. (b) Extract the only necessary part or property.

- *Engineering:* Separate noisy compressor from the air-conditioned room (split-system AC)
- *Business:* Outsource non-core competency (extract accounting from a manufacturing firm)

### Principle 3 — Local Quality
**Sub-principles:** (a) Transition from homogeneous to heterogeneous structure. (b) Different parts perform different functions. (c) Place each part under conditions most favorable for its operation.

- *Engineering:* Pencil with eraser tip — different material where different function needed
- *Software:* Polyglot persistence — use different databases for different data types

### Principle 4 — Asymmetry
**Sub-principles:** (a) Replace symmetric form with asymmetric. (b) If already asymmetric, increase asymmetry.

- *Engineering:* Asymmetric tire tread for better drainage on one side
- *UX:* Place primary CTA button larger and more prominent than secondary actions

### Principle 5 — Merging (Combining)
**Sub-principles:** (a) Combine identical or similar objects/operations. (b) Combine operations in time (parallel). 

- *Engineering:* Multi-blade razor combines multiple cutting edges in one pass
- *Software:* Batch API requests to reduce network round-trips

### Principle 6 — Universality
**Sub-principles:** (a) Make object/part perform multiple functions, eliminating the need for other parts.

- *Engineering:* Smartphone replaces camera, GPS, music player, flashlight
- *Operations:* Cross-train workers to handle multiple stations

### Principle 7 — Nesting (Russian Dolls)
**Sub-principles:** (a) Place one object inside another. (b) Object passes through a cavity in another. (c) Multiple nesting levels.

- *Engineering:* Telescoping antenna; retractable landing gear stowed in wing
- *Software:* Nested containers (Docker in VM); recursive data structures

### Principle 8 — Anti-weight (Counterweight)
**Sub-principles:** (a) Compensate weight with a force from the environment. (b) Compensate weight by interaction with aerodynamic/hydrodynamic forces.

- *Engineering:* Helium balloons to lift advertising signs; hydrofoils for boat lift
- *Business:* Offset fixed costs with recurring revenue (subscription model)

### Principle 9 — Preliminary Anti-action
**Sub-principles:** (a) Perform counter-action in advance. (b) If the object is under tension, provide anti-tension in advance.

- *Engineering:* Pre-stressed concrete — compress before load to counteract future tension
- *Software:* Input validation before processing; pre-flight checks before deployment

### Principle 10 — Preliminary Action
**Sub-principles:** (a) Perform required change fully or partially in advance. (b) Pre-arrange objects for convenient, immediate use.

- *Engineering:* Pre-pasted wallpaper; pre-cut surgical kits arranged for operation sequence
- *Software:* Pre-computing search indices; caching query results before user requests

### Principle 11 — Beforehand Cushioning
**Sub-principles:** (a) Compensate for low reliability with emergency measures prepared in advance.

- *Engineering:* Airbags; fire sprinklers; safety nets under construction sites
- *Software:* Circuit breakers; automatic failover; database backups

### Principle 12 — Equipotentiality
**Sub-principles:** (a) Change operating conditions so object need not be raised or lowered.

- *Engineering:* Loading dock at truck-bed height eliminates lifting
- *Operations:* Bring the tool to the worker instead of worker to the tool (mobile carts)

### Principle 13 — The Other Way Around (Inversion)
**Sub-principles:** (a) Invert the action. (b) Make the moving part stationary and stationary part movable. (c) Turn object upside down.

- *Engineering:* Rotary table in machining — move the part instead of the tool
- *Software:* Inversion of control (dependency injection); push instead of pull (webhooks vs polling)

### Principle 14 — Spheroidality (Curvature)
**Sub-principles:** (a) Move from flat to curved surfaces. (b) Use rollers, balls, spirals. (c) Move from linear to rotary motion.

- *Engineering:* Arched bridge distributes load better than flat beam
- *UX:* Rounded corners on UI elements (visually lighter, more inviting)

### Principle 15 — Dynamization
**Sub-principles:** (a) Make object or environment automatically adjust for optimal performance at each stage. (b) Divide into elements that can change position relative to each other. (c) If object is immovable, make it movable.

- *Engineering:* Variable-geometry aircraft wing; adjustable suspension
- *Software:* Auto-scaling infrastructure; dynamic configuration; adaptive algorithms

### Principle 16 — Partial or Excessive Action
**Sub-principles:** (a) If 100% is hard to achieve, use slightly more or less to simplify the problem.

- *Engineering:* Overfill a mold then trim excess; spray paint wider than needed then mask
- *Software:* Fetch more data than needed (prefetch), discard unused; approximate algorithms

### Principle 17 — Another Dimension
**Sub-principles:** (a) Move object in 2D or 3D space. (b) Use multi-layer arrangement. (c) Tilt or reorient. (d) Use the other side.

- *Engineering:* Multi-story parking garage; spiral staircase; double-sided PCB
- *Software:* Multi-dimensional indexing; adding a time dimension to spatial data

### Principle 18 — Mechanical Vibration
**Sub-principles:** (a) Cause oscillation. (b) Increase frequency to ultrasonic. (c) Use resonance frequency. (d) Use piezo-vibrators. (e) Combine ultrasonic with electromagnetic fields.

- *Engineering:* Ultrasonic cleaning; vibrating concrete to remove air bubbles
- *Manufacturing:* Vibratory parts feeders for automated assembly

### Principle 19 — Periodic Action
**Sub-principles:** (a) Replace continuous action with periodic/pulsed. (b) If already periodic, change frequency. (c) Use pauses between pulses for additional action.

- *Engineering:* Pulsed laser cutting (higher peak power, less heat); intermittent windshield wipers
- *Software:* Polling → event-driven; batch processing during off-peak hours

### Principle 20 — Continuity of Useful Action
**Sub-principles:** (a) Carry out work continuously (eliminate idle time). (b) Eliminate return/intermediate motions. (c) Replace reciprocating with rotary.

- *Engineering:* Rotary printing press (continuous vs reciprocating); conveyor belt
- *Operations:* Continuous flow manufacturing; eliminate changeover/setup time

### Principle 21 — Skipping (Rushing Through)
**Sub-principles:** (a) Conduct a process or certain stages at high speed to avoid harmful side-effects.

- *Engineering:* Flash freezing preserves food texture vs slow freezing (ice crystal damage)
- *Manufacturing:* High-speed cutting with minimal heat transfer to workpiece

### Principle 22 — Blessing in Disguise (Turn Harm into Benefit)
**Sub-principles:** (a) Use harmful factor to achieve a positive effect. (b) Eliminate harmful factor by combining with another harmful factor. (c) Amplify harmful factor until it is no longer harmful.

- *Engineering:* Use waste heat to preheat intake air; sand-blast surface intentionally for grip
- *Business:* Customer complaints → product improvement insights; staff turnover → fresh perspectives

### Principle 23 — Feedback
**Sub-principles:** (a) Introduce feedback. (b) If feedback exists, change its magnitude or influence.

- *Engineering:* Thermostat; cruise control; auto-focus camera
- *Software:* A/B testing with automated traffic allocation; self-healing systems

### Principle 24 — Intermediary (Mediator)
**Sub-principles:** (a) Use an intermediate object to transfer or carry out an action. (b) Temporarily merge one object with another that is easily removed.

- *Engineering:* Welding electrode (consumable intermediary); catalyst in chemical reaction
- *Software:* Message broker; API gateway; adapter pattern
- *Business:* Real estate agent between buyer and seller; escrow service holding funds until contract conditions met

### Principle 25 — Self-Service
**Sub-principles:** (a) Make object service itself (perform auxiliary/repair functions). (b) Use waste resources, energy, or substances.

- *Engineering:* Self-cleaning oven; self-sharpening plow blade that wears to maintain edge
- *Software:* Garbage collection; self-healing infrastructure; auto-generated documentation
- *Operations:* Employee suggestion box where workers fix their own workflow bottlenecks; waste heat from servers used to warm offices

### Principle 26 — Copying
**Sub-principles:** (a) Use inexpensive copy instead of fragile/expensive original. (b) Replace object with optical copy (image), use scale changes. (c) If visible copies used, switch to IR/UV.

- *Engineering:* Wind tunnel testing of scale models; crash-test dummies
- *Software:* Mock objects in testing; staging environment; digital twin
- *Business:* Pilot program in one region before national rollout; tabletop exercises simulating crisis scenarios

### Principle 27 — Cheap Short-Living Object
**Sub-principles:** (a) Replace expensive durable object with cheap disposable ones.

- *Engineering:* Disposable surgical instruments (sterility guaranteed, no cleaning cost)
- *Software:* Ephemeral containers; serverless functions; disposable test environments
- *Operations:* Single-use pallets cheaper than managing return logistics; disposable PPE vs sterilizing reusable gear

### Principle 28 — Mechanics Substitution
**Sub-principles:** (a) Replace mechanical means with sensory (optical, acoustic, taste, smell). (b) Use electric, magnetic, electromagnetic fields. (c) Replace fields: stationary→moving, unstructured→structured, random→phased. (d) Use fields with ferromagnetic particles.

- *Engineering:* Magnetic bearing replaces mechanical bearing (no friction/wear)
- *Manufacturing:* Induction heating replaces gas furnace (precise, instant, clean)
- *Software:* Replace manual code review gates with automated static analysis; OCR replaces manual data entry

### Principle 29 — Pneumatics and Hydraulics
**Sub-principles:** (a) Replace solid parts with gas or liquid: inflatable, air-cushioned, hydrostatic, hydro-reactive.

- *Engineering:* Air bearings for frictionless movement; inflatable structures
- *Operations:* Pneumatic tube delivery systems; hydraulic lifts
- *Software:* Replace rigid data schemas with fluid stream processing; event sourcing as a "flow" replacing fixed state snapshots

### Principle 30 — Flexible Shells and Thin Films
**Sub-principles:** (a) Replace rigid structures with flexible membranes and thin films. (b) Isolate object from environment using flexible shells and thin films.

- *Engineering:* Shrink-wrap packaging; bubble wrap; PTFE-coated cookware
- *Architecture:* Tensile fabric structures (stadium roofs)
- *Software:* Feature flags as thin wrappers around rigid code paths; plugin interfaces that isolate core from extensions

### Principle 31 — Porous Materials
**Sub-principles:** (a) Make object porous or add porous elements. (b) If already porous, fill pores with useful substance.

- *Engineering:* Sintered metal bearings pre-filled with lubricant (self-lubricating)
- *Construction:* Pervious concrete for stormwater management
- *Software:* Bloom filters — probabilistic "porous" data structure that trades perfect accuracy for massive space savings

### Principle 32 — Color Changes
**Sub-principles:** (a) Change color or transparency. (b) Change color of surroundings or external environment. (c) Use colored additives to observe hard-to-see objects. (d) Use luminescent traces.

- *Engineering:* Thermochromic paint indicates overheating; UV dye for leak detection
- *Safety:* High-vis clothing; color-coded wiring and piping
- *UX:* Red/green status indicators in dashboards; syntax highlighting in code editors; heatmaps showing user click density

### Principle 33 — Homogeneity
**Sub-principles:** (a) Make objects interacting with a given object of the same material (or close in properties).

- *Engineering:* Ice-mold container made of ice (no contamination, no cleaning)
- *Manufacturing:* Sacrificial tooling made of same material as workpiece
- *Software:* Test data generated from same schema as production; "dogfooding" — team uses its own product so tool and user share context

### Principle 34 — Discarding and Recovering
**Sub-principles:** (a) Discard (dissolve, evaporate) elements that have fulfilled their function. (b) Immediately restore consumable parts during operation.

- *Engineering:* Soluble surgical sutures; rocket stage separation; lost-wax casting
- *Software:* Temporary scaffolding code; feature flags removed after rollout
- *Operations:* Temporary staffing agencies for seasonal peaks; pop-up stores that close after a promotional period

### Principle 35 — Parameter Changes
**Sub-principles:** (a) Change physical state (gas→liquid→solid). (b) Change concentration or consistency. (c) Change flexibility. (d) Change temperature or volume.

- *Engineering:* Freeze pipe contents for temporary plug (ice plug technique)
- *Food:* Freeze-drying preserves structure while removing water
- *Software:* Serialize objects to JSON for transport, deserialize on arrival; toggle between verbose and compact logging modes

### Principle 36 — Phase Transitions
**Sub-principles:** (a) Use phenomena occurring during phase transitions (volume change, heat release/absorption, etc.).

- *Engineering:* Heat pipes use evaporation/condensation cycle for efficient heat transfer
- *Storage:* Phase-change materials for thermal energy storage (melt to absorb, solidify to release)
- *Business:* Tipping-point marketing — small increases in spend produce disproportionate viral growth once adoption crosses a threshold

### Principle 37 — Thermal Expansion
**Sub-principles:** (a) Use thermal expansion/contraction. (b) If already using, use multiple materials with different thermal expansion coefficients.

- *Engineering:* Bimetallic thermostat; shrink-fit assembly (heat sleeve, insert shaft, cool)
- *Measurement:* Mercury thermometer exploits liquid thermal expansion
- *Software:* Auto-scaling cloud instances that expand capacity under load and contract when idle, paying only for actual usage

### Principle 38 — Strong Oxidants (Boosted Interactions)
**Sub-principles:** (a) Replace normal air with enriched air. (b) Replace enriched air with pure oxygen. (c) Expose air/oxygen to ionizing radiation. (d) Use ionized oxygen (ozone). (e) Replace ozone with ozonized/ionized oxygen.

- *Engineering:* Oxygen-enriched combustion for higher temperatures; ozone water treatment
- *Abstract:* Intensify the interaction/process at each step (applicable to any domain)
- *Software:* Progressive enhancement of test suites — unit → integration → load → chaos engineering, each level more aggressive

### Principle 39 — Inert Atmosphere
**Sub-principles:** (a) Replace normal environment with inert. (b) Add neutral parts or inert additives. (c) Carry out process in vacuum.

- *Engineering:* Welding under argon gas; vacuum packaging for food preservation
- *Software:* Sandboxing; isolated test environments; containerization
- *Operations:* Cleanroom manufacturing; nitrogen-blanketed fuel tanks preventing ignition; neutral third-party mediator in negotiations

### Principle 40 — Composite Materials
**Sub-principles:** (a) Replace homogeneous materials with composite (multi-layer, fiber-reinforced, etc.).

- *Engineering:* Carbon fiber reinforced polymer — strong as steel, fraction of weight
- *Construction:* Reinforced concrete (steel rebar + concrete); laminated safety glass
- *Software:* Hybrid architecture combining microservices (flexibility) with a shared event bus (consistency); full-stack frameworks pairing React UI with server-side rendering

---

## Application Process

### Step 1 — Receive Contradiction

Input is either:
- A TC with improving/worsening parameter numbers (from matrix lookup)
- A TC with parameter descriptions (to be mapped)
- A PC with element and opposing properties
- A direct problem statement (contradiction must be formulated first)

### Step 2 — Identify Candidate Principles

**From Matrix:** Use the Contradiction Matrix to get 3-5 statistically recommended principles for the improving/worsening parameter pair.

**From PC Separation:** Map the separation type to associated principles:
| Separation | Commonly Associated Principles |
|-----------|-------------------------------|
| In Time | 9, 10, 11, 15, 16, 19, 20, 21, 34 |
| In Space | 1, 2, 3, 4, 7, 17, 24, 30 |
| In Condition | 28, 32, 35, 36, 37, 38, 39 |
| In Scale | 1, 3, 5, 14, 17, 31, 40 |

**From Domain Knowledge:** If neither matrix nor PC separation applies, select principles based on the problem domain and LLM knowledge of which principles most commonly apply.

### Step 3 — Generate Specific Solutions

For each candidate principle, generate **concrete, domain-specific** solution ideas. Not generic restatements of the principle.

**Bad:** "Apply Principle 1 (Segmentation) — divide the object into parts"
**Good:** "Apply Principle 1 (Segmentation) — replace the single monolithic filter with a cascade of 3 progressively finer filters: coarse mesh → fine mesh → membrane. This allows each stage to be independently cleaned/replaced, solving the clogging-vs-filtration contradiction."

### Step 4 — Evaluate and Rank Solutions

For each generated solution, assess:

| Criterion | Score 1-5 | Description |
|-----------|-----------|-------------|
| Contradiction Resolution | | Does it ELIMINATE (not compromise) the contradiction? |
| Ideality | | Does it increase useful function / reduce harm and cost? |
| Feasibility | | Can it be implemented with known technology? |
| Resource Usage | | Does it use existing system resources? |
| Inventive Level | | Level 1-5 (higher = more inventive, cross-domain) |

Rank solutions by total score. Present top 3.

### Step 5 — Output

Present solutions with principle cards (see `output-format.md`).

---

## Output Format

```
═══ 40 PRINCIPLES APPLICATION ═══

CONTRADICTION:
  Improving: #[N] [name]
  Worsening: #[N] [name]
  (or PC: [element] must be [X] and [anti-X])

CANDIDATE PRINCIPLES: [from matrix/separation/domain]

┌─────────────────────────────────────┐
│ P#[N] [NAME]                        │
│─────────────────────────────────────│
│ Sub-principle: [specific sub]       │
│                                     │
│ SOLUTION IDEA:                      │
│ [Concrete, specific solution        │
│  description for this problem]      │
│                                     │
│ Resolution: [Full/Partial]          │
│ Feasibility: [High/Med/Low]        │
│ Ideality: [+N% estimated]          │
└─────────────────────────────────────┘

[Repeat for each principle]

SOLUTION RANKING:
  1. P#[N] — [brief] — Score: [X/25]
  2. P#[N] — [brief] — Score: [X/25]
  3. P#[N] — [brief] — Score: [X/25]

RECOMMENDED SOLUTION: #[rank 1]
  [1-2 sentence summary of why]

NEXT STEP:
  → Validate with evolution analysis: /triz:evolution
  → Deep solve if insufficient: /triz:ariz
  → Combine with other principles for composite solution
```

---

## Anti-Patterns

| Anti-Pattern | Why It's Wrong | Fix |
|-------------|---------------|-----|
| Generic principle restatement | Not useful — user already has the principle | Generate SPECIFIC solutions for THIS problem |
| Applying all 40 principles | Noise drowns signal | Focus on 3-5 most relevant from matrix/separation |
| Ignoring sub-principles | Missing the nuance that makes solutions concrete | Read all sub-principles; often (b) or (c) is the key |
| Solutions that compromise | TRIZ eliminates contradictions, not balances them | If the solution trades off, it hasn't resolved the contradiction |
| Domain-locked thinking | Missing cross-domain analogies (TRIZ's strength) | Deliberately seek analogies: "How does nature solve this? Aerospace? Software?" |
| Single-principle fixation | Some problems need principle combinations | Consider 2-principle combinations for stubborn contradictions |

---

## Handoff

### Receives From
- Contradiction Protocol: TC with parameter numbers, or PC with separation strategy
- Matrix Protocol: Suggested principle numbers for a parameter pair
- Direct invocation with problem description

### Passes To
- ARIZ: If no principle yields satisfactory resolution, escalate to full ARIZ
- Evolution: Validate solution against evolutionary trends
- Trimming: If solution adds complexity, check if trimming can simplify
