# Resource Analysis Protocol

## Core Concept

Every technical problem exists within a context rich with untapped resources. Resource analysis is the systematic identification of substances, fields, spaces, time windows, information, and functional capabilities already present in or near the system that can be used to solve the problem without introducing new, expensive elements.

The best TRIZ solutions use resources that are:
- **Already present** in the system or its immediate environment
- **Free or nearly free** — waste products, by-products, unused capacity
- **Available at the right time and place** — where the problem occurs

Resource analysis is not brainstorming. It is a structured survey using six defined categories, applied to three concentric zones: the system itself, the supersystem, and the environment.

## The Three Resource Zones

### Zone 1: System Resources
Elements within the system boundary — components, working substances, operating fields, internal spaces. These are the most desirable resources because they require no external additions.

### Zone 2: Supersystem Resources
Elements of the larger system that contains the system under analysis — adjacent machines, infrastructure, operators, input materials, output products. Available but may require interface changes.

### Zone 3: Environmental Resources
Elements of the natural environment — gravity, ambient temperature, atmospheric pressure, sunlight, humidity, wind, available water. Free but may be intermittent or uncontrollable.

## Six Resource Categories

### 1. Substance Resources

Physical materials available for use in solving the problem.

**System substances**:
- Working materials (the substance being processed)
- Tool materials (the components doing the processing)
- Waste and by-products (chips, heat, exhaust, scrap)
- Wear products (particles from friction, erosion)

**Supersystem substances**:
- Input raw materials before processing
- Output products after processing
- Adjacent system materials
- Packaging, containers, transport media

**Environmental substances**:
- Air (nitrogen, oxygen, CO2, water vapor)
- Water (surface, ground, humidity)
- Soil, dust, sand
- Biological organisms (bacteria, fungi, plants)

**Analysis questions**:
- What substances are present at the problem location right now?
- What substances pass through the problem zone?
- What waste substances are generated near the problem?
- Can any present substance serve a dual function?

### 2. Field and Energy Resources

Energy sources and force fields available in or near the system.

**System fields**:
- Mechanical energy (vibration, pressure, rotation, flow)
- Thermal energy (heat from friction, process heat, exhaust)
- Electrical energy (power supply, static charges, EMF)
- Chemical energy (fuel, reactions, electrochemical)

**Supersystem fields**:
- Power grid, compressed air systems
- Heating/cooling infrastructure
- Communication signals (RF, network)
- Adjacent process energy (waste heat from neighbor)

**Environmental fields**:
- Gravitational field (always present, free)
- Solar radiation (light, heat, UV)
- Earth's magnetic field
- Atmospheric pressure differential
- Wind, water current, tidal forces
- Geothermal energy

**Analysis questions**:
- What energy is currently being wasted in the system?
- What forces or fields already pass through the problem zone?
- What energy sources are available but currently unused?
- Can an existing field perform a secondary function?

### 3. Space Resources

Physical volumes, surfaces, and geometries available for exploitation.

**Internal spaces**:
- Hollow interiors of components
- Gaps between components
- Pores, channels, and capillaries within materials
- Surface texture (roughness, patterns)

**Interface spaces**:
- Boundaries between components
- Contact surfaces
- Clearance gaps required for assembly

**External spaces**:
- Volume above, below, beside the system
- Unused dimensions (if 2D process, the third dimension is available)
- Nested spaces (Matryoshka principle)

**Analysis questions**:
- Are there empty spaces inside or between components?
- Can existing surfaces be used for an additional function?
- Is the system using all three spatial dimensions?
- Can components be nested to save space?
- Are there surfaces that could carry information (markings, textures)?

### 4. Time Resources

Temporal windows and sequencing opportunities.

**Pre-action time**:
- Preparation before the main operation
- Pre-treatment, pre-loading, pre-positioning
- Actions performed during manufacturing (before the product reaches the user)

**Parallel time**:
- Actions that can occur simultaneously with the main operation
- Background processes
- Overlap between sequential steps

**Post-action time**:
- Cooling periods, settling time, transport time
- Time between operational cycles (idle time)
- Maintenance windows

**Off-peak time**:
- Night shifts, weekends, seasonal lulls
- Low-demand periods in variable-load systems

**Micro-time**:
- Intervals between pulses, cycles, or strokes
- Transition periods between phases

**Analysis questions**:
- What happens before, during, and after the main operation?
- Are there idle periods that could be productively used?
- Can preparation be done in advance to speed the main operation?
- Can multiple actions overlap in time?
- Are there natural pauses that could accommodate additional functions?

### 5. Information Resources

Data, signals, and knowledge available in the system.

**Direct information**:
- Sensor readings already being collected
- Process parameters being monitored
- User inputs and selections

**Indirect information**:
- Vibration patterns that indicate machine state
- Temperature profiles that reveal process quality
- Sound that signals normal vs. abnormal operation
- Color changes that indicate chemical state

**Historical information**:
- Past performance data
- Maintenance records
- Failure logs and patterns
- Seasonal and cyclical trends

**Derivative information**:
- Rates of change (derivatives of existing measurements)
- Correlations between parameters
- Statistical distributions and anomalies

**Analysis questions**:
- What data is being collected but not fully exploited?
- What physical phenomena produce detectable signals at the problem location?
- What historical patterns could predict future events?
- Can existing measurements be combined to derive new insights?
- What information exists in the physical state of materials (wear patterns, discoloration)?

### 6. Functional Resources

Capabilities of existing components that can be repurposed or extended.

**Underused functions**:
- Components performing their primary function at partial capacity
- Components with inherent capabilities not currently exploited
- Structural elements that could also conduct, insulate, or sense

**Latent functions**:
- Every component has physical properties beyond its intended function
- A wire conducts electricity (primary) but also has tensile strength, thermal conductivity, reflectivity
- A housing provides containment (primary) but also has thermal mass, electromagnetic shielding, structural rigidity

**Inverse functions**:
- Can a component's harmful side effect become useful?
- Can a waste output become a useful input?
- Can a failure mode be exploited constructively?

**Analysis questions**:
- Which components are operating well below capacity?
- What physical properties do existing components have beyond their assigned function?
- Are any harmful effects or waste outputs potentially useful elsewhere?
- Can existing components serve double or triple duty?

## Process

### Step 1: Map All Available Resources

Work through each of the six categories across all three zones (system, supersystem, environment). Use a resource inventory table:

```
Category      | Zone    | Resource              | Currently Used? | Potential Use
-------------|---------|----------------------|----------------|------------------
Substance    | System  | Cooling water         | Cooling only   | Cleaning, transport
Substance    | Environ | Ambient air           | No             | Pneumatic force
Field        | System  | Waste heat from motor | Wasted         | Pre-heating input
Space        | System  | Interior of shaft     | Empty          | Wiring conduit
Time         | System  | 3s between cycles     | Idle           | Self-inspection
Information  | System  | Motor current draw    | Basic monitor  | Predictive maint.
Functional   | System  | Housing rigidity      | Structural     | Vibration damping
```

### Step 2: Identify Unused and Underused Resources

From the inventory, flag resources that are:
- Present but completely unused
- Present but used far below capacity
- Generated as waste or by-product
- Available for free from the environment

These are the primary candidates for solving the problem.

### Step 3: Match Resources to Problem Requirements

State the problem in functional terms: "I need [field/substance] at [location] during [time] to [perform function]."

Then search the resource inventory:
- Which substances are available at that location?
- Which fields are present at that time?
- Which spaces could accommodate the solution?
- Which existing components could take on this function?

### Step 4: Generate Resource-Based Solutions

For each promising resource match:
1. How specifically would this resource solve the problem?
2. What modification (if any) is needed to deploy it?
3. Does using this resource create any new problems?
4. How close does this solution come to the IFR?

Generate at least 3 solutions using different resource combinations.

### Step 5: Prioritize by Availability and Implementation Ease

Rank solutions on a 2x2 matrix:

```
                    Easy to Implement
                    |
        Quick Wins  |  Strategic Wins
                    |
  ──────────────────┼──────────────────
                    |
        Low Value   |  Complex Projects
                    |
                    Low Availability → High Availability
```

Prefer solutions using:
- Resources already at the problem location (no transport)
- Resources in continuous supply (no depletion risk)
- Resources requiring no modification (use as-is)
- Free resources over purchased ones

## Resource Analysis Heuristics

1. **The best resource is one that is harmful** — if you can turn a harmful substance, field, or effect into the solution, you solve two problems at once (eliminate the harm AND deliver the function).

2. **Waste equals opportunity** — every waste stream (heat, material, vibration, data) is an unused resource. The system is already paying the cost of generating it.

3. **The void is a substance** — empty space, vacuum, bubbles, and foam are legitimate substance resources. Void has properties: thermal insulation, compressibility, low density, transparency.

4. **Time is a design parameter** — if a function cannot be performed during operation, consider performing it before operation (pre-action), after operation (post-action), or between cycles (micro-time).

5. **The object is a resource** — the thing being processed (workpiece, customer, data record) is often the most available substance resource. Can it perform the function on itself?

6. **Copied resources** — if the ideal resource exists elsewhere but cannot be transported, can its key property be replicated using locally available materials? Copy the function, not the substance.

## Integration with Other TRIZ Tools

- **Su-Field**: Resource analysis identifies candidate substances (S2, S3) and fields (F) for building or modifying Su-Field models
- **IFR**: The IFR template explicitly calls for "using only available resources" — resource analysis populates this constraint
- **Trimming**: When a component is trimmed (Rule A), resource analysis identifies which remaining component can receive the transferred function
- **Evolution**: Law 2 (increasing ideality) favors solutions that use existing resources over those requiring new additions
- **Contradiction**: When a contradiction seems unresolvable, resource analysis often reveals a substance or field that can satisfy both requirements simultaneously
