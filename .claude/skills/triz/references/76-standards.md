# 76 Standard Solutions — Complete Reference

## Overview

The 76 Standard Solutions (also called Inventive Standards) were developed by Genrich Altshuller and his colleagues between 1975 and 1985. They provide ready-made solution patterns for problems modeled as Su-Field (Substance-Field) systems.

**How they work**: Once a problem is expressed as a Su-Field model (see [sufield-protocol.md](sufield-protocol.md)), the model type (incomplete, harmful, insufficient, etc.) points to a specific class and subclass of standards. Each standard describes an abstract transformation pattern that can be mapped onto the concrete problem.

**Relationship to other TRIZ tools**: The 76 standards are the primary solution mechanism for Su-Field analysis. They complement the 40 Inventive Principles (which address contradictions) and ARIZ (which handles complex multi-step problems). Many standards encode the same insights as specific inventive principles but in Su-Field notation.

---

## Class 1: Building and Destroying Su-Field Models (13 standards)

**Purpose**: Create a working Su-Field where none exists, or neutralize a harmful interaction.

### Subclass 1.1: Building Su-Field Models (8 standards)

#### Standard 1.1.1 — Build a Complete Su-Field Model
**Pattern**: If there is an object (S1) that is not being adequately controlled, processed, or detected, complete the Su-Field model by introducing the missing substance S2 and/or field F.
**When to use**: The system is incomplete — a required function is not performed because elements are missing.
**Example**: A metal part (S1) needs crack detection. Introduce magnetic powder (S2) and a magnetic field (F). The powder accumulates at cracks, making them visible.
**Su-Field notation**:
```
Before: S1 (incomplete)
After:  F
        |
    S1 --- S2
```

#### Standard 1.1.2 — Build an Internal Complex Su-Field (Internal Additive to S1)
**Pattern**: If S1 cannot be readily changed or replaced, introduce an internal additive into S1 to make it more responsive to the field F.
**When to use**: The Su-Field is complete but S1 is insufficiently responsive, and you can modify S1 internally.
**Example**: Concrete (S1) needs to be monitored for strain. Embed fiber optic sensors (additive within S1) so that light (F) reveals internal stress patterns.
**Su-Field notation**:
```
Before: S1 (low responsiveness)
After:  F
        |
    S1' --- S2    (S1' = S1 with internal additive)
```

#### Standard 1.1.3 — Build an Internal Complex Su-Field (Internal Additive to S2)
**Pattern**: If S2 cannot be readily changed, introduce an internal additive into S2 to improve its ability to transmit or apply the field.
**When to use**: The tool substance S2 needs enhancement but cannot be replaced.
**Example**: A grinding wheel (S2) is inefficient. Add diamond particles as an internal additive to S2, increasing its cutting effectiveness under mechanical force (F) on the workpiece (S1).
**Su-Field notation**:
```
Before: F
        |
    S1 --- S2 (weak action)
After:  F
        |
    S1 --- S2'    (S2' = S2 with internal additive)
```

#### Standard 1.1.4 — Build an External Complex Su-Field (External Additive)
**Pattern**: If S1 and S2 cannot be changed, introduce an external substance S3 between or around them to modify the interaction.
**When to use**: Neither S1 nor S2 can be modified, but the interaction needs improvement.
**Example**: A hot metal plate (S2) must be shaped without damaging a polymer mold (S1). Introduce a release agent layer (S3) between them.
**Su-Field notation**:
```
Before: F
        |
    S1 --- S2
After:  F
        |
    S1 --- S3 --- S2
```

#### Standard 1.1.5 — Build an External Complex Su-Field (Environment as Additive)
**Pattern**: If no external substance can be introduced, use a substance from the environment (air, water, ambient temperature) as S3.
**When to use**: Constraints prohibit adding new substances; must use what is already available.
**Example**: A heated bearing (S1) must be cooled during press-fitting. Use ambient air (S3 from environment) directed as a jet to manage thermal expansion during assembly.
**Su-Field notation**:
```
Before: F
        |
    S1 --- S2
After:  F
        |
    S1 --- S_env --- S2    (S_env = substance from environment)
```

#### Standard 1.1.6 — Minimal Su-Field with Maximum Field
**Pattern**: If a minimal Su-Field can be built but the function is still insufficient, use the maximum effective mode of the field (e.g., resonance frequency, pulsed mode).
**When to use**: The Su-Field is complete but performance is marginal; field intensification is needed.
**Example**: Ultrasonic cleaning (F = acoustic field) is insufficient. Switch to the resonant frequency of the contaminant-substrate bond to maximize dislodging effect.
**Su-Field notation**:
```
Before: F (weak mode)
        |
    S1 --- S2
After:  F_max (resonant/pulsed/optimized mode)
        |
    S1 --- S2
```

#### Standard 1.1.7 — Build a Su-Field Using Existing Fields
**Pattern**: If introducing a new field is difficult, use a field already present in the system or supersystem.
**When to use**: Constraints prevent introducing new energy sources; exploit existing fields.
**Example**: A chemical reactor already generates heat (existing F). Use that thermal field to preheat incoming feedstock (S1) rather than adding a separate heater.
**Su-Field notation**:
```
Before: S1 (needs F, but new F constrained)
After:  F_existing
        |
    S1 --- S2
```

#### Standard 1.1.8 — Build a Su-Field Using Fields at Different Frequencies or Modes
**Pattern**: If a field is present but causes harm at its current parameters, shift to a different frequency, intensity, or mode where it performs the useful function without the harm.
**When to use**: The right field type is present but at wrong parameters.
**Example**: Visible light causes photodegradation of a sample. Switch to infrared illumination to inspect the sample without damage.
**Su-Field notation**:
```
Before: F (harmful at current parameters)
        |
    S1 -~~ S2
After:  F' (different frequency/mode)
        |
    S1 --- S2
```

### Subclass 1.2: Destroying Su-Field Models (5 standards)

#### Standard 1.2.1 — Eliminate Harmful by S3
**Pattern**: Introduce S3 to block harm.
**When to use**: Side effect.
**Example**: Soft pad.
**Su-Field notation**:
```
Before: F
        |
    S1 -~~ S2
After:  F
        |
    S1---S3---S2
```

#### Standard 1.2.2 — Modify S1/S2
**Pattern**: Modify internally.
**When to use**: No new substance.
**Example**: Cooling channels.
**Su-Field notation**:
```
Before: F
        |
    S1 -~~ S2
After:  F
        |
    S1_mod---S2
```

#### Standard 1.2.3 — Counter F2
**Pattern**: F2 vs F1.
**When to use**: Field counter.
**Example**: Ionizing field.
**Su-Field notation**:
```
Before: F1
        |
    S1-~~S2
After:  F1  F2
        |   |
    S1---S2
```

#### Standard 1.2.4 — Switch Off
**Pattern**: Temporal control.
**When to use**: Time-dependent.
**Example**: Pulse EM.
**Su-Field notation**:
```
Before: F(cont)
        |
    S1-~~S2
After:  F(pulsed)
        |
    S1---S2
```

#### Standard 1.2.5 — Ferro Barrier
**Pattern**: Magnetic barrier.
**When to use**: Adjustable.
**Example**: Ferrofluid.
**Su-Field notation**:
```
Before: F
        |
    S1-~~S2
After:  F  Fmg
        |   |
    S1---S3f---S2
```

---

## Class 2: Developing Su-Field Models (23 standards)

**Purpose**: Improve insufficient Su-Field.

### Subclass 2.1: Chain Su-Fields (2)

#### Standard 2.1.1 — Chain with S3
**Pattern**: Insert S3 to amplify.
**When to use**: Too weak.
**Example**: Hydraulic distributes force.
**Su-Field notation**:
```
Before: F
        |
    S1---S2(insuf)
After:  F
        |
    S1---S3---S2
```

#### Standard 2.1.2 — Enhanced Chain
**Pattern**: Additive in S3.
**When to use**: S3 weak.
**Example**: Metal mesh in rubber.
**Su-Field notation**:
```
Before: F
        |
    S1---S3---S2
After:  F
        |
    S1---S3_enh---S2
```

### Subclass 2.2: Double Su-Fields (2)

#### Standard 2.2.1 — Double SF
**Pattern**: Add F2.
**When to use**: Need control.
**Example**: UV+press.
**Su-Field notation**:
```
Before: F1
        |
    S1---S2
After:  F1  F2
        |   |
    S1---S2
```

#### Standard 2.2.2 — Double+Subst
**Pattern**: S3 for F2.
**When to use**: Coupling.
**Example**: Ferro+magnetic.
**Su-Field notation**:
```
Before: F1
        |
    S1---S2
After:  F1  F2
        |   |
    S1---S3---S2
```

### Subclass 2.3: Ferromagnetic Su-Fields (6)

#### Standard 2.3.1 — Ferro S2
**Pattern**: Replace S2+mag.
**When to use**: Remote ctrl.
**Example**: Ferro abrasive.
**Su-Field notation**:
```
Before: Fme
        |
    S1---S2
After:  Fmg
        |
    S1---S2f
```

#### Standard 2.3.2 — Ferro S1
**Pattern**: Add ferro to S1.
**When to use**: Hard to handle.
**Example**: Ferro polymer.
**Su-Field notation**:
```
Before: S1(hard)
After:  Fmg
        |
    S1f---S2
```

#### Standard 2.3.3 — Ferrofluid
**Pattern**: Liquid+mag.
**When to use**: Shape-change.
**Example**: FF seal.
**Su-Field notation**:
```
Before: Fme
        |
    S1---S2
After:  Fmg
        |
    S1---S2ff
```

#### Standard 2.3.4 — Cap+Ferro
**Pattern**: Porous+ferro.
**When to use**: Wick+ctrl.
**Example**: Self-clean.
**Su-Field notation**:
```
Before: F
        |
    S1---S2p
After:  F Fmg
        |  |
    S1---S2fp
```

#### Standard 2.3.5 — Curie
**Pattern**: Temp switch.
**When to use**: Th-mag.
**Example**: Fuse release.
**Su-Field notation**:
```
Before: Fmg
        |
    S1---S2f
After:  Above Curie: released
```

#### Standard 2.3.6 — MR Fluids
**Pattern**: Visc via Fmg.
**When to use**: Adj stiff.
**Example**: MR damper.
**Su-Field notation**:
```
Before: Fme
        |
    S1---S2
After:  Fme+Fmg
        |
    S1---S2mr
```

### Subclass 2.4: Dynamic/Structured Fields (13)

#### Standard 2.4.1 — Gradients
**Pattern**: Non-uniform.
**When to use**: Diff treatment.
**Example**: Thermal grad.
**Su-Field notation**:
```
Before: F(uni)
        |
    S1---S2
After:  F_grad
        |
    S1---S2
```

#### Standard 2.4.2 — Structured
**Pattern**: Periodic.
**When to use**: Selective.
**Example**: Pattern UV.
**Su-Field notation**:
```
Before: F(cont)
        |
    S1---S2
After:  F_struct
        |
    S1---S2
```

#### Standard 2.4.3 — Resonance
**Pattern**: Nat freq.
**When to use**: Insufficient.
**Example**: Resonant US.
**Su-Field notation**:
```
Before: F(arb)
        |
    S1---S2
After:  F_res
        |
    S1---S2
```

#### Standard 2.4.4 — Traveling
**Pattern**: Direction.
**When to use**: Transport.
**Example**: Piezo wave.
**Su-Field notation**:
```
Before: F_stand
        |
    S1---S2
After:  F_travel
        |
    S1---S2
```

#### Standard 2.4.5 — Pulsed
**Pattern**: Off-time.
**When to use**: Overheat.
**Example**: Pulsed laser.
**Su-Field notation**:
```
Before: F(cont)
        |
    S1---S2
After:  F_pulse
        |
    S1---S2
```

#### Standard 2.4.6 — Synchronize
**Pattern**: Coordinate.
**When to use**: Interference.
**Example**: Sync spray.
**Su-Field notation**:
```
Before: F1 F2(unsync)
After:  F1<->F2(sync)
```

#### Standard 2.4.7 — Micro-Level
**Pattern**: Molecular.
**When to use**: Macro crude.
**Example**: SMA change.
**Su-Field notation**:
```
Before: F(macro)
        |
    S1---S2
After:  F(micro)
        |
    S1m---S2
```

#### Standard 2.4.8 — Bi/Poly-F
**Pattern**: Combine.
**When to use**: Single insuf.
**Example**: Mech+US.
**Su-Field notation**:
```
Before: F1
        |
    S1---S2
After:  F1+F2
        |
    S1---S2
```

#### Standard 2.4.9 — Segmented
**Pattern**: Articulated.
**When to use**: Rigid.
**Example**: Pin mold.
**Su-Field notation**:
```
Before: F
        |
    S1---S2(rig)
After:  F
        |
    S1---S2_seg
```

#### Standard 2.4.10 — Non-Uniform
**Pattern**: Gradient.
**When to use**: Diff props.
**Example**: Cer-Cu pad.
**Su-Field notation**:
```
Before: F
        |
    S1---S2(uni)
After:  F
        |
    S1---S2_grad
```

#### Standard 2.4.11 — Therm Exp
**Pattern**: Differential.
**When to use**: Precise.
**Example**: Bimetal.
**Su-Field notation**:
```
Before: Fme
        |
    S1---S2
After:  Fth
        |
    S1---S2bi
```

#### Standard 2.4.12 — E/M Dyn
**Pattern**: Replace mech.
**When to use**: Slow.
**Example**: Piezo eject.
**Su-Field notation**:
```
Before: Fme
        |
    S1---S2
After:  Fe
        |
    S1---S2pz
```

#### Standard 2.4.13 — ER/MR
**Pattern**: Visc via E/M.
**When to use**: Var stiff.
**Example**: ER mount.
**Su-Field notation**:
```
Before: Fme
        |
    S1---S2
After:  Fme+Fe
        |
    S1---S2er
```

---

## Class 3: System Transitions (6 standards)

**Purpose**: Transform the system to a higher level of organization when improvement within the current architecture has reached its limits.

### Subclass 3.1: Transition to Bi-Systems and Poly-Systems (4 standards)

#### Standard 3.1.1 — Bi-System (Combine Identical Systems)
**Pattern**: Combine two identical systems to gain emergent properties that neither system has alone. The combined system produces effects greater than the sum of individual systems.
**When to use**: A single system has reached its performance limit and cannot be improved further within its current architecture.
**Example**: Two single-blade razors combined into a multi-blade system — the first blade lifts the hair, the second cuts it lower, achieving a closer shave than either blade alone.
**Su-Field notation**:
```
Before: F           F
        |           |
    S1---S2     S1---S2   (two separate identical systems)
After:  F
        |
    S1---[S2a+S2a]        (bi-system with emergent property)
```

#### Standard 3.1.2 — Poly-System (Combine Different Systems)
**Pattern**: Combine two or more different systems so that each contributes a unique capability. The combined poly-system performs functions that no individual system can.
**When to use**: A single system cannot provide all required functions, and adding functions to it creates contradictions.
**Example**: A Swiss Army knife combines blade (S2a), screwdriver (S2b), and corkscrew (S2c) — each tool serves a different function, and the combined system replaces carrying three separate tools.
**Su-Field notation**:
```
Before: F1          F2
        |           |
    S1---S2a    S1---S2b   (two different systems)
After:  F1, F2
        |
    S1---[S2a+S2b]         (poly-system with multiple functions)
```

#### Standard 3.1.3 — Maximize Differences in Poly-System
**Pattern**: When combining systems into a poly-system, maximize the differences between the components. Greater diversity yields more emergent properties and a more capable combined system.
**When to use**: A poly-system has been created but its components are too similar, limiting the emergent benefits.
**Example**: A drill bit set with identical geometry but maximally different sizes, coatings, and materials (HSS, carbide, diamond) — the diversity ensures every drilling scenario is covered by the optimal tool.
**Su-Field notation**:
```
Before: [S2a ~ S2b]        (similar components in poly-system)
After:  [S2a ≠ S2b]        (maximally different components → richer capability)
```

#### Standard 3.1.4 — Convolution (Integrate into Single Element)
**Pattern**: After creating a bi- or poly-system, convolve (integrate) the separate components into a single element that performs all functions. This is the evolutionary endpoint of system combination.
**When to use**: A poly-system works well but is complex, bulky, or hard to manage. The separate components can be merged into one multi-functional element.
**Example**: A smartphone integrates camera, GPS, music player, phone, and computer into a single device — each was originally a separate system in a poly-system (PDA + phone + camera), now convoluted into one.
**Su-Field notation**:
```
Before: [S2a + S2b + S2c]  (poly-system, multiple components)
After:  S2_integrated       (single element performing all functions)
```

### Subclass 3.2: Transition to Micro-Level (2 standards)

#### Standard 3.2.1 — Transition from Macro to Micro Level
**Pattern**: Replace a macro-level mechanical system with micro-level interactions (molecular, atomic, or field-based). This enables finer control, eliminates mechanical wear, and often resolves contradictions that are unsolvable at the macro level.
**When to use**: The system has reached fundamental physical limits at the macro level, or mechanical interactions create unavoidable harmful effects (friction, wear, vibration).
**Example**: Chemical-mechanical planarization (CMP) in semiconductor manufacturing — instead of purely mechanical grinding (macro), a chemical slurry (micro-level reaction) dissolves surface material while gentle mechanical action removes residue, achieving nanometer-level flatness impossible with mechanical means alone.
**Su-Field notation**:
```
Before: Fme (mechanical)
        |
    S1---S2
After:  Fch (chemical/molecular)
        |
    S1---S2_micro   (micro-level interaction)
```

#### Standard 3.2.2 — Use Micro-Structure of Substance
**Pattern**: Exploit the internal micro-structure (grain boundaries, crystal orientation, molecular arrangement) of existing substances to gain new properties without adding new components.
**When to use**: The system needs new properties but constraints prevent adding new substances; the existing substances have untapped micro-level features.
**Example**: Single-crystal turbine blades — by controlling the crystal structure of the nickel superalloy (eliminating grain boundaries), the blade gains dramatically higher creep resistance at extreme temperatures, using the same material.
**Su-Field notation**:
```
Before: F
        |
    S1---S2 (polycrystalline, standard properties)
After:  F
        |
    S1---S2_micro  (controlled micro-structure → enhanced properties)
```

---

## Class 4: Detection and Measurement Standards (17 standards)

**Purpose**: Solve problems of detection, measurement, and information gathering by restructuring them as Su-Field problems. The core insight is: if you cannot measure something directly, build a Su-Field model where the measured parameter modulates a detectable field.

### Subclass 4.1: Indirect Methods (2 standards)

#### Standard 4.1.1 — Measure a Copy or Model Instead of the Original
**Pattern**: If the object cannot be measured directly (too large, too small, too dangerous, or inaccessible), create a copy or model and measure that instead.
**When to use**: Direct measurement of the object is physically impossible or impractical.
**Example**: Measuring the internal profile of a deep bore — take a silicone impression (copy) of the bore, extract it, and measure the impression with calipers or optical scanner.
**Su-Field notation**:
```
Before: F_meas → S1 (inaccessible, measurement fails)
After:  F_meas → S1_copy (accessible copy, measurement succeeds)
```

#### Standard 4.1.2 — Measure a Correlated Parameter
**Pattern**: If a parameter cannot be measured directly, measure a different parameter that changes proportionally or predictably with the target parameter.
**When to use**: The target parameter is inaccessible or has no direct sensor, but a correlated parameter is measurable.
**Example**: Measuring temperature inside a sealed furnace — instead of inserting a thermocouple (impossible), measure the infrared radiation (correlated parameter) emitted through a viewport using a pyrometer.
**Su-Field notation**:
```
Before: F_meas → Parameter_A (hard to measure)
After:  F_meas → Parameter_B (easy to measure, proportional to A)
```

### Subclass 4.2: Building Measurement Su-Fields (3 standards)

#### Standard 4.2.1 — Build a Complete Measurement Su-Field
**Pattern**: If no measurement system exists, build one by introducing a detectable substance (S2) and a detection field (F). The substance interacts with the object and modulates the field in a measurable way.
**When to use**: The object (S1) produces no detectable signal on its own — no existing measurement Su-Field.
**Example**: Detecting gas leaks in pipes — apply soapy water (S2) to pipe joints; escaping gas creates visible bubbles, detected by visual inspection (F = visible light).
**Su-Field notation**:
```
Before: S1 (undetectable — no measurement system)
After:  F_vis
        |
    S1---S2_soap   (bubbles modulate visible light → leak detected)
```

#### Standard 4.2.2 — Add Internal Additive for Detection
**Pattern**: If the object is opaque or internally inaccessible, introduce a detectable additive inside the object that responds to an external detection field.
**When to use**: Internal features of S1 need measurement, but S1 is opaque or sealed.
**Example**: Medical CT scan — inject iodine-based contrast agent (internal additive to bloodstream S1); X-rays (F) are absorbed differently by the contrast agent, revealing blood vessel structure.
**Su-Field notation**:
```
Before: F_xray → S1 (low contrast, internal structure invisible)
After:  F_xray → S1' (S1 with internal contrast additive → structure visible)
```

#### Standard 4.2.3 — Add External Additive for Detection
**Pattern**: If the object's surface or external features need detection and internal modification is not possible, apply a detectable substance externally.
**When to use**: Surface features of S1 need measurement but produce insufficient signal; S1 cannot be modified internally.
**Example**: Detecting surface cracks in welds — apply fluorescent dye penetrant (S3) to the surface; after cleaning, illuminate with UV light (F); dye trapped in cracks fluoresces, revealing defect locations.
**Su-Field notation**:
```
Before: S1 (surface defects invisible)
After:  F_UV
        |
    S1---S3_fluor   (fluorescent dye on surface reveals cracks under UV)
```

### Subclass 4.3: Enhancing Measurement Su-Fields (3 standards)

#### Standard 4.3.1 — Use Resonance for Amplification
**Pattern**: If a measurement signal is too weak, use resonance to amplify it. Drive the measurement system at its natural frequency — small changes in the measured parameter cause large changes in resonance response.
**When to use**: The measurement Su-Field exists but the signal-to-noise ratio is too low for reliable detection.
**Example**: Quartz crystal microbalance (QCM) — a quartz crystal oscillates at its resonance frequency; when mass deposits on its surface (even nanograms), the resonance frequency shifts measurably, detecting extremely small mass changes.
**Su-Field notation**:
```
Before: F_meas (weak signal)  →  S1
After:  F_resonance (amplified signal)  →  S1  (small parameter change → large frequency shift)
```

#### Standard 4.3.2 — Use Combined Fields for Disambiguation
**Pattern**: If a single measurement field gives ambiguous results, use two different fields simultaneously. The combination resolves ambiguity by providing independent data channels.
**When to use**: A single measurement field cannot distinguish between multiple causes of signal variation.
**Example**: Non-destructive testing of composites — ultrasonic testing (F1) detects delaminations but cannot distinguish from porosity. Adding thermographic imaging (F2) differentiates: delaminations trap heat differently than pores.
**Su-Field notation**:
```
Before: F1 → S1 (ambiguous signal — multiple possible causes)
After:  F1 + F2 → S1 (combined fields disambiguate the measurement)
```

#### Standard 4.3.3 — Measure Derivatives Instead of Absolute Values
**Pattern**: If direct measurement of a parameter is noisy or unreliable, measure the rate of change (first derivative) or acceleration (second derivative) instead. Derivatives are often more sensitive and less affected by baseline drift.
**When to use**: The absolute value of the parameter is masked by noise, drift, or offset, but changes in the parameter are significant.
**Example**: Detecting a slow chemical leak — absolute concentration measurements fluctuate with ventilation. Instead, measure dC/dt (rate of concentration change); a positive derivative above threshold indicates active leak regardless of baseline.
**Su-Field notation**:
```
Before: |X| measured (noisy, unreliable absolute value)
After:  dX/dt measured (cleaner signal, more sensitive to change)
```

### Subclass 4.4: Transition to Ferromagnetic Measurement (4 standards)

#### Standard 4.4.1 — Use Ferromagnetic Particles as Indicators
**Pattern**: Introduce ferromagnetic particles into or onto the object being measured, then use a magnetic field to detect their distribution pattern. Particles accumulate at anomalies, making invisible features visible.
**When to use**: Surface or near-surface features need detection but produce no signal with conventional methods.
**Example**: Magnetic particle inspection (MPI) — iron powder (S2) is applied to a magnetized steel part (S1); particles cluster at surface cracks where magnetic flux leaks, revealing defects invisible to the naked eye.
**Su-Field notation**:
```
Before: S1 (defects undetectable)
After:  Fmg
        |
    S1---S2_ferro   (ferromagnetic particles accumulate at defects)
```

#### Standard 4.4.2 — Use Ferrofluid for Conformable Detection
**Pattern**: Replace solid ferromagnetic particles with ferrofluid (magnetic nanoparticles in liquid carrier). The liquid conforms to complex surfaces, filling gaps and crevices for more thorough detection.
**When to use**: The surface geometry is complex (curved, recessed, threaded) and solid particles cannot reach all areas.
**Example**: Detecting leaks in complex seal assemblies — ferrofluid is applied to one side of the seal; a magnetic sensor on the other side detects any fluid that penetrates through micro-leaks.
**Su-Field notation**:
```
Before: Fmg
        |
    S1---S2_powder  (poor coverage on complex geometry)
After:  Fmg
        |
    S1---S2_ferrofluid  (conforms to all surface features)
```

#### Standard 4.4.3 — Use Curie Point for Passive Temperature Detection
**Pattern**: Exploit the Curie point (temperature at which ferromagnetic material loses magnetism) to create a passive, self-triggering temperature indicator. No external power or sensor needed.
**When to use**: Temperature monitoring is needed in inaccessible or hazardous locations where active sensors are impractical.
**Example**: Fire indicator labels — a ferromagnetic sticker on equipment is normally attracted to a magnetic backing; when temperature exceeds the Curie point (e.g., 360°C), the material becomes paramagnetic and the label falls off or changes state, permanently indicating overheating.
**Su-Field notation**:
```
Before: Fth (unknown temperature)  →  S1
After:  Fth → S2_ferro (at Curie point, magnetic property changes) → Fmg change detected
```

#### Standard 4.4.4 — Use Magnetostrictive Effect for Contact-Free Measurement
**Pattern**: Exploit magnetostriction (coupling between mechanical stress and magnetic properties) to measure mechanical parameters (force, torque, pressure) without physical contact.
**When to use**: Mechanical measurement is needed on rotating, moving, or inaccessible parts where contact sensors would interfere with operation.
**Example**: Non-contact torque measurement on a drive shaft — the shaft material (ferromagnetic steel) changes its magnetic permeability under torsional stress; a coil sensor near (but not touching) the shaft detects permeability changes, providing real-time torque readings.
**Su-Field notation**:
```
Before: Fme (torque — hard to measure on rotating shaft)
After:  Fme → S1_magnetostrictive → Fmg change → sensor  (mechanical-to-magnetic conversion)
```

### Subclass 4.5: Evolution of Measurement Systems (5 standards)

#### Standard 4.5.1 — Transition to Poly-System Measurement
**Pattern**: If a single measurement field provides insufficient information, use multiple different measurement fields simultaneously. Each field reveals different aspects of the object.
**When to use**: Single-field measurement is insufficient — it misses defect types, lacks resolution, or cannot distinguish between failure modes.
**Example**: Multi-modal medical imaging — combine X-ray (structural), ultrasound (soft tissue), and MRI (molecular) to build a complete diagnostic picture that no single modality can provide.
**Su-Field notation**:
```
Before: F1 → S1 (insufficient information)
After:  F1 + F2 + F3 → S1 (poly-field measurement → complete picture)
```

#### Standard 4.5.2 — Use Existing Fields for Measurement
**Pattern**: Instead of introducing a new measurement field, detect and analyze fields already present in or generated by the system during normal operation.
**When to use**: Adding a measurement field would disturb the process, or constraints prevent introducing new energy.
**Example**: Predictive maintenance via vibration analysis — a running motor already produces vibrations (existing field); analyzing the vibration spectrum reveals bearing wear, imbalance, and misalignment without adding any new sensors or energy.
**Su-Field notation**:
```
Before: F_existing (present but ignored)
After:  F_existing → analysis → measurement data
```

#### Standard 4.5.3 — Use Tracers for Flow and Distribution Measurement
**Pattern**: Introduce a small amount of detectable tracer substance into the system to track flow paths, distribution patterns, or residence times.
**When to use**: Internal flow or distribution cannot be observed directly; the system is opaque or too large for direct imaging.
**Example**: Radioactive tracer in petroleum pipelines — a tiny amount of radioactive isotope is injected at one point; detectors along the pipeline track its passage, revealing flow velocity, mixing zones, and blockage locations.
**Su-Field notation**:
```
Before: S1 (flow pattern unknown)
After:  S1 + S_tracer → F_detection → flow map revealed
```

#### Standard 4.5.4 — Use Physical Effects for Field Conversion
**Pattern**: When the parameter to be measured does not produce a directly detectable signal, use a physical effect to convert it into a different, detectable field type (e.g., mechanical → optical, thermal → electrical).
**When to use**: The target parameter exists in a field type for which no suitable sensor is available, but conversion to another field type enables measurement.
**Example**: Photoelastic stress analysis — a transparent model of a part is placed under load; stress (mechanical field) causes birefringence (optical effect), producing colored fringe patterns visible under polarized light that map the stress distribution.
**Su-Field notation**:
```
Before: Fme (stress — invisible)
After:  Fme → physical effect → Fem_optical (visible stress pattern)
```

#### Standard 4.5.5 — Transition from Continuous to Pulsed Measurement
**Pattern**: Replace continuous measurement with pulsed (time-domain) measurement. Pulsing enables time-of-flight analysis, background subtraction, signal averaging, and depth discrimination.
**When to use**: Continuous measurement suffers from noise, interference, or inability to distinguish signal from background.
**Example**: Pulsed ultrasonic thickness gauging — a short ultrasonic pulse is sent through a pipe wall; the time delay of the echo determines wall thickness. Pulsing allows gating out surface echoes and measuring only the back-wall reflection.
**Su-Field notation**:
```
Before: F_continuous → S1 (noisy, ambiguous)
After:  F_pulsed → S1 (time-gated, depth-resolved, background-rejected)
```

---

## Class 5: Helpers — Introducing Substances and Fields Under Constraints (17 standards)

**Purpose**: Practical strategies for cases where introducing new substances or fields seems impossible due to constraints (purity requirements, sealed systems, no external energy, prohibited additives). These standards provide creative workarounds.

### Subclass 5.1: Introducing Substances Under Constraints (5 standards)

#### Standard 5.1.1 — Use Void (Nothing) as a Substance
**Pattern**: When adding a substance is prohibited, use "nothing" — voids, bubbles, foam, hollow structures, or vacuum. The absence of substance provides insulation, cushioning, buoyancy, or selective passage without contamination.
**When to use**: No foreign substance is permitted in the system, but a function requiring a substance (insulation, separation, cushioning) is needed.
**Example**: Bubble wrap packaging — air-filled bubbles (void) provide cushioning without adding solid packing material; the "substance" doing the work is air trapped in thin film chambers.
**Su-Field notation**:
```
Before: S1---S2 (need S3 for separation, but S3 prohibited)
After:  S1---void---S2 (void performs the function of S3)
```

#### Standard 5.1.2 — Derive Substance from Existing System Components
**Pattern**: Instead of introducing a foreign substance, derive the needed substance from materials already in the system through chemical or physical transformation (oxidation, dissolution, erosion, decomposition).
**When to use**: Foreign substances are prohibited, but existing system materials can be transformed into the needed additive.
**Example**: Protective oxide layer — instead of adding a coating to aluminum (S1), expose it to controlled oxidation; the aluminum itself produces Al₂O₃ (derived S3) that forms a hard, protective surface layer.
**Su-Field notation**:
```
Before: Need S3 (protective substance, but foreign addition prohibited)
After:  F → S1 → S3_derived (S3 is produced from S1 itself)
```

#### Standard 5.1.3 — Use a Decomposable (Temporary) Substance
**Pattern**: If a substance is needed temporarily but must leave no residue, introduce a substance that decomposes, evaporates, or dissolves after performing its function.
**When to use**: A substance is needed during processing but must be completely absent from the final product.
**Example**: Lost-wax casting — a wax model (S3) defines the mold cavity; after the mold is formed, the wax is melted out, leaving the precise cavity with zero residue. Dry ice (CO₂) blasting cleans surfaces and sublimates completely.
**Su-Field notation**:
```
Before: Need S3 temporarily (but no residue allowed)
After:  S3_temp performs function → S3_temp decomposes → no trace remains
```

#### Standard 5.1.4 — Use Extreme Amounts (Trace or Overwhelming)
**Pattern**: If a substance is "prohibited," use it in such extreme quantity (either trace amount below detection/harm threshold, or overwhelming amount that becomes the new environment) that the prohibition no longer applies.
**When to use**: A substance is needed but prohibited at normal concentrations; however, at extreme concentrations (very low or very high) the prohibition rationale is eliminated.
**Example**: Homeopathic catalysis — a trace amount of catalyst (parts per billion) accelerates a reaction without contaminating the product above specification limits. Conversely, submerging electronic components in inert fluorocarbon liquid (overwhelming amount) provides cooling without the "added substance" being a contaminant — it becomes the environment.
**Su-Field notation**:
```
Before: S3 prohibited at normal concentration
After:  S3_trace (below threshold) or S3_overwhelming (becomes environment)
```

#### Standard 5.1.5 — Introduce Substance at a Different Location or Time
**Pattern**: If a substance cannot be introduced directly where needed, introduce it at a different location and let it migrate, or introduce it at a different time (before or after the critical period).
**When to use**: The operational zone is inaccessible or the substance would interfere during the critical process period.
**Example**: Pre-impregnation of bearings — sintered bronze bearings are soaked in lubricant (S3) during manufacturing (different time); during operation, the lubricant gradually migrates to the contact surface where it is needed.
**Su-Field notation**:
```
Before: Need S3 at location A during time T1 (inaccessible)
After:  Introduce S3 at location B during time T0 → S3 migrates to A by T1
```

### Subclass 5.2: Introducing Fields Under Constraints (3 standards)

#### Standard 5.2.1 — Use Self-Generated Fields
**Pattern**: Instead of introducing an external field, use fields generated by the system itself during operation (vibration, heat, pressure fluctuations, electromagnetic emissions).
**When to use**: No external energy source is available, or adding an external field would disturb the process.
**Example**: Energy harvesting from machinery vibration — a piezoelectric element converts the machine's own vibrations (self-generated mechanical field) into electrical energy to power wireless sensors, requiring no external power supply.
**Su-Field notation**:
```
Before: Need F (but no external source available)
After:  F_self-generated (harvested from system's own operation)
```

#### Standard 5.2.2 — Use Environmental Fields
**Pattern**: Instead of generating a field, use fields freely available in the environment: gravity, solar radiation, ambient temperature gradients, atmospheric pressure, wind, Earth's magnetic field.
**When to use**: No internal or external powered field source is available, but the environment provides usable energy.
**Example**: Solar chimney ventilation — a vertical black-painted tube uses solar radiation (environmental field) to heat air inside; hot air rises by convection (gravity-assisted), drawing fresh air through the building without fans or electricity.
**Su-Field notation**:
```
Before: Need F (no power source)
After:  F_environment (solar, gravity, thermal gradient — free and always available)
```

#### Standard 5.2.3 — Convert Available Field to Needed Field Type
**Pattern**: If the available field is the wrong type (e.g., mechanical when electrical is needed), use a physical effect to convert it to the required type.
**When to use**: A field is available but is the wrong type for the required function; a transducer or physical effect can bridge the gap.
**Example**: Ultrasonic horn — electrical energy (available field) is converted to high-intensity mechanical vibration (needed field) via a piezoelectric transducer, enabling ultrasonic welding.
**Su-Field notation**:
```
Before: F_available (wrong type for the function)
After:  F_available → transducer/effect → F_needed (correct type)
```

### Subclass 5.3: Using Phase Transitions (5 standards)

#### Standard 5.3.1 — Solid-Liquid Transition
**Pattern**: Use melting or freezing to create a temporary substance, generate force (expansion), or change properties reversibly. Ice-to-water and water-to-ice are the most accessible examples.
**When to use**: A temporary solid barrier, expansion force, or reversible shape change is needed.
**Example**: Ice plug technique for pipe repair — freeze a section of water-filled pipe to create a solid ice plug (temporary valve) upstream of the repair area; after repair, thaw the plug to restore flow. No permanent modification needed.
**Su-Field notation**:
```
Before: Need temporary S3 (barrier/plug)
After:  H₂O → ice (solid, performs barrier function) → H₂O (removed by thawing)
```

#### Standard 5.3.2 — Liquid-Gas Transition
**Pattern**: Use boiling, evaporation, or cavitation to generate expansion force, create bubbles for mixing/cleaning, or produce a gas from a liquid already present in the system.
**When to use**: Expansion force, agitation, or gas generation is needed; a liquid is already present in the system.
**Example**: Steam cleaning — water (already present or easily added) is heated past boiling point; the expanding steam (1,700× volume increase) provides powerful cleaning force that penetrates crevices, with the "substance" (water) leaving no harmful residue.
**Su-Field notation**:
```
Before: Need F_expansion (or gas for agitation)
After:  S_liquid → Fth → S_gas (phase transition provides force/substance)
```

#### Standard 5.3.3 — Structural Phase Transition (Allotropic/Crystallographic)
**Pattern**: Use structural phase transitions (crystal structure changes, allotropic transitions) to obtain shape change, force generation, or property switching without adding new substances.
**When to use**: A shape change or property switch is needed that is reversible and precisely controllable by temperature or field.
**Example**: Shape-memory alloy (SMA) actuators — a NiTi wire is deformed at low temperature; when heated above its transition temperature, it returns to its "memorized" shape, generating significant force. Used as actuators in medical stents (expand on body temperature) and satellite deployment mechanisms.
**Su-Field notation**:
```
Before: Need Fme (mechanical actuation force)
After:  Fth → S_SMA (structural transition) → Fme (shape recovery generates force)
```

#### Standard 5.3.4 — Dual-Phase State (Emulsions, Suspensions, Foams)
**Pattern**: Use dual-phase systems (liquid-liquid emulsion, solid-liquid suspension, gas-liquid foam) to combine properties of both phases in a single working substance.
**When to use**: A single-phase substance cannot provide the needed combination of properties (e.g., both flowability and abrasiveness, both lubrication and solid particle delivery).
**Example**: Grinding slurry (CMP) — a suspension of abrasive nanoparticles in chemical solution combines mechanical abrasion (solid phase) with chemical etching (liquid phase), achieving planarization that neither phase alone can accomplish.
**Su-Field notation**:
```
Before: S2 (single phase — cannot provide both properties)
After:  S2_dual (two phases combined — both properties available)
```

#### Standard 5.3.5 — Use Boundary Effects (Capillary, Surface Tension, Wetting)
**Pattern**: Exploit phenomena that occur at phase boundaries — capillary action, surface tension, wetting/non-wetting, meniscus formation — as sources of force, transport, or selective behavior.
**When to use**: A transport mechanism or force is needed without pumps or external pressure; surfaces or microstructures are present that can drive capillary effects.
**Example**: Heat pipe — liquid evaporates at the hot end (absorbing heat), vapor travels to the cold end (releasing heat), and condensed liquid returns to the hot end via capillary wicking through a sintered metal wick structure. No pump needed — capillary forces provide the return transport.
**Su-Field notation**:
```
Before: Need F_transport (but no pump/pressure available)
After:  F_capillary (boundary effect provides transport force for free)
```

### Subclass 5.4: Using Physical Effects (2 standards)

#### Standard 5.4.1 — Use Self-Controlling (Self-Regulating) Physical Effects
**Pattern**: Select physical effects that are inherently self-limiting or self-regulating, so the system controls itself without external feedback or sensors.
**When to use**: Active control (sensors, feedback loops, controllers) is impractical, too expensive, or unreliable; a passive self-regulating mechanism is preferred.
**Example**: PTC (Positive Temperature Coefficient) thermistor as a self-regulating heater — resistance increases sharply above a set temperature, automatically reducing current and heat output. The heater stabilizes at its design temperature without any thermostat or control circuit.
**Su-Field notation**:
```
Before: F (uncontrolled — needs external regulation)
After:  F_self-regulating (physical effect provides built-in negative feedback)
```

#### Standard 5.4.2 — Consult the Physical Effects Catalog
**Pattern**: When the needed function is known but no mechanism is apparent, systematically search the catalog of physical effects indexed by function (generate force, change shape, detect parameter, transport substance, etc.) to find a suitable effect.
**When to use**: The problem has been clearly formulated but the solution mechanism is unknown; a systematic search of known physical effects can reveal non-obvious solutions.
**Example**: Need to generate precise micro-displacement without mechanical linkages — consulting the effects catalog under "generate displacement" reveals: piezoelectric effect (voltage → displacement), magnetostriction (magnetic field → displacement), thermal expansion, and electrostriction. Piezo is selected for nanometer precision.
**Su-Field notation**:
```
Before: F_in → ? → desired function (mechanism unknown)
After:  F_in → physical effect (from catalog) → F_out (desired function achieved)
```

### Subclass 5.5: Experimental Standards — Working at Particle Level (2 standards)

#### Standard 5.5.1 — Decompose Macro-Substance into Micro-Particles
**Pattern**: If a macro-level substance cannot perform the required function, decompose it into micro- or nano-scale particles. Smaller particles have higher surface-area-to-volume ratio, different physical properties, and can access spaces that macro-substances cannot.
**When to use**: The needed substance exists but its macro-scale properties are inadequate; micro/nano-scale versions would have enhanced reactivity, penetration, or distribution.
**Example**: Ceramic nanoparticles in coatings — bulk ceramic is brittle and hard to apply; grinding it to nanoparticles allows it to be suspended in liquid and sprayed as a thin, uniform, crack-resistant coating with enhanced hardness.
**Su-Field notation**:
```
Before: S_macro (inadequate properties at macro scale)
After:  S_macro → S_micro/nano (enhanced properties at particle level)
```

#### Standard 5.5.2 — Combine Precursors to Generate Needed Substance In Situ
**Pattern**: If the needed substance cannot be introduced directly (it is unstable, dangerous, or unavailable in ready form), introduce two or more precursor substances that combine in situ to generate the needed substance at the point of use.
**When to use**: The required substance is unstable, hazardous to transport, or unavailable in ready form; but its precursors are stable and easily introduced separately.
**Example**: Two-part epoxy adhesive — neither resin nor hardener alone provides bonding; mixed at the point of use, they react to form a strong structural adhesive. Similarly, in-situ corrosion inhibitor generation — two harmless precursor chemicals are injected into a pipeline; they react at the corrosion site to form a protective inhibitor film.
**Su-Field notation**:
```
Before: Need S3 (but S3 is unavailable/unstable/dangerous to introduce directly)
After:  S3a + S3b → S3 (precursors combine in situ to generate needed substance)
```

---

## Quick Reference Table

| Class | Standards | Focus |
|-------|-----------|-------|
| 1 | 1.1.1 – 1.2.5 (13) | Build or destroy Su-Field models |
| 2 | 2.1.1 – 2.4.13 (23) | Develop and intensify existing Su-Fields |
| 3 | 3.1.1 – 3.2.2 (6) | System transitions (bi/poly, micro-level) |
| 4 | 4.1.1 – 4.5.5 (17) | Detection and measurement |
| 5 | 5.1.1 – 5.5.2 (17) | Introduce substances/fields under constraints |

**Total: 76 Standard Solutions**

## Usage Guide

1. **Model** your problem as a Su-Field system (identify S1, S2, F) — see [sufield-protocol.md](sufield-protocol.md)
2. **Classify** the problem type: incomplete, harmful, insufficient, excessive, or measurement
3. **Navigate** to the primary class for your problem type (use the mapping table in sufield-protocol.md)
4. **Scan** each subclass within that class for applicable transformation patterns
5. **Map** the abstract pattern onto your specific substances and fields
6. **Generate** 3-5 concrete solution concepts from the matching standards
7. **Evaluate** each concept against the Ideal Final Result (see [ifr-protocol.md](ifr-protocol.md))
6. **Generate** concepts
7. **Evaluate** vs IFR
