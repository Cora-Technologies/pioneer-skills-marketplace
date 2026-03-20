# Contributing to the Pioneer Skills Marketplace

Thanks for building something useful! This guide walks you through creating, testing, and submitting a skill or plugin.

---

## The Short Version

1. Copy the [skill template](./templates/skill-template/) and fill it in
2. Test it by installing it locally in Cowork
3. Open a pull request — someone will review and merge it
4. It gets packaged and added to the catalog automatically (or you can package it yourself)

---

## Step 1 — Create Your Skill

### Option A: Let Claude help you (recommended)

Open Cowork and say something like:

> "I want to create a skill that helps me [describe what it does]. Can you help me build it?"

Claude will walk you through the whole process, generate the skill file, and let you test it before you submit.

### Option B: Use the template manually

Copy the template folder and fill in the blanks:

```bash
cp -r templates/skill-template skills/my-plugin-name/my-skill-name
```

Then edit `SKILL.md` — the file has comments explaining each section.

---

## Step 2 — Skill Writing Tips

A good skill has three things:

**A clear description** — This is what Claude reads to decide when to use your skill. Be specific about the situations it helps with. Example:

> "Draft a weekly status update for a project. Use when someone says 'write a status update', 'weekly update', or 'project summary for stakeholders'."

**Clear instructions** — Write in the imperative ("Ask the user for X", "Format the output as Y"). Explain *why* things matter, not just *what* to do.

**The right scope** — One skill should do one thing well. If you find yourself writing "and also...", consider splitting into two skills.

### File size guidelines

| File | Max size |
|------|----------|
| `SKILL.md` | ~500 lines / ~3,000 words |
| Reference files in `references/` | No hard limit, but add a table of contents if >300 lines |

If your skill needs a lot of reference material (e.g., a style guide, a data schema), put it in `references/` and have `SKILL.md` point to it.

---

## Step 3 — Add It to a Plugin

Skills live inside plugins. You have two options:

**Add to an existing plugin** — If your skill fits naturally in an existing plugin (e.g., a new productivity skill could go in `pioneer-core`), add it to that plugin's skills folder under `skills/plugin-name/`.

**Create a new plugin** — If your skill is the start of something new, copy the plugin template:

```bash
cp -r templates/plugin-template skills/my-new-plugin
```

Fill in `.claude-plugin/plugin.json` with your plugin's name, version, and description.

---

## Step 4 — Test Locally

1. Package your plugin into a `.plugin` file:
   ```bash
   cd skills/my-plugin-name
   zip -r /tmp/my-plugin-name.plugin . -x "*.DS_Store"
   ```
2. Install it in Cowork: **Settings → Plugins → Install from file**
3. Try a few prompts that should trigger your skill — does it work as expected?
4. Try a few prompts that *shouldn't* trigger it — does it stay quiet?

---

## Step 5 — Submit a Pull Request

Open a PR with:

- [ ] Your skill source files in `skills/<plugin-name>/<skill-name>/`
- [ ] Updated `catalog.json` if you're adding a new plugin (see format below)
- [ ] A short description of what the skill does and what prompted you to build it
- [ ] (Optional) The packaged `.plugin` file in `plugins/` — a maintainer can do this for you if you prefer

### PR checklist

- [ ] `SKILL.md` has a `name` and `description` in the frontmatter
- [ ] Description includes specific trigger phrases
- [ ] Skill has been tested locally in Cowork
- [ ] No hardcoded personal names, API keys, or internal URLs (use placeholders like `[TEAM_NAME]`)
- [ ] Skill does one focused thing

---

## Updating `catalog.json`

If you're adding a new plugin, add an entry to `catalog.json`:

```json
{
  "name": "my-plugin-name",
  "version": "0.1.0",
  "description": "One sentence describing what this plugin does.",
  "author": "Your Name",
  "skills": ["skill-one", "skill-two"],
  "file": "plugins/my-plugin-name.plugin",
  "updated": "2026-03-20"
}
```

---

## Packaging (for maintainers)

When a PR is approved, a maintainer packages the plugin and adds the `.plugin` file to `plugins/`:

```bash
cd skills/plugin-name
zip -r ../../plugins/plugin-name.plugin . -x "*.DS_Store"
```

Then update `catalog.json` with the new version and date.

---

*Something unclear? Open an issue or ping Ryan.*
