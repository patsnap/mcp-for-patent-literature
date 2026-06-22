# Maintain Payment

> by [PatSnap](https://www.patsnap.com)

## Product Definition

A global patent search tool for freedom-to-operate assessment. It supports query-based, semantic, and image search, and can be combined with patent family, legal status, and analytics views to help users identify patents that may create FTO barriers more systematically. It is suitable for pre-launch assessment, R&D route selection, and legal support. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- A global patent search tool for freedom-to-operate assessment. It supports query-based
- semantic
- image search
- can be combined with patent family
- legal status
- analytics views to help users identify patents that may create FTO barriers more systematically. It is suitable for pre-launch assessment
- R&D route selection
- legal support

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "maintain_payment": {
      "url": "https://connect.patsnap.com/e5851d/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/aae364b6-a111-4e17-a99f-d7b74539cfa3](https://open.patsnap.com/marketplace/mcp-servers/aae364b6-a111-4e17-a99f-d7b74539cfa3)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
