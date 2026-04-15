# research-writer

Claude Code plugin for researching and writing structured articles.

## Features

- 3 writing patterns: bullet notes, single-file articles, multi-chapter structured articles
- Parallel chapter writing via `chapter-writer` subagent
- Obsidian integration (default) or local filesystem output
- WebSearch-based research before writing

## Usage

```
/research-writer
```

## Components

- **skills/research-writer**: Main skill with 3 writing patterns
- **agents/chapter-writer**: Subagent for parallel chapter writing (Pattern 3)
