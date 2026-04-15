# research-plugin

Claude Code plugin for researching and writing structured articles.

## Features

- 3 writing patterns: bullet notes, single-file articles (~5000 words), multi-chapter structured articles
- Parallel chapter writing via `chapter-writer` subagent (Pattern 3)
- Obsidian integration (default) or local filesystem output
- Obsidian CLI support (`obsidian create`, `obsidian search`, `obsidian tags`)
- WebSearch-based research before writing
- Zotero / KAKEN / Context7 for supplementary research
- User approval of outlines before writing begins
- Written in Japanese (technical terms in English)

## Usage

```
/survey
```

You will be prompted to choose a pattern and output destination.

## Writing Patterns

| Pattern | Description | Agent |
|---|---|---|
| 1. Bullet notes | Concise bullet-point notes | Single agent |
| 2. Single-file article | ~5000-word article in one file | Single agent |
| 3. Structured article | Multi-chapter article with table of contents | Main + chapter-writer subagents in parallel |

## Components

- **skills/survey**: Main skill with 3 writing patterns
- **agents/chapter-writer**: Subagent for parallel chapter writing (Pattern 3, runs on Sonnet)

## File Layout (Pattern 3)

```
{Title}/
  {Title}.md              # Table of contents
  {Title} - 第1章.md      # Chapter 1
  {Title} - 第2章.md      # Chapter 2
  ...
```

Patterns 1 & 2 output a single file: `{Title}/{Title}.md`
