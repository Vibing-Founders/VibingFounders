# Contributing a Plugin

This document explains how to add a new plugin to the founder-kit marketplace.

## Plugin directory structure

Every plugin lives under `plugins/<plugin-name>/` and must contain:

```
plugins/
  <plugin-name>/
    .claude-plugin/
      plugin.json       # Required metadata
    skills/
      SKILL.md          # At least one skill
      ...               # Additional skills and knowledge files
```

## Required `plugin.json` fields

```json
{
  "name": "your-plugin-name",
  "version": "1.0.0",
  "description": "One sentence describing what the plugin does and who it is for.",
  "author": {
    "name": "Your Name or Org",
    "url": "https://github.com/your-handle"
  },
  "homepage": "https://github.com/Vibing-Founders/founder-kit",
  "repository": "https://github.com/Vibing-Founders/founder-kit",
  "license": "MIT",
  "keywords": ["relevant", "keywords"],
  "skills": ["./skills/"]
}
```

All fields are required. `keywords` should be an array of lowercase strings.

## Skill structure

Each skill is a `SKILL.md` file with YAML frontmatter followed by the skill body:

```markdown
---
name: my-skill
description: >
  Triggers when user asks about X, Y, or Z.
  Use this skill to help with ...
---

# My Skill

[Skill instructions here]
```

The `description` field is used by Claude to decide whether to invoke the skill — make it specific and include example trigger phrases.

## Adding knowledge files

Knowledge files live alongside or under the skill that uses them. For knowledge shared across multiple skills, place it under `skills/_shared/`.

```
skills/
  _shared/
    legislation/        # Acts and regulations used by multiple skills
    jurisdiction-map.md # Which rules apply where
  my-skill/
    SKILL.md
    knowledge/          # Knowledge specific to this skill
```

## Registering your plugin

After adding your plugin:

1. Add a row to the plugins table in [README.md](./README.md)
2. Add a "Plugin Details" section describing the skills and example usage

## PR checklist

- [ ] `plugins/<name>/.claude-plugin/plugin.json` exists with all required fields
- [ ] At least one `SKILL.md` with valid frontmatter (`name`, `description`)
- [ ] Plugin added to README.md plugins table
- [ ] Plugin details section added to README.md
- [ ] All legislation files cite official sources
- [ ] No personally identifiable information in any committed file
