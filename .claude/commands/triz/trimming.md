---
name: triz:trimming
description: "Trimming — systematically remove components while keeping functions"
argument-hint: "[System: <text>] [--format mermaid|ascii] [--depth shallow|deep]"
---

EXECUTE IMMEDIATELY — do not deliberate, do not ask clarifying questions before reading the protocol.

## Argument Parsing (do this FIRST)

Extract from $ARGUMENTS:

- **System**: The system to simplify by removing components. What are its parts? What does each part do? Which parts seem redundant, expensive, or problematic? The entire argument text IS the system if not explicitly labeled.
- **Format**: `mermaid` (default) or `ascii`. Set by `--format`.
- **Depth**: `shallow` (default, trim 1-2 components with function redistribution) or `deep` (full functional model + systematic trimming of all trimmable components + cascading effects). Set by `--depth`.

If System is missing or too vague, use AskUserQuestion:

```
header: "System"
question: "Describe the system you want to simplify. List its main components and what each one does. Which components are expensive, problematic, or seem unnecessary? What is the system's primary function?"
```

## Execution

1. Read the protocol file:
   ```
   .claude/skills/triz/references/trimming-protocol.md
   ```

2. Read the output format specification:
   ```
   .claude/skills/triz/references/output-format.md
   ```

3. Execute the Trimming protocol:
   - Phase 1: Build a Functional Model — list all components and their functions (useful, harmful, insufficient)
   - Phase 2: Rank components by trimming priority:
     - Rule A: The function is not needed (eliminate)
     - Rule B: Another existing component can perform the function (reassign)
     - Rule C: A modified component or super-system element can perform the function (redesign)
   - Phase 3: For each trimmable component, determine which rule applies and how its functions are redistributed
   - Phase 4: Check for cascading effects — does trimming component X break anything downstream?
   - Phase 5: Calculate complexity reduction and ideality improvement
   - Phase 6: Render output in requested format

4. Present the result with:
   - Functional Model: components, functions, and interactions (diagram)
   - Trimming candidates ranked by priority
   - For each trimmed component: which rule, where the function goes, and any new contradictions introduced
   - Before/After system comparison (component count, cost, complexity)
   - Suggested next step: `/triz:contradiction` if trimming introduces new contradictions, `/triz:ifr` to verify alignment with ideal
