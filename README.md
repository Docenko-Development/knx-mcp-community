# KNX-MCP Community

**KNX-MCP** is an ETS App that lets AI assistants such as Claude, Microsoft Copilot or ChatGPT work directly inside the open ETS project — through the Model Context Protocol (MCP) and the official ETS SDK.

This repository is the public place for **questions, bug reports, feature ideas, setup examples and release notes**. It does not contain the source code of KNX-MCP.

| | |
|---|---|
| Current version | **1.1.0.0** (Release 1) — validated by KNX |
| Runs in | ETS5 (5.7 or later) and ETS6 |
| Get it | KNX Online Shop → *KNX-MCP* (free in Release 1) |
| Website | https://knx-mcp.com |
| Publisher | Gerald Docenko |

## What KNX-MCP does

- **Read and check** the project: building, topology, trades, functions, group addresses, devices, objects, parameters, history, to-do list — with checks for typical mistakes.
- **Find addresses from plain language** ("switch on the light at the bar").
- **Change the project**: group addresses, rooms, devices, links, parameters, trades, functions, to-do items. Every change waits for your confirmation in the app panel and is a normal ETS undo step.
- **Bus via the ETS connection**: monitor, read and send values (each telegram confirmed), identify devices, scan a line. Programming devices is blocked by default.
- **Several projects and several AI clients** at the same time, in ETS5 and ETS6.

The endpoint is reachable from the local computer only by default. KNX-MCP sends no data to the publisher; project data only goes to the assistant you connect yourself.

## Getting started

See [docs/getting-started.md](docs/getting-started.md) — installation, switching the project on, and client configuration for Claude Desktop, Claude Code and other MCP clients.

## Where to go

| You want to … | Use |
|---|---|
| ask a question, share an example or a workflow | **Discussions** → Q&A / Show and tell |
| report a bug | **Issues** → *Bug report* |
| suggest a feature | **Discussions** → Ideas (or Issues → *Feature request*) |
| report a security problem | **not public** — see [SECURITY.md](SECURITY.md) |

Please **never post project files, passwords, keys or customer data** here. Screenshots and log excerpts are fine once customer names and addresses are removed.

## Release notes

- [1.1.0.0 — Release 1](docs/release-notes/1.1.0.0.md)

## License

KNX-MCP is licensed under its End User License Agreement, available in MyKNX with the app. This repository contains documentation only. KNX and ETS are trademarks of KNX Association; KNX-MCP is not a product of KNX Association.

---

### Deutsch, kurz

KNX-MCP ist eine ETS-App, mit der KI-Assistenten direkt im geöffneten ETS-Projekt arbeiten – über MCP und das offizielle ETS-SDK, in ETS5 und ETS6. Hier gibt es Fragen und Antworten, Fehlerberichte, Ideen, Einrichtungsbeispiele und Versionshinweise. Beiträge gern auch auf Deutsch. Bezug über den KNX Online Shop, mehr auf https://knx-mcp.com.
