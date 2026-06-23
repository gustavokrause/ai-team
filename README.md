# 🤖 AI Team

> A team of AI-simulated professionals to build and validate products collaboratively. Tool-agnostic: Claude Code, Codex, Cursor.

## 📋 Overview

A system of **AI-simulated professionals**, each with its own memory, context, and responsibilities. You consult the right persona for each decision — from strategy to implementation.

Every persona works at **Staff/Principal level** and is **context-first**: it reads your situation (business model, stage, stack, jurisdiction, constraints) and adapts, instead of assuming. No baked-in point of view — Finance won't assume you're raising, Marketing won't assume SEO, Frontend won't assume React. Need deep niche work? Add a **specialist persona** that pairs with the generalist via handoff.

Contains **only the AI team configuration** (contexts, rules, routing). It's product- and tool-agnostic: point it at any project.

## 🔌 How each tool loads it

| Tool | Entrypoint | Mechanism |
| --- | --- | --- |
| **Claude Code** | `CLAUDE.md` | imports `@AGENTS.md` |
| **Codex** | `AGENTS.md` | native read |
| **Cursor** | `.cursor/rules/team.mdc` | points to `AGENTS.md` |

`AGENTS.md` is the **source of truth**. The others just point to it — no duplication, no drift.

## 👥 The Team

```
├── 🚀 STRATEGY
│   └── Augusto (Principal Strategic Advisor)
│
├── 🧠 AI/ORCHESTRATION
│   └── Caio (AI Solutions Architect & Orchestration)
│
├── 🏢 BUSINESS
│   ├── Maria (Product)        ├── Carla (Marketing)
│   ├── Roberto (Sales)        └── Diego (Metrics)
│   └── Fernanda (Finance)
│
├── 🎨 DESIGN
│   ├── Helena (UX)   ├── Mariana (UI)   └── Julia (Copywriting)
│
├── 💻 TECH
│   ├── Ana (Frontend)   ├── Rafael (Backend)   └── Lucas (DevOps)
│
└── ⚖️ COMPLIANCE
    └── Patrícia (Legal)
```

## 🔀 How to invoke a persona

Three modes (details in [`AGENTS.md`](AGENTS.md)):

1. **Manual** — you name it: _"Act as Product: what's the next priority?"_ or _"Rafael, what architecture should we use?"_
2. **Auto-route** — without naming, the agent picks the persona by the question's domain.
3. **Handoff** — the persona closes with a note that triggers the next one: `→ Helena (UX): validate this flow.` — closing the loop.

## 🗂️ Structure

```
.
├── AGENTS.md                 # source of truth (roster, invocation, rules)
├── CLAUDE.md                 # @AGENTS.md (Claude Code)
├── .cursor/rules/team.mdc    # pointer (Cursor)
├── ai/
│   ├── README.md
│   └── professionals/[name]/
│       ├── context.md        # persona's deep context
│       └── rules.md          # short card (when present)
└── docs/
    ├── README.md
    └── glossary.md
```

## 📚 Documentation

- Agent instructions and routing → [`AGENTS.md`](AGENTS.md)
- Workflow and usage tips → [`docs/README.md`](docs/README.md)
- Each persona → `ai/professionals/[name]/`
