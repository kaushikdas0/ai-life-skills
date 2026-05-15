# hyperframes

## Summary

Open-source video rendering framework by HeyGen. Write HTML with data attributes, preview in browser, render to MP4. Designed for AI agent workflows — agents already speak HTML, so no proprietary DSL or React required. Supports GSAP, Lottie, CSS, Three.js animation runtimes via a Frame Adapter pattern. Ships skills/plugins for Claude Code, Cursor, Codex, and Gemini CLI.

## Aliases

- heygen hyperframes
- html video renderer
- html-to-video

## When to use

- Creating video compositions from HTML/CSS/JS
- Agent-driven video generation workflows
- Programmatic video rendering (deterministic, same input = same output)
- Replacing Remotion when open-source licensing (Apache 2.0) matters
- Quick product intros, social clips, animated chart races, pitch videos from structured data

## Official URL

https://hyperframes.heygen.com/

## Source / repo URL

https://github.com/heygen-com/hyperframes

## Trigger phrases

- "render video from HTML"
- "html to video"
- "agent video generation"
- "video composition framework"
- "hyperframes"

## Setup

```bash
npx hyperframes init my-video
cd my-video
npx hyperframes preview      # live reload preview
npx hyperframes render       # render to MP4
```

Requirements: Node.js >= 22, FFmpeg.

For agent skill install: `npx skills add heygen-com/hyperframes`

## Usage notes

- Compositions are plain HTML files with `data-*` attributes — no build step needed.
- `index.html` plays as-is in a browser; the CLI drives headless Chrome for deterministic render.
- Agent skills register as slash commands (`/hyperframes`, `/hyperframes-cli`, `/hyperframes-media`, `/gsap`, etc.).
- Supports Tailwind v4 browser-runtime styles.
- Licensed Apache 2.0 — fully open source, no per-render fees or seat caps.

## Caveats

- Distributed rendering not yet supported (single-machine only).
- Requires FFmpeg installed locally.
- Relatively new (18k+ stars, 963 commits) — check Issues for known gaps.

## Related

- [Remotion](https://www.remotion.dev) — React-based alternative (source-available license)
- [Hyperframes vs Remotion guide](https://hyperframes.heygen.com/guides/hyperframes-vs-remotion)
