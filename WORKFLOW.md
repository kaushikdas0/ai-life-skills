# Channel Workflow

> This document defines how the **#maintainer** Discord channel operates for this repo.

## Purpose

This channel is the single intake point for anything AI-skill-related that Kaushik finds worth cataloging: tools, CLIs, scripts, skills, frameworks, libraries — anything in the AI skill space.

## How it works

1. **Kaushik sends a message** in the channel — could be a URL, a name + description, a paste, a screenshot, or any combination.
2. **Idly 🍚 (the bot) receives it** and does the following automatically:
   - Researches the item (visit URL, search, extract details)
   - Determines the right category: **Featured**, **Design darlings**, **Tech toys**, or **Odd little extras**
   - Creates a skill note file in `skills/` using `skills/_template.md` as the base
   - Updates the relevant category table in `README.md`
   - Commits and pushes to `main`
3. **If info is missing** (e.g., no clear name or URL), Idly asks one short question before proceeding.
4. **If the item already exists** in the catalog, Idly updates the existing entry instead of duplicating.

## Categories

| Category | Use when |
|---|---|
| **✨ Featured** | Standout tools that deserve top billing — best-in-class or game-changing |
| **🎨 Design darlings** | UI/UX, styling, design systems, visual tools |
| **🛠️ Tech toys** | Dev tools, CLIs, frameworks, infra, productivity, coding aids |
| **🧩 Odd little extras** | Niche, weird, experimental, or hard-to-classify stuff |

## Conventions

- Skill note files: lowercase hyphenated, matching the catalog slug
- One file per entry, template from `skills/_template.md`
- Keep README table rows short; details go in the note file
- Commit messages: `[catalog] add <name>` or `[catalog] update <name>`
- Push to `main` after every intake (no PRs needed for catalog updates)

## Future scope

This channel may be extended to manage additional repos. The workflow will adapt as needed.
