# Patent Briefing

> by [PatSnap](https://www.patsnap.com)

## Product Definition

A quick-read tool for understanding a patent or patent family. It brings together bibliographic data, legal status, family information, the three core technical elements, drawings, and translations of specifications, abstracts, and claims so that even users without a patent background can grasp the key points quickly. It is useful for internal communication, early screening, patent training, and client briefings. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- A quick-read tool for understanding a patent or patent family. It brings together bibliographic data
- legal status
- family information
- the three core technical elements
- drawings
- translations of specifications
- abstracts
- claims so that even users without a patent background can grasp the key points quickly. It is useful for internal communication

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "patent_briefing": {
      "url": "https://connect.patsnap.com/958a46/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/e54e3afc-df5c-47e9-878f-1e7bb38a7275](https://open.patsnap.com/marketplace/mcp-servers/e54e3afc-df5c-47e9-878f-1e7bb38a7275)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
