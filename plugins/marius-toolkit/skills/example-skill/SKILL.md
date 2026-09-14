---
description: Example placeholder skill. Replace or delete once you add your own skills.
---

This is a placeholder skill to confirm the plugin structure works end to end.

Once you have a real skill to add:
1. Create a new folder under `skills/<skill-name>/`
2. Add a `SKILL.md` file with YAML frontmatter (a `description` field) and the skill's instructions
3. Bump the `version` field in `plugins/marius-toolkit/.claude-plugin/plugin.json`
4. Commit and push
5. Run `/plugin marketplace update marius-claude-skills` (Claude Code) or refresh the marketplace in Claude Desktop to pick up the change
