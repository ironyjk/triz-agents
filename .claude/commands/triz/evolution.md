---
name: triz:evolution
description: "Laws of Technical System Evolution — predict next-generation designs"
argument-hint: "[System/Technology: <text>] [--format mermaid|ascii] [--depth shallow|deep]"
---

EXECUTE IMMEDIATELY — do not deliberate, do not ask clarifying questions before reading the protocol.

## Argument Parsing (do this FIRST)

Extract from $ARGUMENTS:

- **System**: The system or technology to analyze for evolutionary trends and predict its next generation. The entire argument text IS the system if not explicitly labeled.
- **Format**: `mermaid` (default) or `ascii`. Set by `--format`.
- **Depth**: `shallow` (default, assess 3-4 most relevant evolution laws with current position) or `deep` (all 8 laws assessed, with multi-generation roadmap and S-curve positioning). Set by `--depth`.

If System is missing or too vague, use AskUserQuestion:

```
header: "System"
question: "Describe the system or technology you want to analyze for evolutionary trends. What is its current form? How has it changed over time? What limitations does it face today?"
```

## Execution

1. Read the protocol file:
   ```
   .claude/skills/triz/references/evolution-protocol.md
   ```

2. Read the output format specification:
   ```
   .claude/skills/triz/references/output-format.md
   ```

3. Execute the Evolution Analysis protocol:
   - Phase 1: Position the system on the S-Curve (infancy, growth, maturity, decline)
   - Phase 2: Assess against the 8 Laws of Technical System Evolution:
     1. Completeness of parts (engine, transmission, working body, control)
     2. Energy conductivity
     3. Harmonization of rhythms
     4. Increasing ideality
     5. Uneven development of parts
     6. Transition to super-system
     7. Transition from macro to micro level
     8. Increasing dynamism and controllability
   - Phase 3: Identify the weakest subsystem (uneven development)
   - Phase 4: Predict next evolutionary steps based on unfulfilled laws
   - Phase 5: Generate specific next-generation design concepts
   - Phase 6: Render output in requested format

4. Present the result with:
   - S-Curve position with evidence
   - Scorecard: each evolution law rated (fulfilled / partially / unfulfilled)
   - Weakest subsystem identified (highest leverage for innovation)
   - Predicted next-generation features (1-3 generations ahead)
   - Specific design concepts for the next evolutionary step
   - Suggested next step: `/triz:ifr` to define the ideal next generation, `/triz:trimming` if system is at maturity/decline
