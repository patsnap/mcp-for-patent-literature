# PatSnap Finance MCP Servers

> by [PatSnap](https://www.patsnap.com)

Official Model Context Protocol (MCP) servers for Finance, powered by PatSnap's proprietary intelligence platform. These servers give AI agents structured access to PatSnap data, search, analytics, and workflow capabilities for this domain.

## Available MCP Servers

| Server | Focus | Quick Link |
|---|---|---|
| **Internal Patent Data Connector** | Provides a unified connection layer for bringing patent data into internal systems, applications, and automated workflows. It exposes com... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/91e1eddf-d691-4eb7-bd36-7d76e4d1d3f9) Or [Repo](https://github.com/patsnap/mcp/tree/main/finance/patsnap-internal-patent-data-connector) |

## Setup

All servers follow the same setup pattern. You can connect one or all of them depending on your use case.

### 1. Get an API Key

Log in to the [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key.

### 2. Connect the MCP Servers

Run the following commands in your terminal with an MCP-compatible client:

```bash
# Internal Patent Data Connector
claude mcp add --transport http internal_patent_data_connector \
  "https://connect.patsnap.com/cac75e/mcp"
```

Set your API key as an environment variable:

```bash
export PATSNAP_API_KEY=sk-your-key-here
```

### 3. Verify

In your MCP-compatible client, confirm that the added servers show as connected.

## Resources

- [PatSnap](https://www.patsnap.com)
- [PatSnap Developer Portal](https://open.patsnap.com)
- [PatSnap MCP Marketplace](https://open.patsnap.com/marketplace/mcp-servers)
- [PatSnap MCP Server Source](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com) ? Innovate with Confidence.
