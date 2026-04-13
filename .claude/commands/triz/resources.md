---
name: triz:resources
description: "Resource Analysis — discover hidden resources in and around the system"
argument-hint: "[System/Situation: <text>] [--format mermaid|ascii] [--depth shallow|deep]"
---

EXECUTE IMMEDIATELY — do not deliberate, do not ask clarifying questions before reading the protocol.

## Argument Parsing (do this FIRST)

Extract from $ARGUMENTS:

- **System**: The system or situation to mine for hidden, underutilized, or free resources. The entire argument text IS the system if not explicitly labeled.
- **Format**: `mermaid` (default) or `ascii`. Set by `--format`.
- **Depth**: `shallow` (default, scan 3-4 resource categories with top findings) or `deep` (exhaustive scan of all 7 resource categories across system, super-system, and environment, with derivative resources). Set by `--depth`.

If System is missing or too vague, use AskUserQuestion:

```
header: "System"
question: "Describe the system or situation where you want to find hidden resources. What components exist? What is the environment? What waste, byproducts, or unused elements are present? What problem are you trying to solve with these resources?"
```

## Execution

1. Read the protocol file:
   ```
   .claude/skills/triz/references/resources-protocol.md
   ```

2. Read the output format specification:
   ```
   .claude/skills/triz/references/output-format.md
   ```

3. Execute the Resource Analysis protocol:
   - Phase 1: Define the system boundary — system, super-system, environment
   - Phase 2: Scan all 7 resource categories:
     1. **Substance resources** — materials, objects, waste, byproducts (in system, super-system, environment)
     2. **Field/Energy resources** — existing forces, energy flows, gradients, vibrations, thermal, electromagnetic
     3. **Space resources** — empty spaces, surfaces, volumes, nesting opportunities, another dimension
     4. **Time resources** — idle time, pauses, pre-action, post-action, parallel operations
     5. **Information resources** — signals, data, feedback, copies, models, traces
     6. **Functional resources** — existing functions that can be repurposed, combined, or inverted
     7. **Derivative resources** — resources created by combining or modifying other resources
   - Phase 3: For each found resource, assess:
     - Availability (free / low cost / requires modification)
     - Applicability to the problem
     - How to mobilize it (what change is needed to use it)
   - Phase 4: Rank resources by value = (impact on problem) x (availability) / (cost to mobilize)
   - Phase 5: Generate solution concepts using top resources
   - Phase 6: Render output in requested format

4. Present the result with:
   - System boundary diagram (system / super-system / environment)
   - Resource inventory table organized by category
   - Top 5-10 resources ranked by value
   - For each top resource: what it is, where it comes from, how to use it
   - Solution concepts that leverage the best resources (prefer free or nearly free)
   - Suggested next step: `/triz:sufield` to model new interactions using found resources, `/triz:ifr` to check if resources enable the ideal solution
