# PatSnap RD Innovation MCP Servers

MCP servers for scientific literature discovery, journal intelligence, innovation report generation, patent value reporting, and novelty-check workflows, powered by PatSnap's proprietary RD intelligence databases.

## About PatSnap

PatSnap is a global innovation intelligence platform covering 200M+ patents across 170+ jurisdictions (USPTO, EPO, WIPO and more), 216M+ scientific papers, pharma records, clinical trials, and RD data.

To explore PatSnap RD data interactively, try [Eureka](https://eureka.patsnap.com), PatSnap's AI-native RD assistant. To access RD data programmatically, use the MCP servers or REST API via [PatSnap Open Platform](https://open.patsnap.com).

## Available MCP Servers

| Server | Description | Open Platform |
| :--- | :--- | :--- |
| **Innovation Report Generator** | Innovation, patent value, and novelty-check report generation | [Innovation Report Generator](https://open.patsnap.com/marketplace/mcp-servers/8929e1a2-7b3b-4f9d-9bf2-2e5e29524bd3) |
| **Scientific Literature & Journals** | Scientific literature, journal, author, institution, and citation discovery | [Scientific Literature & Journals](https://open.patsnap.com/marketplace/mcp-servers/dcfdc2d0-9d81-4cdd-8689-b89ae98b8a50) |

## Quick Start

### 1. Get your API key

Register at [PatSnap Open Platform](https://open.patsnap.com) to get your free API key.

### 2. Add to your MCP client

Add the following to your MCP configuration (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "patsnap_innovation_report_generator": {
      "url": "https://connect.patsnap.com/1fadfc/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Replace `YOUR_API_KEY` with your key from PatSnap Open Platform.

Each MCP server has its own URL. See the individual README or Open Platform page for the exact endpoint.

## Resources

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Eureka](https://eureka.patsnap.com)
- [PatSnap MCP Server Source](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com). Innovate with Confidence.
