# Inventory Reconciler — an Agent Skill by The Ask Why Company

Compare two independently maintained inventories and produce a conservative, evidence-backed candidate ledger for human review.

**When it's used:** use when matching records across a frozen research dataset and a separate read-only catalog, finding likely duplicates, surfacing conflicts, or listing unmatched coverage leads.

Read the skill: [skills/inventory-reconciler/SKILL.md](skills/inventory-reconciler/SKILL.md)

Works with any AI agent that reads the open [Agent Skills](https://agentskills.io) `SKILL.md` format.

## Install in Claude

**Claude Code:** `/plugin marketplace add theaskwhy/inventory-reconciler` then `/plugin install inventory-reconciler@inventory-reconciler`. Replace the placeholder with the Git host path where you obtained this package.

**Manual:** copy `skills/inventory-reconciler/` into `~/.claude/skills/` or `.claude/skills/`.

**Claude.ai:** zip the `skills/inventory-reconciler` folder and upload it under Settings → Capabilities → Skills.

## Use it with any AI agent

This skill uses the open **Agent Skills** standard (`SKILL.md`) and works with Claude Code, OpenAI Codex, Cursor, Gemini CLI, GitHub Copilot, Windsurf, Antigravity, OpenCode, Goose and other compatible agents.

**Quickest:** `npx skills add theaskwhy/inventory-reconciler`

**Manual:** copy `skills/inventory-reconciler/` into your tool's skills folder, such as `~/.codex/skills/`, `.agents/skills/`, `~/.cursor/skills/`, `.github/skills/`, or `.claude/skills/`. Tools without skill support can use `SKILL.md` in their instruction file.

## Licence

MIT © The Ask Why Company LLC. A credit is appreciated if you use or adapt this skill.
