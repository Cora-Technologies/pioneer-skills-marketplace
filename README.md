# Pioneer Skills Marketplace

A shared library of Claude skills and plugins built by and for the Pioneer team. Browse below to find something useful, or [contribute your own](#contributing).

---

## How to Install a Plugin

1. Download the `.plugin` file from the [`plugins/`](./plugins/) folder
2. In the Cowork desktop app, go to **Settings → Plugins → Install from file**
3. Select the downloaded file — Claude will have the new skills immediately

---

## Plugin Catalog

| Plugin | Description | Skills Included | Maintained By |
|--------|-------------|-----------------|---------------|
| [pioneer-core](./plugins/pioneer-core.plugin) | Essential Pioneer workflows every employee needs | Meeting notes, weekly digest, status updates | @ryan |
| *(more coming soon)* | | | |

> **Looking for something specific?** Check [`catalog.json`](./catalog.json) for a machine-readable list, or open an issue using the [skill request template](./.github/ISSUE_TEMPLATE/skill-request.md).

---

## Skills by Category

Skills are the building blocks inside plugins. Browse by category:

### Productivity
- `weekly-digest` — Summarize what happened across your tools this week
- `meeting-notes` — Capture and structure notes from a meeting

### Communication
- `status-update` — Draft a crisp project status update for stakeholders

### *(Add your category here)*

---

## Contributing

Want to share a skill you've built? Great — here's the short version:

1. **Build your skill** — use the [skill template](./templates/skill-template/) as a starting point, or ask Claude to help you create one from scratch in Cowork
2. **Add it to a plugin** — either add it to an existing plugin or create a new one using the [plugin template](./templates/plugin-template/)
3. **Submit a pull request** — open a PR with your changes; see [CONTRIBUTING.md](./CONTRIBUTING.md) for the full checklist

---

## Repo Structure

```
pioneer-skills-marketplace/
├── plugins/                  ← Packaged .plugin files (ready to install)
├── skills/                   ← Skill source files, organized by plugin
│   └── plugin-name/
│       └── skill-name/
│           └── SKILL.md
├── templates/
│   ├── skill-template/       ← Copy this to start a new skill
│   └── plugin-template/      ← Copy this to start a new plugin
├── catalog.json              ← Machine-readable plugin registry
├── CONTRIBUTING.md           ← How to build and submit skills
└── README.md                 ← You are here
```

---

*Questions? Ping Ryan in Slack or open an issue.*
