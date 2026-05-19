# agent-browser

## Summary

Browser automation CLI for AI agents from Vercel Labs. It is a fast native Rust CLI that drives Chrome/Chromium over CDP, exposes compact accessibility-tree snapshots with `@eN` element refs, and includes built-in agent skills for browser workflows, Electron apps, Slack, dogfooding/QA, Vercel Sandbox, and AWS Bedrock AgentCore cloud browsers.

## Aliases

- Vercel agent-browser
- agent browser
- browser automation CLI for AI agents

## When to use

- Navigating websites, clicking buttons, filling forms, uploading files, taking screenshots, or saving PDFs
- Extracting page text/data with low context usage via accessibility snapshots
- Testing or dogfooding web apps, exploratory QA, and bug hunts
- Automating browser-backed workflows where Playwright/Puppeteer would be too heavy or less agent-friendly
- Automating supported non-web surfaces through specialized skills, including Electron desktop apps and Slack

## Official URL

https://agent-browser.dev/

## Source / repo URL

https://github.com/vercel-labs/agent-browser

## Trigger phrases

- "open a website"
- "fill out a form"
- "click a button"
- "take a screenshot"
- "scrape data from a page"
- "test this web app"
- "login to a site"
- "automate browser actions"
- "use agent-browser"

## Setup

Global npm install from the official README:

```bash
npm install -g agent-browser
agent-browser install  # Download Chrome from Chrome for Testing, first time only
```

Other documented install paths: local `npm install agent-browser`, Homebrew on macOS, or `cargo install agent-browser`. On Linux, run `agent-browser install --with-deps` when system dependencies are missing.

For source builds:

```bash
git clone https://github.com/vercel-labs/agent-browser
cd agent-browser
pnpm install
pnpm build
pnpm build:native
pnpm link --global
agent-browser install
```

Agent skill install path:

```bash
npx skills add vercel-labs/agent-browser
```

## Usage notes

- Core loop: `agent-browser open <url>`, `agent-browser snapshot -i`, interact with refs such as `agent-browser click @e3`, then re-snapshot after page changes.
- The CLI serves version-matched skill docs: start with `agent-browser skills get core`; use `--full` for the full command reference and templates.
- Specialized skill docs are available through `agent-browser skills get electron`, `slack`, `dogfood`, `vercel-sandbox`, and `agentcore`.
- Supports semantic locators (`find role`, `find text`, `find label`, etc.), CSS selectors, screenshots, PDF export, tabs/windows, cookies/storage, network inspection/HAR, viewport/device settings, batch execution, auth vault, saved state, and an observability dashboard.
- Package metadata lists version `0.27.0`, Apache-2.0 license, homepage `https://agent-browser.dev`, and repository `https://github.com/vercel-labs/agent-browser` at intake time.

## Caveats

- First-time setup needs a compatible browser; `agent-browser install` downloads Chrome from Chrome for Testing, while existing Chrome/Brave/Playwright/Puppeteer installations may be auto-detected.
- Snapshot refs are fresh per snapshot and become stale after navigation, form submits, dialogs, dynamic re-renders, or other page changes.
- Building from source requires Rust and pnpm; the daemon itself does not require Playwright or Puppeteer.
- The `chat` command requires AI Gateway configuration, including `AI_GATEWAY_API_KEY`.
- Browser automation can expose credentials or private page data; use the documented auth vault/state workflows for sensitive logins.

## Related

- Playwright
- Puppeteer
- Chrome DevTools Protocol
- Browser automation / web QA tools
