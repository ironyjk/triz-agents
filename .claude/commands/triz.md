---
name: triz
description: "TRIZ — Systematic Innovation and Inventive Problem Solving toolkit"
argument-hint: "[Problem: <text>] [--tool contradiction|40p|matrix|sufield|ifr|trimming|evolution|ariz|resources] [--format mermaid|ascii] [--depth shallow|deep]"
---

EXECUTE IMMEDIATELY — do not deliberate, do not ask clarifying questions before reading the protocol.

## Argument Parsing (do this FIRST)

Extract from $ARGUMENTS:

- **Problem**: The system, situation, or inventive challenge to analyze. The entire argument text IS the problem if not explicitly labeled.
- **Tool**: Optional. Routes to a specific sub-tool: `contradiction`, `40p`, `matrix`, `sufield`, `ifr`, `trimming`, `evolution`, `ariz`, `resources`. Set by `--tool`.
- **Format**: `mermaid` (default) or `ascii`. Set by `--format`.
- **Depth**: `shallow` (default) or `deep`. Set by `--depth`.

## Routing

### Single Tool Mode (--tool specified)

If `--tool` is specified, route to the corresponding sub-skill:

| --tool | Invoke |
|--------|--------|
| `contradiction` | Read `.claude/skills/triz/references/contradiction-protocol.md` and execute |
| `40p` | Read `.claude/skills/triz/references/40p-protocol.md` and execute |
| `matrix` | Read `.claude/skills/triz/references/matrix-protocol.md` and execute |
| `sufield` | Read `.claude/skills/triz/references/sufield-protocol.md` and execute |
| `ifr` | Read `.claude/skills/triz/references/ifr-protocol.md` and execute |
| `trimming` | Read `.claude/skills/triz/references/trimming-protocol.md` and execute |
| `evolution` | Read `.claude/skills/triz/references/evolution-protocol.md` and execute |
| `ariz` | Read `.claude/skills/triz/references/ariz-protocol.md` and execute |
| `resources` | Read `.claude/skills/triz/references/resources-protocol.md` and execute |

Always also read `.claude/skills/triz/references/output-format.md` for rendering.

### Full Workflow Mode (no --tool)

If no `--tool` is specified, run the full ARIZ-based workflow.

Read the orchestration protocol:
```
.claude/skills/triz/references/full-workflow.md
```

Read the output format:
```
.claude/skills/triz/references/output-format.md
```

### Missing Problem

If Problem is missing or too vague, use AskUserQuestion:

```
header: "Problem"
question: "Describe the inventive problem, system, or challenge you want to solve. What are you trying to improve? What gets worse when you try? Be as specific as possible about the system and its constraints."
```

After receiving the answer, determine whether to suggest a specific tool or run the full workflow:

| Signal in user's response | Suggested tool |
|--------------------------|----------------|
| "improve X without worsening Y", "tradeoff", "can't have both" | `/triz:contradiction` |
| "how to solve", "inventive principle", "creative solution" | `/triz:40p` |
| "which principle", "parameter conflict", "improving vs worsening" | `/triz:matrix` |
| "interaction", "substance", "field", "harmful effect", "insufficient action" | `/triz:sufield` |
| "ideal", "perfect", "ultimate goal", "zero cost", "self-X" | `/triz:ifr` |
| "simplify", "remove component", "reduce cost", "eliminate part" | `/triz:trimming` |
| "trend", "next generation", "evolution", "future version" | `/triz:evolution` |
| "step by step algorithm", "complex problem", "stuck", "intractable" | `/triz:ariz` |
| "hidden resource", "what can we use", "free resource", "leverage what exists" | `/triz:resources` |
| Complex/unclear — multiple aspects | Full ARIZ workflow (IFR→Contradiction→Resources→Principles→Solution) |
