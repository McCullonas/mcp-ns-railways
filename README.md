# mcp-ns-railways

MCP server for Dutch railway queries via the [NS API](https://apiportal.ns.nl).
Covers NS intercity, Sprinter, and international train services.

> **Status: Work in Progress** — Server scaffolding is in place. Tools are not yet implemented.

---

## Prerequisites

- [Bun](https://bun.sh) runtime (`curl -fsSL https://bun.sh/install | bash`)
- An [NS API key](https://apiportal.ns.nl) — free registration required

---

## Planned Tools

- `ns_search_stations` — Search Dutch railway stations by name
- `ns_get_departures` — Get departures from a station with live delay info
- `ns_get_trips` — Plan journeys between two Dutch stations
- `ns_get_disruptions` — Get current disruptions and maintenance works

---

## Data Source

The [NS Developer Portal](https://apiportal.ns.nl) provides access to NS timetable,
real-time, and disruption data. Free registration gives access to the Reisinformatie API.

---

## Install

```bash
git clone git@github.com:McCullonas/mcp-ns-railways.git
cd mcp-ns-railways
bun install
```

---

## MCP Client Configuration (once implemented)

```json
{
  "mcpServers": {
    "ns-railways": {
      "command": "bun",
      "args": ["run", "/path/to/mcp-ns-railways/src/index.ts"],
      "env": {
        "NS_API_KEY": "your-key-here"
      }
    }
  }
}
```

---

## Licence

MIT
