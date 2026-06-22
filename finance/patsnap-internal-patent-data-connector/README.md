# Internal Patent Data Connector

> by [PatSnap](https://www.patsnap.com)

## Product Definition

PatSnap Internal Patent Data Connector MCP is a Model Context Protocol server that connects AI agents to PatSnap's Internal Patent Data Connector capabilities. Provides a unified connection layer for bringing patent data into internal systems, applications, and automated workflows. It exposes commonly used capabilities such as search, legal status, transfer, licensing, pledge, classification, and bibliographic data so patent data can be embedded into existing business processes more easily. It is suitable for system integration, data platforms, and workflow automation.

## Quick Links

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Internal Patent Data Connector MCP](https://open.patsnap.com/marketplace/mcp-servers/patent-connector)

## Data Sources and Coverage

Powered by PatSnap data services and enterprise-connected patent data workflows. Coverage depends on enabled internal data connectors, account permissions, and API key scope.

## Supported Tools

- Search and discovery — semantic, keyword, identifier, or fielded search workflows
- Retrieval and detail — fetch complete records or supporting details when available
- Analytics and synthesis — summarize, compare, count, or structure retrieved results

## Installation

```json
{
  "mcpServers": {
    "internal_patent_data_connector": {
      "url": "https://connect.patsnap.com/cac75e/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [PatSnap Open Platform](https://open.patsnap.com).

## Usage Example

- Use Internal Patent Data Connector to search for the most relevant records for my topic.
- Summarize the top results and cite the returned record names or IDs.
- Compare the findings and suggest follow-up queries.

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/patent-connector](https://open.patsnap.com/marketplace/mcp-servers/patent-connector)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com) ? Innovate with Confidence.
