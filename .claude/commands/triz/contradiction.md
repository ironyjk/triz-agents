---
name: triz:contradiction
description: "Identify and formulate technical and physical contradictions"
argument-hint: "[Problem/System: <text>] [--format mermaid|ascii] [--depth shallow|deep]"
---

EXECUTE IMMEDIATELY — do not deliberate, do not ask clarifying questions before reading the protocol.

## Argument Parsing (do this FIRST)

Extract from $ARGUMENTS:

- **Problem**: The system, situation, or design challenge where something improves but something else gets worse, or where a parameter must simultaneously have two opposite values. The entire argument text IS the problem if not explicitly labeled.
- **Format**: `mermaid` (default) or `ascii`. Set by `--format`.
- **Depth**: `shallow` (default, 1-2 technical contradictions + 1 physical contradiction) or `deep` (3-5 technical contradictions + 2-3 physical contradictions with intensification). Set by `--depth`.

If Problem is missing or too vague to identify conflicting requirements, use AskUserQuestion:

```
header: "Problem"
question: "Describe the system or design challenge. What are you trying to improve? What gets worse when you try to improve it? Or what property needs to be both X and not-X at the same time?"
```

## Execution

1. Read the protocol file:
   ```
   .claude/skills/triz/references/contradiction-protocol.md
   ```

2. Read the output format specification:
   ```
   .claude/skills/triz/references/output-format.md
   ```

3. Execute the Contradiction Analysis protocol:
   - Phase 1: Describe the system — components, functions, parameters
   - Phase 2: Identify Technical Contradictions (TC) — "If we improve Parameter A, then Parameter B worsens"
   - Phase 3: Map to the 39 Engineering Parameters (improving vs. worsening)
   - Phase 4: Identify Physical Contradictions (PC) — "Parameter X must be LARGE to [function] AND must be SMALL to [function]"
   - Phase 5: Intensify the PC — push both sides to extremes
   - Phase 6: Render output in requested format

4. Present the result with:
   - System description and key parameters
   - Technical Contradiction(s) in standard "IF...THEN...BUT..." form
   - Mapped 39-parameter pairs (ready for `/triz:matrix`)
   - Physical Contradiction(s) in standard "X must be A AND not-A" form
   - Intensified contradiction statement
   - Suggested next steps: `/triz:matrix` for TC resolution, `/triz:40p` for direct principle application
