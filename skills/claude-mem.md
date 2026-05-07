# claude-mem

## Summary
Claude Code plugin for persistent memory across sessions. It captures tool-use observations, compresses them into semantic summaries, and injects relevant context back into future sessions.

## Aliases
- Claude-Mem
- claude mem
- persistent memory plugin
- memory plugin for Claude Code

## When to use
Use when you want Claude to remember project history, prior decisions, and relevant context across separate sessions.

## Official URL
https://docs.claude-mem.ai/

## Source / repo URL
https://github.com/thedotmack/claude-mem

## Trigger phrases
- remember this across sessions
- persistent memory
- save project context
- bring back prior context
- keep session history
- repair claude-mem

## Setup
- Verified: install via `npx claude-mem install` or the Claude Code marketplace commands.
- Verified: the GitHub README says `npm install -g claude-mem` only installs the SDK/library and does not register hooks.
- Verified: docs mention support for Claude Code, Cursor, Gemini CLI, Windsurf, OpenCode, Codex CLI, and OpenClaw.
- Verified: Node.js 20+, Bun, and uv are required or auto-installed by the installer.
- Inferred: the installer is the preferred path for normal users; source builds are mainly for development/testing.

## Usage notes
- Verified: it automatically captures tool usage, creates summaries, and re-injects relevant context into later sessions.
- Verified: the docs describe a web viewer UI at `http://localhost:37777`.
- Verified: search is layered/progressive to reduce token cost.
- Verified: a `repair` command exists for stale installs after plugin updates.

## Caveats
- Do not confuse the plugin install with `npm install -g claude-mem`; that alone does not enable memory hooks.
- Likely overkill if you only need a one-off note or small local reminder.

## Related
- Claude Code
- Cursor
- Gemini CLI
- OpenCode
- Codex CLI
- OpenClaw
