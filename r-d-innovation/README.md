# PatSnap R&D Innovation MCP Servers

> by [PatSnap](https://www.patsnap.com)

Official Model Context Protocol (MCP) servers for R&D Innovation, powered by PatSnap's proprietary intelligence platform. These servers give AI agents structured access to PatSnap data, search, analytics, and workflow capabilities for this domain.

## Available MCP Servers

| Server | Focus | Quick Link |
|---|---|---|
| **Innovation Report Generator** | Turns analytical results into deliverable reports and task-based outputs. It supports enterprise reports, patent value reports, and novel... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/8929e1a2-7b3b-4f9d-9bf2-2e5e29524bd3) Or [Repo](https://github.com/patsnap/mcp/tree/main/r-d-innovation/patsnap-innovation-report-generator) |
| **Scientific Literature & Journals** | Provides a unified search entry for scientific literature, journals, authors, institutions, and citation information. It helps users find... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/dcfdc2d0-9d81-4cdd-8689-b89ae98b8a50) Or [Repo](https://github.com/patsnap/mcp/tree/main/r-d-innovation/patsnap-scientific-literature-journals) |

## Setup

All servers follow the same setup pattern. You can connect one or all of them depending on your use case.

### 1. Get an API Key

Log in to the [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key.

### 2. Connect the MCP Servers

Run the following commands in your terminal with an MCP-compatible client:

```bash
# Innovation Report Generator
claude mcp add --transport http innovation_report_generator \
  "https://connect.patsnap.com/1fadfc/mcp"

# Scientific Literature & Journals
claude mcp add --transport http scientific_literature_journals \
  "https://connect.patsnap.com/eba075/mcp"
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
