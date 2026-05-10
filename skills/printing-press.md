# printing-press

## Summary
Printing Press is an agent-native CLI factory and library. It can generate Go CLIs, Claude Code skills, and MCP servers from an API or website, with a focus on token-efficient workflows for agents.

## Aliases
- printing press
- cli-printing-press

## When to use
- Building a custom CLI for an API or website
- Finding or reusing community-built CLIs
- Creating an agent-friendly workflow around a service
- Generating a matching skill and MCP server alongside the CLI

## Official URL
https://printingpress.dev/

## Source / repo URL
https://github.com/mvanhorn/cli-printing-press

## Trigger phrases
- build me a CLI for this API
- print a CLI for this site
- make an agent-native CLI
- generate a skill and MCP server
- find the best CLI for this service

## Setup
- Requires Go 1.26.3+ and Claude Code
- Install binary: `go install github.com/mvanhorn/cli-printing-press/v4/cmd/printing-press@latest`
- Verify with: `printing-press --version`
- Recommended repo clone: `git clone https://github.com/mvanhorn/cli-printing-press.git`
- Skills-only install: `gh skill install mvanhorn/cli-printing-press --agent claude-code --scope user`
- Alternate skills install: `npx skills add mvanhorn/cli-printing-press/skills -g -a claude-code -y`

## Usage notes
- The primary interface is the Claude Code command `/printing-press <app>`
- It can work from an API spec, a website, or sniffed traffic
- Typical output includes a Go CLI, research docs, verification proofs, and a quality score
- It also supports reprinting and polishing existing CLIs
- Some installs can load the repo directly with `claude --plugin-dir .`

## Caveats
- Best supported with Claude Code; other harnesses may work but are not the primary target
- A binary alone is not the full workflow; the matching skills matter too
- Best suited to API/website automation and agent workflows, not general-purpose app hosting

## Related
- here-now
- OpenClaw agent tooling
- MCP servers
- Claude Code skills
