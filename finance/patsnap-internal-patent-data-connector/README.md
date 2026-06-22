# Internal Patent Data Connector

> by [PatSnap](https://www.patsnap.com)

## Product Definition

Provides a unified connection layer for bringing patent data into internal systems, applications, and automated workflows. It exposes commonly used capabilities such as search, legal status, transfer, licensing, pledge, classification, and bibliographic data so patent data can be embedded into existing business processes more easily. It is suitable for system integration, data platforms, and workflow automation. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Finance domain.

## Supported Tools and Query Types

- Provides a unified connection layer for bringing patent data into internal systems
- applications
- automated workflows. It exposes commonly used capabilities such as search
- legal status
- transfer
- licensing
- pledge
- classification

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "internal_patent_data_connector": {
      "url": "https://connect.patsnap.com/cac75e/mcp",
      "type": "streamableHttp"
    }
  }
}
```

## Simplest Usage Example

1. Get a PatSnap API key from [PatSnap Open Platform](https://open.patsnap.com).
2. Replace `$PATSNAP_API_KEY` or `YOUR_API_KEY` in the MCP config.
3. Add the config to an MCP-compatible client.
4. Ask a simple domain question, such as: `Search recent records related to this target, drug, company, or patent topic.`

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/91e1eddf-d691-4eb7-bd36-7d76e4d1d3f9](https://open.patsnap.com/marketplace/mcp-servers/91e1eddf-d691-4eb7-bd36-7d76e4d1d3f9)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
