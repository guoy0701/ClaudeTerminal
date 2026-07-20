# ClaudeTerminal

**A chat-style desktop GUI for Claude Code.**

ClaudeTerminal renders your Claude Code sessions as a single chat-style message stream with terminal aesthetics — plus the things a raw terminal can't give you: real block folding, multi-tab concurrent sessions, multi-account switching, unattended auto-resume when you hit rate limits, cross-session full-text search, and a floating "dynamic island" companion window. Session data is fully interoperable with the official `claude` CLI — start here, continue in the terminal, or the other way around.

![screenshot](./docs/screenshot.png)

📖 中文用户手册：[docs/使用说明.md](./docs/使用说明.md)

## Download

Grab the latest **`ClaudeTerminal-Setup-x.y.z.exe`** from the [**Releases**](../../releases) page, run it, done. The app auto-updates from here. A portable **`.zip`** (no installer) is also attached to each release.

> Windows SmartScreen may warn because the installer isn't code-signed yet. Click **More info → Run anyway** if you trust the source.

## Requirements

- **Windows 10/11 x64**
- **[Claude Code](https://claude.com/claude-code) installed and logged in** — ClaudeTerminal drives the official `@anthropic-ai/claude-agent-sdk` and reuses your Claude Code authentication. It runs on *your own* Claude login and quota; no extra API key needed, no data leaves your machine.

## Highlights

- **Multi-account switching** — keep several Claude accounts as profiles; bind each tab to a different account, with per-account quota tracking. Account A hits the 5-hour limit? Open a tab on account B and keep going.
- **Unattended automation** — auto-resume when the rate-limit window resets (with max-rounds, deadline, auto-compact and cheap-model-compact controls), plus scheduled tasks that can launch fully autonomous sessions at a set time.
- **Terminal parity, or not — your choice** — a "classic" UI style replicates the official CLI pixel-for-pixel (banner, `? for shortcuts`, Claude orange), while the "modern" style adds real GUI power. All official keyboard habits work: `Shift+Tab` mode cycling, double-`Esc` rewind, `↑↓` history, `Ctrl+R` reverse search, and the `/` `@` `!` `#` input prefixes.
- **Interoperable with the official CLI** — sessions live in `~/.claude/projects/`, permission rules in `.claude/settings.local.json`, memory in `CLAUDE.md`. Zero lock-in: switch between GUI and terminal at any time.
- **Cross-session full-text search** — `Ctrl+Shift+F` searches every session on your machine (including ones from the terminal) and restores any hit into a new tab.
- **Dynamic island** — an always-on-top capsule showing each tab's state; answer questions, approve permissions and plans right on the island without switching windows.

## More features

- Chat-style message stream: every turn, tool call, and thinking block is a structured, **collapsible** card
- Multi-tab concurrent sessions, each with its own working directory, permission mode — and account
- Status HUD: model, permission mode, context/quota bars, session stats (tokens, cost), and a **prompt-cache timer**
- Interactive cards: permission prompts, question choices, plan approval, engine-error recovery
- Rewind (double-tap Esc), transcript view (Ctrl+O), Markdown export (Ctrl+S), turn-rail navigation
- 30+ slash commands implemented natively (`/model`, `/effort`, `/status`, `/cost`, `/mcp`, `/automation`, …)
- Image paste, `@` file completion, `!` local commands, `#` project memory
- 8 themes (4 palettes × light/dark) and live Chinese/English UI switching

## Key shortcuts

**Enter** send · **Shift+Enter** newline · **Esc** interrupt · **Shift+Tab** cycle permission mode · double-tap **Esc** rewind · **Ctrl+F** search · **Ctrl+Shift+F** search all sessions · **Ctrl+S** export Markdown · **Ctrl+O** transcript · **Ctrl+G** file changes · **Ctrl+B** background tasks · **Ctrl+Tab / Ctrl+1–9** switch tabs

## Feedback

Bugs, ideas, feature requests → [**GitHub Issues**](../../issues) (or the in-app `/feedback` command / Help menu). 中文 issue 完全欢迎。

## About this repository

This repository hosts the **binary releases** for ClaudeTerminal. New installers are published here so the app's built-in auto-updater can fetch new versions automatically.

## License

[MIT](./LICENSE)
