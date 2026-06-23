# 📚 AI Team System Documentation

> A system of AI-simulated professionals for collaborative development. Tool-agnostic (Claude Code, Codex, Cursor).

## 🚀 Quick Start

Agent instructions in [`AGENTS.md`](../AGENTS.md) (source of truth). Three invocation modes:

1. **Manual** — name the persona: _"Act as Finance: current spend?"_
2. **Auto-route** — without naming, the agent routes by domain.
3. **Handoff** — the persona chains to another: `→ Rafael (Backend): validate the architecture.`

## 👥 Personas

Each persona keeps its context in `ai/professionals/[name]/context.md` (+ `rules.md` when a short card exists). Full roster in [`AGENTS.md`](../AGENTS.md).

## 🔗 System Configuration

- **Source of truth** → [`AGENTS.md`](../AGENTS.md)
- **Claude Code** → [`CLAUDE.md`](../CLAUDE.md) (`@AGENTS.md`)
- **Cursor** → [`.cursor/rules/team.mdc`](../.cursor/rules/team.mdc)
- **Glossary** → [`glossary.md`](glossary.md)

## 🚀 Recommended Workflows

- **New feature**: Product → UX → UI → Backend → Frontend → review
- **Business decision**: Startup Advisor → Finance → Sales → Legal → consensus
- **Optimization**: Metrics → UX → UI → Frontend

## 💡 Tips

- **Be specific**: ❌ "How do we improve the app?" → ✅ "How do we reduce drop-off between signup and quick setup?"
- **Leverage handoff**: let the persona point to the next owner and follow the chain.
- **High risk** (financial/legal/strategy) always needs confirmation — see safe words in `AGENTS.md`.
