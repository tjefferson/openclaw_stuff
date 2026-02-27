# clawhub-skill-stats

An [OpenClaw](https://openclaw.ai) Skill for querying any ClawHub skill's statistics directly from the command line — no need to open the slow ClawHub web UI.

## Features

- Query a single skill's stats (stars, downloads, current installs, all-time installs)
- Batch compare multiple skills side by side
- Search skills by keyword and view stats in one go

## Supported Metrics

| Metric | Description |
|---|---|
| Stars | Number of users who starred the skill |
| Downloads | Total download count |
| Current Installs | Number of active installations |
| All-time Installs | Total installations since release |

## Installation

Copy the `clawhub-skill-stats` folder to one of the following locations:

- **Workspace level** (highest priority): `<your-project>/skills/clawhub-skill-stats/`
- **User level**: `~/.openclaw/skills/clawhub-skill-stats/`

Or install via ClawHub CLI:

```bash
clawhub install clawhub-skill-stats
```

## Usage

Once installed, ask the AI in your OpenClaw session:

- "查一下 self-improving-agent 在 ClawHub 上的统计数据"
- "Compare stats of tavily-search and self-improving-agent"
- "Search ClawHub for skills related to web scraping and show their stats"

The skill instructs the AI to use `curl` + `python3` to call the public ClawHub API and format the results.

## API Reference

- **Endpoint**: `GET https://clawhub.ai/api/skill?slug={slug}`
- **Auth**: None required (public API)
- **Response fields**: `stars`, `downloads`, `installsCurrent`, `installsAllTime`, `comments`, `versions`

## Requirements

- `curl` (pre-installed on macOS/Linux)
- `python3` (pre-installed on macOS/Linux)

## License

MIT
