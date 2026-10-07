# KNX-MCP Community

**KNX-MCP** is an ETS App that connects an open ETS project to MCP-compatible AI assistants such as Claude, Microsoft Copilot or ChatGPT through the **Model Context Protocol (MCP)** and the official ETS SDK.

This repository is the public community space for **questions, bug reports, feature ideas, setup help, reusable skills and release information**. It does **not** contain the source code of KNX-MCP.

| | |
|---|---|
| Current version | **1.1.0.0 · Release 1** — validated by KNX |
| ETS support | **ETS5 (5.7 or later) and ETS6** |
| Availability | **Currently available free of charge** in the KNX Online Shop |
| Website | https://knx-mcp.com |
| Publisher | Gerald Docenko |

## Quick links

- **Get KNX-MCP:** https://my.knx.org/shop?action=search&search=KNX-MCP
- **Website:** https://knx-mcp.com
- **Getting started:** [docs/getting-started.md](docs/getting-started.md)
- **Questions & workflows:** https://github.com/Docenko-Development/knx-mcp-community/discussions
- **Bug reports:** https://github.com/Docenko-Development/knx-mcp-community/issues
- **Skills:** [skills/README.md](skills/README.md)
- **Release notes:** [1.1.0.0 · Release 1](docs/release-notes/1.1.0.0.md)
- **Security:** [SECURITY.md](SECURITY.md)

## What KNX-MCP does

KNX-MCP works with the project data that ETS itself provides — without exporting a separate project copy.

- **Read and inspect** building structure, topology, trades, functions, group addresses, devices, communication objects, parameters, history and the ETS to-do list.
- **Find group addresses from natural language**, including room names, common synonyms and typical actions such as switching, dimming or reading status values.
- **Check the project** for typical inconsistencies and suspicious configurations.
- **Change the project**: create or update rooms, group addresses, devices, links, parameters, trades, functions and to-do items.
- **Work with the KNX bus through ETS**: monitor telegrams, read and send values, identify devices and scan a line.
- **Use several open projects and several AI clients** at the same time in ETS5 and ETS6.

## You stay in control

Permissions are configured per project and per tool:

- **Allowed** — the tool may run directly.
- **Confirmation required** — KNX-MCP asks in the ETS panel before execution.
- **Blocked** — the tool cannot run.

A project-wide **read-only mode** disables changes and bus writes. Project changes are created as named ETS undo steps. Device programming is blocked by default.

## Data and privacy

KNX-MCP runs locally inside ETS. By default, its MCP endpoint is reachable only from the same computer.

KNX-MCP does not operate a publisher cloud service through which project data is routed. Project data is provided only to the MCP client that you connect. If that client uses a cloud AI provider, the provider's own terms and privacy rules apply.

Optional network access can be enabled explicitly. The KNX-MCP endpoint uses plain HTTP, so remote access should be limited to a trusted network or VPN and protected with the configured access key.

## Community: where to go

| You want to … | Use |
|---|---|
| ask a question or discuss a workflow | **GitHub Discussions** |
| share a setup example | **GitHub Discussions** |
| report a reproducible bug | **Issues → Bug report** |
| propose a product improvement | **Discussions** or **Issues → Feature request** |
| contribute a reusable skill or documentation improvement | **Pull request** |
| report a security problem | **Privately** — see [SECURITY.md](SECURITY.md) |
| discuss a commercial or confidential matter | **gerald@docenko.eu** |

Please **never post ETS project files, customer data, passwords, access keys, KNX Secure keys or other confidential information** in a public issue or discussion. Anonymised screenshots and excerpts are welcome.

See [SUPPORT.md](SUPPORT.md) for the complete support routing.

## Skills

The [`skills/`](skills/) directory is intended for reusable prompts, workflows and AI-client instructions that work with KNX-MCP. Skills should be project-independent, explain required permissions and make clear whether they only read data or may change the ETS project or access the bus.

## Languages

English is used as the primary documentation language so the material is useful internationally. Questions and contributions in **German or English** are welcome.

A short German overview is available in [docs/README-de.md](docs/README-de.md).

## License and trademarks

KNX-MCP is licensed under its End User License Agreement, available in MyKNX with the app. This repository contains community documentation and examples; it does not contain the KNX-MCP application source code.

KNX and ETS are trademarks of KNX Association. **KNX-MCP is a software product by Gerald Docenko and is not a product of KNX Association.**
