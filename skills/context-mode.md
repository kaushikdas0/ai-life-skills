# context-mode

## Summary
MCP server / plugin for AI coding agents that keeps large tool output out of the conversation, compresses assistant output, and restores session state across compaction.

## Aliases
- Context Mode
- Claude Context Mode (inferred from branding and repo naming)

## When to use
Use for large logs, JSON dumps, many-file analysis, long coding sessions, and any workflow where context fills up too fast.

## Official URL
https://context-mode.com/

## Source / repo URL
https://github.com/mksglu/context-mode

## Trigger phrases
- context window
- large output
- too much log data
- analyze many files
- use ctx_execute
- keep this out of context
- restore session state

## Setup
- Verified: the site and GitHub README describe a Claude Code plugin install, plus a global `npm install -g context-mode` path.
- Verified: the docs also mention MCP-only install for trying it without hooks.
- Inferred: the exact install path depends on the host platform, so use the platform-specific docs for the right hook/routing setup.

## Usage notes
- Verified: it routes big tool calls into sandboxed subprocesses so raw output stays out of chat.
- Verified: it stores session events in a local SQLite-backed knowledge base with FTS5/BM25 search.
- Verified: it pushes the agent toward “think in code” by generating scripts instead of pulling raw data into context.
- Verified: it compresses assistant output by stripping filler while keeping technical meaning.

## Caveats
- Marketing numbers vary a bit across the site, GitHub README, and npm metadata; verify the current docs before depending on a specific claim or install command.
- Best fit is agentic coding work, not general-purpose prompting.

## Related
- Claude Code
- Cursor
- Gemini CLI
- Codex CLI
- MCP
