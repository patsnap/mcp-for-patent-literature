# Advanced Patent Search

> by [PatSnap](https://www.patsnap.com)

## Product Definition

Provides flexible and in-depth advanced patent search capabilities. It supports semantic, similarity, image, patent-number, nested-query, analytics, and keyword-assist workflows, enabling experienced users to build and refine complex search strategies efficiently. It is suitable for search specialists, analysts, and demanding research projects. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- Provides flexible
- in-depth advanced patent search capabilities. It supports semantic
- similarity
- image
- patent-number
- nested-query
- analytics
- keyword-assist workflows

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "advanced_patent_search": {
      "url": "https://connect.patsnap.com/33072f/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/1f837249-fce5-4ae3-96b5-1d9038ec41d5](https://open.patsnap.com/marketplace/mcp-servers/1f837249-fce5-4ae3-96b5-1d9038ec41d5)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
