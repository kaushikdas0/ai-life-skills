# here-now

## Summary
here.now is instant web hosting and file storage for agents. It publishes static sites and files to live URLs and can also store private files in here.now Drive.

## Aliases
- here.now
- heredotnow

## When to use
- Publishing websites, prototypes, docs, dashboards, tools, visualizations, and static assets
- Giving agent-generated work a shareable URL quickly
- Storing private agent files in cloud Drive

## Official URL
https://here.now/

## Source / repo URL
https://github.com/heredotnow/skill

## Trigger phrases
- publish this site
- host this for me
- give me a live URL
- upload this folder to the web
- store this privately in Drive

## Setup
- Install with: `npx skills add heredotnow/skill --skill here-now -g`
- Fallback: `curl -fsSL https://here.now/install.sh | bash`
- Anonymous sites work without an account but expire after 24 hours
- For permanent sites, register and use an API key

## Usage notes
- Works with files or folders, especially static HTML/CSS/JS content
- Sites can be published at random `.here.now` URLs or custom domains
- Anonymous publishes return a claim URL/token; save it immediately
- Supports password protection and paid access for authenticated sites
- Drive storage is for private agent files, separate from public Sites

## Caveats
- Best suited to static hosting, not a full app server
- Anonymous site claim tokens are returned only once
- Public by default, so avoid sensitive content unless protected
- Password protection and payment gating are mutually exclusive

## Related
- OpenClaw agents that need a URL for generated work
- Static site generators
- File upload / artifact publishing workflows
