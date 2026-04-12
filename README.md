# OneDayBI Marketplace

A Claude Code plugin marketplace by [Mihaly Kavasi](https://github.com/KavasiMihaly) — AI-powered tools for data engineering, analytics, and Power BI workflows.

---

## Available Plugins

| Plugin | Description | Repo |
|--------|-------------|------|
| **dbt-pipeline-toolkit** | End-to-end dbt pipeline automation for SQL Server. CSV to star schema with agents, skills, MCP server, and validation hooks. | [DBT-Pipeline-Plugin](https://github.com/KavasiMihaly/DBT-Pipeline-Plugin) |

More plugins coming soon.

---

## Installation

### 1. Add the marketplace

Run this once in Claude Code:

```
/plugin marketplace add KavasiMihaly/AI-plugins
```

### 2. Browse and install plugins

```
/plugin
```

Select any plugin from the **OneDayBI-Marketplace** in the picker, or install by name:

```
/plugin install dbt-pipeline-toolkit@OneDayBI-Marketplace
```

### 3. Reload

```
/reload-plugins
```

If MCP tools don't appear, fully restart Claude Code.

---

## Adding a New Plugin to This Marketplace

1. Create your plugin repo with a `.claude-plugin/plugin.json` manifest
2. Add an entry to `.claude-plugin/marketplace.json` in this repo:

```json
{
  "name": "your-plugin-name",
  "description": "What it does in one sentence.",
  "source": {
    "source": "url",
    "url": "https://github.com/KavasiMihaly/Your-Plugin-Repo.git"
  },
  "category": "development",
  "homepage": "https://github.com/KavasiMihaly/Your-Plugin-Repo"
}
```

3. Commit and push — users who already added this marketplace will see the new plugin on next `/plugin` or `/reload-plugins`

---

## Marketplace Structure

```
AI-plugins/
├── .claude-plugin/
│   └── marketplace.json     # lists all plugins (external references)
├── .gitignore
└── README.md
```

Each plugin lives in its own repo, versioned and maintained independently. This repo is just the index.

---

## Author

**Mihaly Kavasi** — [@KavasiMihaly](https://github.com/KavasiMihaly) | [OneDayBI](https://www.onedaybi.com)
