# Priomate integrations

[Priomate](https://priomate.com) is a task manager for individuals and teams. Its remote MCP server lets AI apps read and manage your tasks, notes, inbox, team projects and time tracking.

- MCP server URL: `https://mcp.priomate.com/mcp` (Streamable HTTP)
- Authentication: OAuth (the Priomate consent page opens on first connect)
- Requires a Priomate **Pro** or **Business** plan. On the Free plan the connection is refused.
- Some clients currently get read-only access.
- MCP Registry name: `com.priomate/priomate`

## Install

### Claude

Add a custom connector with the URL above. Step by step: [Connect Claude](https://docs.priomate.com/en/ai-connection/connect-claude).

### Cursor

Paste this link into your browser to install with one click:

```
cursor://anysphere.cursor-deeplink/mcp/install?name=Priomate&config=eyJ1cmwiOiJodHRwczovL21jcC5wcmlvbWF0ZS5jb20vbWNwIn0=
```

Or add to `mcp.json`:

```json
{
  "mcpServers": {
    "priomate": {
      "url": "https://mcp.priomate.com/mcp"
    }
  }
}
```

### Gemini CLI

> Per [geminicli.com](https://geminicli.com), Google replaced Gemini CLI with Antigravity CLI on June 18th, 2026 for unpaid tier and Google One users. If that applies to you, use the Antigravity instructions below.

```
gemini extensions install https://github.com/Sunksnoek/priomate-integrations
```

### Antigravity

Install as a plugin: the plugin lives in the [`antigravity`](antigravity) folder. Clone this repository, then run:

```
agy plugin install <path-to-clone>/antigravity
```

Or add the server manually to `~/.gemini/config/mcp_config.json` (all projects) or `<workspace>/.agents/mcp_config.json` (one workspace):

```json
{
  "mcpServers": {
    "priomate": {
      "serverUrl": "https://mcp.priomate.com/mcp"
    }
  }
}
```

In the Antigravity CLI, type `/mcp` to manage servers. In the IDE, open **Manage MCP Servers** and click **View raw config**.

### ChatGPT

Not available as a ChatGPT plugin yet. In apps that allow custom MCP connectors, add the URL manually.

### Other apps

Any app that supports remote MCP servers with OAuth works. See [Connect other AI apps](https://docs.priomate.com/en/ai-connection/connect-other-ai-apps).

## Links

- [Documentation](https://docs.priomate.com/en/ai-connection/connect-claude)
- [Privacy policy](https://priomate.com/en/datenschutz)

## License

MIT, see [LICENSE](LICENSE).
