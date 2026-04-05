---
name: skill-creator
version: 1.0.0
description: "Create and register new skills for this agent."
allowed-tools:
  - Bash
  - Read
  - Write
  - Edit
user-invocable: true
---

# Skill Creator

Create new SKILL.md skill files and register them in the agent's skill directory.

## How to Create a Skill

1. Define the skill's purpose and capabilities
2. Write the SKILL.md with proper YAML frontmatter (name, version, description, allowed-tools, user-invocable)
3. Save to ~/.openclaw/workspace/skills/<skill-id>/SKILL.md
4. The skill is immediately available for use

## SKILL.md Format

\`\`\`yaml
---
name: <kebab-case-skill-id>
version: 1.0.0
description: "<what this skill does>"
allowed-tools:
  - Bash
  - Read
  - Write
  - Edit
  - WebFetch
user-invocable: true
---
\`\`\`

## Guidelines

- Skills should be atomic — one skill, one responsibility
- Include a clear description so the agent knows when to invoke it
- List only the tools the skill actually needs in allowed-tools
- Add a Usage section explaining when and how to invoke the skill
- Add an Implementation section with step-by-step instructions
