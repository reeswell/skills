# Reeswell Skills

Agent-ready coding conventions for JavaScript and TypeScript projects.

This repository packages the same Reeswell engineering preferences for Cursor,
Codex, Claude, and portable Agent Skills.

## Included

- `skills/reeswell/SKILL.md`: portable skill for Codex and Claude-compatible agents.
- `skills/reeswell/agents/openai.yaml`: UI metadata for skill-capable OpenAI surfaces.
- `.cursor/rules/reeswell.mdc`: Cursor rule, enabled by default.
- `.claude-plugin/plugin.json`: Claude plugin manifest for this skill package.
- `AGENTS.md`: Codex project instructions.
- `CLAUDE.md`: Claude Code project instructions.
- `CODEX.md`: short Codex-specific usage note.
- `CURSOR.md`: short Cursor-specific usage note.

## Install

### Codex

Install the skill manually:

```bash
mkdir -p ~/.codex/skills
cp -R skills/reeswell ~/.codex/skills/reeswell
```

Or use this repository directly in a project by copying `AGENTS.md` into that
project root.

### Claude

Use the portable skill by copying it into your Claude skills directory:

```bash
mkdir -p ~/.claude/skills
cp -R skills/reeswell ~/.claude/skills/reeswell
```

For Claude Code project instructions, copy `CLAUDE.md` into the project root.
This repository also includes `.claude-plugin/plugin.json` so the skill can be
packaged as a Claude plugin by clients that support plugin manifests.

### Cursor

From the target project, copy the Cursor rule from this repository:

```bash
REESWELL_SKILLS=/path/to/reeswell-skills
mkdir -p .cursor/rules
cp "$REESWELL_SKILLS/.cursor/rules/reeswell.mdc" .cursor/rules/reeswell.mdc
```

## Use

Ask the agent to use the Reeswell skill when writing, reviewing, or refactoring
JavaScript and TypeScript code.

Example:

```text
Use $reeswell to review this TypeScript module and suggest focused improvements.
```

## Maintain

Keep these files semantically aligned when changing conventions:

- `skills/reeswell/SKILL.md`
- `.cursor/rules/reeswell.mdc`
- `AGENTS.md`
- `CLAUDE.md`

The skill should stay concise. Put detailed project-specific guidance in the
target project's own instructions instead of expanding this general-purpose
skill.

## License

MIT
