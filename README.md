# marius-claude-skills

Central, versioned home for Marius's custom Claude skills, packaged as a Claude Code / Claude Desktop plugin marketplace.

## Why this exists

Claude Code and Claude Desktop each keep their own local skill storage. This repo is the single source of truth: skills are written here once, versioned with git, and installed into both surfaces as a plugin from this marketplace.

## Structure

```
.claude-plugin/marketplace.json      <- marketplace manifest (lists the plugin(s) below)
plugins/marius-toolkit/
  .claude-plugin/plugin.json         <- plugin manifest (name, version, author)
  skills/<skill-name>/SKILL.md       <- one folder per skill
```

## Add or update a skill

1. Add/edit a folder under `plugins/marius-toolkit/skills/`.
2. Bump `version` in `plugins/marius-toolkit/.claude-plugin/plugin.json`.
3. Commit and push to `main`.
4. Refresh wherever it's installed (see below) to pick up the change.

## Install / update in Claude Code

```
/plugin marketplace add mariuskroh/claude-skills-marketplace
/plugin install marius-toolkit@marius-claude-skills
```

To pick up a later update:

```
/plugin marketplace update marius-claude-skills
```

## Install / update in Claude Desktop

Open the plugin browser (Settings > Plugins, or the in-app plugin manager) and add the marketplace by repo:
`mariuskroh/claude-skills-marketplace`, then install `marius-toolkit` from it. Refresh the marketplace there the same way when you push updates.
