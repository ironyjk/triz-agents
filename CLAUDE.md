# triz-agents

TRIZ — the complete Altshuller framework as Claude Code skills. No external dependencies.

## Commands

### Problem Analysis

| Command | Tool | Purpose |
|---------|------|---------|
| `/triz "problem"` | Full Workflow | IFR → Contradiction → Principles → Resources → Evolution |
| `/triz:ifr "problem"` | Ideal Final Result | Define the perfect solution |
| `/triz:contradiction "problem"` | Contradiction Analysis | Find technical and physical contradictions |

### Solution Generation

| Command | Tool | Purpose |
|---------|------|---------|
| `/triz:matrix "parameters"` | Contradiction Matrix | Map parameters to inventive principles |
| `/triz:40p "contradiction"` | 40 Principles | Apply inventive principles |
| `/triz:sufield "system"` | Su-Field Analysis | Model substance-field interactions |
| `/triz:resources "situation"` | Resource Analysis | Find hidden resources |

### System Design

| Command | Tool | Purpose |
|---------|------|---------|
| `/triz:trimming "system"` | Trimming | Remove components, keep functions |
| `/triz:evolution "technology"` | Evolution Laws | Predict next-generation designs |
| `/triz:ariz "complex problem"` | ARIZ Algorithm | Full structured problem-solving |

## Rules

- Output diagrams in Mermaid by default, ASCII with `--format ascii`
- Always formulate contradictions explicitly before solving
- IFR first — establish the ideal before compromising
- Never present a "compromise" as a TRIZ solution — TRIZ eliminates contradictions
- Each sub-skill is standalone — can be invoked independently
- No external dependencies — pure Claude Code skills
