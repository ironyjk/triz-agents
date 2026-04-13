---
name: triz:sufield
description: "Substance-Field (Su-Field) analysis and modeling"
argument-hint: "[System: <text>] [--format mermaid|ascii] [--depth shallow|deep]"
---

EXECUTE IMMEDIATELY — do not deliberate, do not ask clarifying questions before reading the protocol.

## Argument Parsing (do this FIRST)

Extract from $ARGUMENTS:

- **System**: A system with interactions to model — especially incomplete, insufficient, or harmful interactions between substances (objects) and fields (energy/forces). The entire argument text IS the system if not explicitly labeled.
- **Format**: `mermaid` (default) or `ascii`. Set by `--format`.
- **Depth**: `shallow` (default, single Su-Field model with primary transformation) or `deep` (chain of Su-Field models showing progressive transformations, including 76 Standard Solutions mapping). Set by `--depth`.

If System is missing or too vague, use AskUserQuestion:

```
header: "System"
question: "Describe the system you want to analyze. What objects (substances) are involved? What forces, energies, or interactions (fields) act between them? What is the problem — is an interaction missing, insufficient, or harmful?"
```

## Execution

1. Read the protocol file:
   ```
   .claude/skills/triz/references/sufield-protocol.md
   ```

2. Read the output format specification:
   ```
   .claude/skills/triz/references/output-format.md
   ```

3. Execute the Su-Field Analysis protocol:
   - Phase 1: Identify Substances (S1 = tool/agent, S2 = object/product) and Field (F = energy/force/interaction)
   - Phase 2: Build the Su-Field model diagram — classify as:
     - Incomplete (missing element)
     - Ineffective/Insufficient (weak desired action)
     - Harmful (unwanted side effect)
     - Complete and effective (no problem — verify scope)
   - Phase 3: Apply the appropriate transformation rule:
     - Incomplete → Complete the model (add missing S or F)
     - Insufficient → Add a new substance S3 or modify the field
     - Harmful → Add S3 to block, introduce a counter-field, or chain models
   - Phase 4: Map to the 76 Standard Solutions (if depth=deep)
   - Phase 5: Generate specific solution concepts from the transformed model
   - Phase 6: Render output in requested format

4. Present the result with:
   - Original Su-Field model (S1, S2, F) with diagram
   - Problem classification (incomplete/insufficient/harmful)
   - Transformed Su-Field model with diagram
   - Applicable Standard Solution class and number (if depth=deep)
   - Concrete solution concept derived from the transformation
   - Suggested next step: `/triz:resources` to find substances/fields in the environment, `/triz:trimming` if the model is over-complicated
