# Deep Patent Mining

> by [PatSnap](https://www.patsnap.com)

## Product Definition

Designed for deeper mining of technical content from patent text and classification data. It supports analysis of technology topics, the three technical elements of problem-solution-effect, strategic emerging industries, materials, application areas, and classification explanations, helping users move from patent retrieval to real technical understanding. It is useful for technology breakdown, domain research, and R&D inspiration. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- Designed for deeper mining of technical content from patent text
- classification data. It supports analysis of technology topics
- the three technical elements of problem-solution-effect
- strategic emerging industries
- materials
- application areas
- classification explanations
- helping users move from patent retrieval to real technical understanding. It is useful for technology breakdown

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "deep_patent_mining": {
      "url": "https://connect.patsnap.com/7cc6ae/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/d1f84e46-f494-4927-aba8-94eeaef94c55](https://open.patsnap.com/marketplace/mcp-servers/d1f84e46-f494-4927-aba8-94eeaef94c55)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
