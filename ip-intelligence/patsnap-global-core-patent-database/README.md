# Global Core Patent Database

> by [PatSnap](https://www.patsnap.com)

## Product Definition

A core patent data tool for high-frequency patent workflows. It supports search, full text and drawings, legal status, licensing, transfer, pledge, and reexamination and invalidation proceeding information, helping teams complete patent checks and fact verification efficiently. It is suitable for daily search, case research, legal support, and operational analysis. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- A core patent data tool for high-frequency patent workflows. It supports search
- full text
- drawings
- legal status
- licensing
- transfer
- pledge
- reexamination

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "global_core_patent_database": {
      "url": "https://connect.patsnap.com/1458a4/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/8dc7ef1d-d900-4c6d-bec6-2a9c03e7456b](https://open.patsnap.com/marketplace/mcp-servers/8dc7ef1d-d900-4c6d-bec6-2a9c03e7456b)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
