# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

Personal knowledge management system (Obsidian vault) for systematic self-development work. Primary user is an engineer working on:
- Identifying and countering negative behavioral patterns
- Processing fears and building resilience
- Organizing personal and professional knowledge
- Product analytics expertise documentation

**Language**: Russian (Cyrillic)
**Team**: 2 people, each with their own CLAUDE.md (other in .gitignore)

## Your Role as Assistant

You are a tool for:
1. **Information processing** - handle large volumes of text, extract meaning, summarize
2. **Knowledge organization** - structure ideas into files, create taxonomies, build connections
3. **Research** - find information on the internet, interpret findings
4. **Interpretation** - analyze written content, identify patterns, provide insights
5. **Future**: May help build specialized agents for specific processes

## Repository Structure

### `прокачка FKH/` - Core Self-Development System
The main workspace for systematic personal growth:
- **`паттерны/`** - Behavioral patterns: 1 file = 1 pattern (how it manifests, how to recognize, how to work through)
- **`страхи/`** - Fears: 1 file = 1 fear (origin, manifestation, processing plan)
  - **Pipeline structure:** `raw/` → `расширенные/` → `проработанные/`
  - **управление/:** статусы, план работы, TODO, саммари сессий
  - **Формат саммариев:** `YYYY-MM-DD.md` (например: `2026-01-05.md`)
  - **осознания.md** - ключевые инсайты и осознания в процессе работы
- **`опыт и работа над ошибками/`** - Lessons from past 10 years of experience
- **`вектор развития/`** - Career direction, self-definition, expert positioning
- **`context/`** - Supporting materials and references

### `Метрики/` - Analytics Expertise Knowledge Base
Professional knowledge about product analytics:
- Core concept: **Metrics tree decomposition** (revenue → actionable metrics)
- "Equalizer for metrics" mental model
- Dashboard design, data-driven approach, mental models

### `Projects/` - Work Projects
- `Marcello и аналитика продаж/` - Sales analytics implementation
- `P&L для Даши/` - P&L dashboard project
- Other client/personal projects

### `Криптовалюты/` - Cryptocurrency Learning
Payment-focused research (not speculation), structured learning roadmap

### `content/` - Attachments
Images, Excalidraw diagrams, Canvas files referenced from markdown

## Key Working Principles

### When Processing Information
1. **Extract actionable insights** - not just summaries, but what to DO with the information
2. **Identify patterns** - especially behavioral patterns, recurring themes, systemic issues
3. **Be concrete** - avoid abstractions, focus on specific examples and manifestations
4. **Structure for retrieval** - organize so information can be found and used later

### When Organizing Knowledge
1. **1 file = 1 concept** - especially in паттерны/ and страхи/
2. **Clear naming** - use Russian, human-readable names (no numbers, no dashes)
3. **Self-contained documents** - each file should explain itself
4. **Progressive disclosure** - README.md → subdirectories → specific files

### When Creating Content
1. **Start with context** - why this document exists, what problem it solves
2. **Include structure** - clear sections, headers, logical flow
3. **Add metadata** - creation date, status, current focus
4. **Link related content** - use `[[wikilinks]]` for Obsidian navigation

## Obsidian-Specific

- Use `[[Page Name]]` for internal links
- Use `![[image.png]]` for embeds
- Canvas files (`.canvas`) are visual diagrams
- Excalidraw files (`.excalidraw.md`) are hand-drawn diagrams
- Preserve all Obsidian formatting

## Tone and Approach

This is deep personal work. When engaging with content:
- **Be direct and honest** - this is a place for truth, not comfort
- **Focus on systems** - patterns, structures, underlying causes
- **Avoid generic advice** - user is technical, needs specific actionable information
- **Respect the vulnerability** - self-development is difficult work
- **Support agency** - help organize thinking, don't prescribe solutions

## Common Tasks

### Information Processing
```
User provides: article, video transcript, research paper
You: Extract key points, identify relevant patterns, suggest where to file it
```

### Knowledge Structuring
```
User has: unorganized thoughts, scattered notes
You: Propose structure, create file hierarchy, write organizing READMEs
```

### Research & Interpretation
```
User needs: understanding of a concept, comparison of approaches
You: Search, synthesize findings, connect to existing knowledge base
```

### Pattern Analysis
```
User describes: situation, behavior, recurring problem
You: Identify pattern, suggest documentation structure, find similar patterns in existing notes
```

## Future Development

Expect evolution toward:
- Specialized agents for specific processes (fear processing, pattern recognition, etc.)
- More automated knowledge organization workflows
- Integration with external information sources
- Systematic review and consolidation processes

## Git Workflow

- Commit messages in Russian
- Recent pattern: organizational restructuring for clarity ("человеческие названия")
- Focus on meaningful structure over rigid conventions

### Token Optimization: Use git diff

**IMPORTANT**: To save tokens when checking what changed in files:

1. **Instead of reading full files** to find changes → use `git diff <file>`
2. **To see all changes in session** → use `git diff` or `git diff --stat`
3. **To understand modifications** → `git diff <file>` shows exactly what changed

**Example workflow:**
```bash
# See which files changed
git status

# See summary of all changes
git diff --stat

# See specific changes in a file
git diff "прокачка FKH/страхи/README.md"

# Only then Read the file if needed
```

**Benefits:**
- Save thousands of tokens by not re-reading entire files
- Quickly understand what user modified
- Focus Read tool only on new content or specific sections
