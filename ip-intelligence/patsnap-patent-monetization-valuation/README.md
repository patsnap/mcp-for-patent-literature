# Patent Monetization & Valuation

> by [PatSnap](https://www.patsnap.com)

## Product Definition

A tool designed for patent transactions, licensing, and commercialization-oriented valuation. It combines patent value, legal status, licensing, transfer, reexamination and invalidation proceedings, and full-text information to help users judge whether a patent is better suited for sale, licensing, or continued holding. It is useful for patent operations, asset disposal, and commercialization assessment. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- A tool designed for patent transactions
- licensing
- commercialization-oriented valuation. It combines patent value
- legal status
- licensing
- transfer
- reexamination
- invalidation proceedings

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "patent_monetization_valuation": {
      "url": "https://connect.patsnap.com/11227f/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/1c20be56-30a5-4917-b5dd-f88986fbe9f8](https://open.patsnap.com/marketplace/mcp-servers/1c20be56-30a5-4917-b5dd-f88986fbe9f8)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
