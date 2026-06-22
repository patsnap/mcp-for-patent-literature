# Patent Visual Analytics

> by [PatSnap](https://www.patsnap.com)

## Product Definition

Transforms patent data into more intuitive visual analysis. It supports chart-based views across trends, patent types, value, litigation, citations, and technical-effect phrase distribution so users can spot concentration, hotspots, and outliers faster. It is useful for management reporting, client presentations, and thematic analysis. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- Transforms patent data into more intuitive visual analysis. It supports chart-based views across trends
- patent types
- value
- litigation
- citations
- technical-effect phrase distribution so users can spot concentration
- hotspots
- outliers faster. It is useful for management reporting

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "patent_visual_analytics": {
      "url": "https://connect.patsnap.com/3fd502/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/29ec8427-6e8a-4125-a246-10af19b24001](https://open.patsnap.com/marketplace/mcp-servers/29ec8427-6e8a-4125-a246-10af19b24001)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
