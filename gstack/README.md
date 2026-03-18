# gstack

**Garry Tan's open-source software factory for Claude Code.**

Turns Claude Code into a virtual engineering team — 13 specialist slash commands covering the full product lifecycle.

- **Source:** https://github.com/garrytan/gstack
- **License:** MIT
- **Version:** 0.6.4.0

## Installation

```bash
git clone https://github.com/garrytan/gstack.git ~/.claude/skills/gstack
cd ~/.claude/skills/gstack
./setup
```

> Requires [bun](https://bun.sh). The setup script builds a headless browser binary and downloads Playwright Chromium (~280 MB).

## Skills

| Command | Description |
|---|---|
| `/browse` | Headless browser — navigate, click, screenshot, diff (~100ms/cmd) |
| `/qa` | Full QA pass: test a web app and fix bugs found |
| `/qa-only` | QA report only, no fixes |
| `/ship` | Full ship workflow: merge, test, review, bump version, PR |
| `/review` | Pre-landing PR review (SQL safety, LLM trust, perf, security) |
| `/plan-ceo-review` | CEO/founder-mode plan review — rethink the problem |
| `/plan-eng-review` | Eng manager-mode plan review — lock architecture & scope |
| `/plan-design-review` | Designer's eye plan review |
| `/design-consultation` | Research landscape, propose design direction |
| `/design-review` | Visual QA — spacing, hierarchy, consistency |
| `/retro` | Weekly engineering retrospective from commit history |
| `/document-release` | Post-ship docs update |
| `/setup-browser-cookies` | Import cookies from your real browser for authenticated QA |
| `/gstack-upgrade` | Upgrade gstack to latest version |

## Usage Notes

- Use `/browse` for **all web browsing** — do not use `mcp__claude-in-chrome__*` tools directly.
- `/qa` and `/browse` require the compiled binary at `~/.claude/skills/gstack/browse/dist/browse`.
- Run `/setup-browser-cookies` once to enable authenticated browsing in QA flows.
