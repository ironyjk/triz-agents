---
name: triz:ariz
description: "ARIZ — Algorithm of Inventive Problem Solving (full structured process)"
argument-hint: "[Problem: <text>] [--format mermaid|ascii] [--depth shallow|deep]"
---

EXECUTE IMMEDIATELY — do not deliberate, do not ask clarifying questions before reading the protocol.

## Argument Parsing (do this FIRST)

Extract from $ARGUMENTS:

- **Problem**: A complex inventive problem that resists conventional approaches. The entire argument text IS the problem if not explicitly labeled.
- **Format**: `mermaid` (default) or `ascii`. Set by `--format`.
- **Depth**: `shallow` (default, ARIZ Parts 1-3: analysis through IFR) or `deep` (full ARIZ Parts 1-9: analysis through solution verification and generalization). Set by `--depth`.

If Problem is missing or too vague, use AskUserQuestion:

```
header: "Problem"
question: "Describe the complex inventive problem you want to solve. What system is involved? What do you want it to do that it currently cannot? What have you already tried? Why didn't conventional approaches work?"
```

## Execution

1. Read the protocol file:
   ```
   .claude/skills/triz/references/ariz-protocol.md
   ```

2. Read the output format specification:
   ```
   .claude/skills/triz/references/output-format.md
   ```

3. Execute the ARIZ protocol (based on ARIZ-85C):
   - **Part 1: Problem Analysis**
     - Step 1.1: State the mini-problem (preserve everything, change one thing)
     - Step 1.2: Identify the conflicting pair (tool + object)
     - Step 1.3: Formulate Technical Contradiction 1 (TC-1)
     - Step 1.4: Formulate Technical Contradiction 2 (TC-2)
     - Step 1.5: Choose the TC that delivers the primary useful function
     - Step 1.6: Intensify the conflict — push to extremes
     - Step 1.7: Identify the Operative Zone (OZ) — where the conflict physically occurs
   - **Part 2: Problem Model**
     - Step 2.1: Identify the Operative Time (OT) — when the conflict occurs
     - Step 2.2: Identify the Substance-Field Resources (SFR)
     - Step 2.3: Formulate the Ideal Final Result (IFR)
     - Step 2.4: Formulate the Physical Contradiction (PC) at the micro-level
     - Step 2.5: Intensify the PC — "X must be A to [function] and must be not-A to [avoid harm]"
   - **Part 3: Solution**
     - Step 3.1: Apply separation principles (time, space, condition, scale)
     - Step 3.2: Apply the 76 Standard Solutions
     - Step 3.3: Apply the 40 Inventive Principles
     - Step 3.4: Apply resource analysis — use what is already available
     - Step 3.5: Evaluate solution against IFR
   - **Parts 4-9 (depth=deep only):**
     - Part 4: Mobilize and apply substance-field resources
     - Part 5: Apply knowledge base (effects database)
     - Part 6: Change or reformulate the problem
     - Part 7: Verify the solution (no new contradictions?)
     - Part 8: Extract maximum value from the solution
     - Part 9: Generalize — can this solution pattern apply elsewhere?

4. Present the result with:
   - Mini-problem statement
   - Both Technical Contradictions (TC-1 and TC-2)
   - Physical Contradiction at the micro-level
   - IFR statement
   - Operative Zone and Time
   - Solution concept(s) with the separation principle or inventive principle used
   - Solution verification: does it resolve the PC without new contradictions?
   - If depth=deep: generalized solution pattern for knowledge reuse

5. Suggest next steps:
   - `/triz:resources` to find implementation resources
   - `/triz:evolution` to check alignment with evolution trends
   - `/triz:trimming` to simplify the resulting solution
