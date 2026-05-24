# Interview to Obsidian

A Claude Code skill that extracts interview questions from screenshots/photos, categorizes them by topic, and organizes them into structured Obsidian notes.

## What it does

1. **Reads images** — Extracts interview questions and answers from uploaded screenshots or photos
2. **Smart categorization** — Automatically classifies questions into topics like Agent, MCP, RAG, LLM Basics, Machine Learning, etc.
3. **Writes to Obsidian** — Creates organized markdown files in your Obsidian vault under `面试题/` folder
4. **Append-friendly** — If a category file already exists, appends new questions without overwriting

## Usage

Upload interview question screenshots and say something like:

- "帮我把这些面试题整理到 obsidian 中"
- "这些面试题归个类"
- "帮我把这些面试题记下来"
- `/interview-to-obsidian`

## Output format

Each category gets its own file (e.g., `面试题/Agent.md`, `面试题/RAG.md`) with:

```markdown
---
tags:
  - 面试题
  - Agent
date: 2026-05-24
---

# Agent 面试题

## 你们用的 Agent 框架是什么？ReAct 还是 Plan-and-Execute？

答案内容...
```

## Installation

```bash
claude install-skill /path/to/interview-to-obsidian
```

Or manually copy the `interview-to-obsidian/` folder to `~/.claude/skills/`.

## Configuration

Edit the vault path in `SKILL.md` to match your Obsidian vault location:

```
Obsidian vault 路径：`/path/to/your/Obsidian Vault/`
```

## Requirements

- Claude Code with image reading capability
- An Obsidian vault on your local filesystem

## License

MIT
