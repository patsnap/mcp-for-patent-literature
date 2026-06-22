# Patent Legal Status & Annuity

> by [PatSnap](https://www.patsnap.com)

## Product Definition

Focused on reviewing patent legal status, annuity status, and core legal documents. It supports annuity payment information, legal status, full text, specifications, claims, and citation-related signals to help determine whether a patent remains in force and whether there are title changes or lapse risks. It is suitable for maintenance management, transaction checks, licensing review, and due diligence. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- Focused on reviewing patent legal status
- annuity status
- core legal documents. It supports annuity payment information
- legal status
- full text
- specifications
- claims
- citation-related signals to help determine whether a patent remains in force

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "patent_legal_status_annuity": {
      "url": "https://connect.patsnap.com/30096b/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/cba8ca99-fcc3-4cb6-8afd-baf393151692](https://open.patsnap.com/marketplace/mcp-servers/cba8ca99-fcc3-4cb6-8afd-baf393151692)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
