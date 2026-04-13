---
name: triz:ifr
description: "Ideal Final Result — define the perfect solution with zero cost"
argument-hint: "[Problem/System: <text>] [--format mermaid|ascii] [--depth shallow|deep]"
---

EXECUTE IMMEDIATELY — do not deliberate, do not ask clarifying questions before reading the protocol.

## Argument Parsing (do this FIRST)

Extract from $ARGUMENTS:

- **Problem**: The system or problem to idealize. What function should be delivered perfectly, with zero cost, zero harm, and zero complexity? The entire argument text IS the problem if not explicitly labeled.
- **Format**: `mermaid` (default) or `ascii`. Set by `--format`.
- **Depth**: `shallow` (default, single IFR statement with gap analysis) or `deep` (multiple IFR formulations at different system levels — component, system, super-system — with ideality evolution path). Set by `--depth`.

If Problem is missing or too vague, use AskUserQuestion:

```
header: "Problem"
question: "Describe the system or problem you want to idealize. What useful function must be delivered? What harmful effects or costs currently exist? Imagine the perfect outcome — what would it look like if the problem solved itself?"
```

## Execution

1. Read the protocol file:
   ```
   .claude/skills/triz/references/ifr-protocol.md
   ```

2. Read the output format specification:
   ```
   .claude/skills/triz/references/output-format.md
   ```

3. Execute the Ideal Final Result protocol:
   - Phase 1: Define the Primary Useful Function (PUF) of the system
   - Phase 2: List all harmful effects, costs, and complexity in the current system
   - Phase 3: Formulate the IFR: "The [system element] ITSELF [performs the function], WITHOUT [harmful effects], WHILE [maintaining all useful functions]"
   - Phase 4: Calculate Ideality = Sum(Useful Functions) / Sum(Harmful Effects + Costs)
   - Phase 5: Gap Analysis — what prevents the IFR from being reality right now?
   - Phase 6: Identify which gaps are physical contradictions (hand off to `/triz:contradiction`)
   - Phase 7: If depth=deep, formulate IFR at component, system, and super-system levels
   - Phase 8: Render output in requested format

4. Present the result with:
   - Current system description with PUF
   - IFR statement in standard "X ITSELF does Y" form
   - Ideality score (current vs. ideal)
   - Gap analysis — specific barriers to achieving IFR
   - Physical contradictions embedded in the gaps
   - Suggested next step: `/triz:contradiction` to formulate contradictions from gaps, `/triz:resources` to find free ways to close gaps
