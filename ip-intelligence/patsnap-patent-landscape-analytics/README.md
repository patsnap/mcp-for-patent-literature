# Patent Landscape Analytics

> by [PatSnap](https://www.patsnap.com)

## Product Definition

Converts patent search results into practical patent landscape analysis. It covers filing trends, technology composition, leading applicants, jurisdiction and patent office distribution, technical branches, technology mapping, and technology life cycle to help teams understand the competitive structure and direction of a technology space. It is useful for landscape reviews, competitor analysis, portfolio planning, and early-stage research. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- Converts patent search results into practical patent landscape analysis. It covers filing trends
- technology composition
- leading applicants
- jurisdiction
- patent office distribution
- technical branches
- technology mapping
- technology life cycle to help teams understand the competitive structure

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "patent_landscape_analytics": {
      "url": "https://connect.patsnap.com/59100a/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/6dd83771-70f2-46ce-b4aa-6fdf60ace3f8](https://open.patsnap.com/marketplace/mcp-servers/6dd83771-70f2-46ce-b4aa-6fdf60ace3f8)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
