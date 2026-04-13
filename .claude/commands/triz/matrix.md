---
name: triz:matrix
description: "Contradiction Matrix — map improving/worsening parameters to principles"
argument-hint: "[Parameters: <improving> vs <worsening>] [--format mermaid|ascii] [--depth shallow|deep]"
---

EXECUTE IMMEDIATELY — do not deliberate, do not ask clarifying questions before reading the protocol.

## Argument Parsing (do this FIRST)

Extract from $ARGUMENTS:

- **Parameters**: Two conflicting engineering parameters — one improving, one worsening. Look for patterns like "X vs Y", "improving X worsens Y", or a pair of the 39 parameters. The entire argument text IS the parameter description if not explicitly labeled.
- **Format**: `mermaid` (default) or `ascii`. Set by `--format`.
- **Depth**: `shallow` (default, single matrix lookup with top principles) or `deep` (multiple parameter mappings, cross-referencing, and principle overlap analysis). Set by `--depth`.

If Parameters are missing or unclear, use AskUserQuestion:

```
header: "Parameters"
question: "What two parameters are in conflict? State: (1) What parameter are you trying to IMPROVE? (2) What parameter gets WORSE as a result? Examples: 'speed vs accuracy', 'strength vs weight', 'productivity vs quality'."
```

## Execution

1. Read the protocol file:
   ```
   .claude/skills/triz/references/matrix-protocol.md
   ```

2. Read the output format specification:
   ```
   .claude/skills/triz/references/output-format.md
   ```

3. Execute the Contradiction Matrix protocol:
   - Phase 1: Map the user's improving parameter to one of the 39 Engineering Parameters
   - Phase 2: Map the user's worsening parameter to one of the 39 Engineering Parameters
   - Phase 3: Look up the matrix cell — retrieve recommended Inventive Principles (typically 2-4)
   - Phase 4: For each recommended principle, explain its relevance to this specific conflict
   - Phase 5: Generate domain-specific solution concepts for each principle
   - Phase 6: If depth=deep, try alternative parameter mappings and compare results
   - Phase 7: Render output in requested format

4. Present the result with:
   - Parameter mapping table: user's terms → 39 standard parameters (with parameter numbers)
   - Matrix cell result: principle numbers and names
   - For each principle: explanation + concrete solution concept
   - If depth=deep: alternative mappings and their results
   - Suggested next step: `/triz:40p` for deeper principle exploration, `/triz:contradiction` to refine the contradiction
