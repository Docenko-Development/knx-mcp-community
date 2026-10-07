# Getting started with KNX-MCP

## 1. Install

1. Get **KNX-MCP** from the KNX Online Shop (MyKNX).
2. In ETS: *Settings → ETS Apps* → install / activate KNX-MCP.
3. Open a project. The KNX-MCP panel shows four tabs: Live monitor, Tools, Server settings, Protocol.

## 2. Switch the project on

New projects start **switched off**. In the panel or the ETS toolbar choose **"Switch project MCP on"**. Only switched-on projects are reachable by an AI client.

Default endpoints (the port can be changed in *Server settings*):

| ETS | Endpoint |
|---|---|
| ETS6 | `http://127.0.0.1:51900/mcp` |
| ETS5 | `http://127.0.0.1:51950/mcp` |

One endpoint serves all projects open in that ETS. With more than one project switched on, the assistant names the project in each call.

## 3. Connect your AI client

The panel (*Server settings → Client configuration*) shows ready-to-copy snippets **including your access key**. The examples below use `<KEY>` as a placeholder.

### Claude Desktop (configuration file, via mcp-remote)

`claude_desktop_config.json` only supports local (stdio) servers, so the bridge `mcp-remote` is used. Requires Node.js.

```json
{
  "mcpServers": {
    "knx-ets6": {
      "command": "npx",
      "args": [
        "mcp-remote@latest",
        "http://127.0.0.1:51900/mcp",
        "--allow-http",
        "--header",
        "X-KnxMcp-Key:<KEY>"
      ]
    }
  }
}
```

Do **not** put a `url` entry into `claude_desktop_config.json` — Claude Desktop may silently drop the whole `mcpServers` section.

### Claude Code and other clients with native HTTP support

```json
{
  "mcpServers": {
    "knx-ets6": {
      "type": "http",
      "url": "http://127.0.0.1:51900/mcp",
      "headers": { "X-KnxMcp-Key": "<KEY>" }
    }
  }
}
```

### Other MCP clients

Any client that speaks MCP over HTTP (Streamable HTTP) works with the endpoint URL and the header `X-KnxMcp-Key`. Clients that only start local programs use `mcp-remote` as shown above.

## 4. First steps

Ask your assistant, for example:

- "Which projects can you reach?"
- "Give me an overview of the building and the group address structure."
- "Which group addresses have no datapoint type or more than one sender?"
- "Create switch, dimming value and status addresses for rooms 2.01 to 2.06."

Changes appear in the panel and wait for your confirmation. Undo works as usual in ETS.

## 5. Bus functions

Select a bus connection in ETS. KNX-MCP listens and sends through that connection.
In **ETS5**, telegrams captured by the app itself carry no sender address — start a group monitor in ETS and choose **KNX-MCP as its decoding app** to get the sender.

## 6. Network access (optional)

By default the endpoint is reachable from the local computer only. If you enable network access in *Server settings*, keep the access key secret and use a VPN or a trusted network: the connection is plain HTTP without encryption. `mcp-remote` needs `--allow-http` for this; some clients refuse plain HTTP over the network entirely.

## 7. Permissions

| Group | Default |
|---|---|
| Read, analyse, navigate, export | allowed |
| Telegrams | allowed — sending a value asks every time |
| Change project | confirmation required |
| Program devices | blocked |

Every tool can be set to *allowed*, *confirmation* or *blocked*. The read-only switch per project blocks all changes and sending.
