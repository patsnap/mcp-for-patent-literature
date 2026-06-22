# Patent Valuation Scorecard

> by [PatSnap](https://www.patsnap.com)

## Product Definition

Breaks patent value into multiple scoring dimensions such as technology, legal strength and stability, market relevance, strategy, protection scope, and commercialization outlook. This helps users compare patent quality and business potential in a more structured way instead of relying on a single signal. It is useful for project screening, asset tiering, transaction review, and portfolio management. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- Breaks patent value into multiple scoring dimensions such as technology
- legal strength
- stability
- market relevance
- strategy
- protection scope
- commercialization outlook. This helps users compare patent quality
- business potential in a more structured way instead of relying on a single signal. It is useful for project screening

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "patent_valuation_scorecard": {
      "url": "https://connect.patsnap.com/67d1b4/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/ff5b188b-48c5-49ce-aaa7-0b1294a89d55](https://open.patsnap.com/marketplace/mcp-servers/ff5b188b-48c5-49ce-aaa7-0b1294a89d55)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
