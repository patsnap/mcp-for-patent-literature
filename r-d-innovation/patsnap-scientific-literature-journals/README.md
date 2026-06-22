# Scientific Literature & Journals

> by [PatSnap](https://www.patsnap.com)

## Product Definition

Provides a unified search entry for scientific literature, journals, authors, institutions, and citation information. It helps users find relevant research quickly, identify key authors and organizations, and understand the influence of a study through citation signals. It is suitable for topic research, literature reviews, scientific intelligence, and study planning. This MCP server connects AI agents to PatSnap data and workflow capabilities for the R&D-Innovation domain.

## Supported Tools and Query Types

- Provides a unified search entry for scientific literature
- journals
- authors
- institutions
- citation information. It helps users find relevant research quickly
- identify key authors
- organizations
- understand the influence of a study through citation signals. It is suitable for topic research

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "scientific_literature_journals": {
      "url": "https://connect.patsnap.com/eba075/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/dcfdc2d0-9d81-4cdd-8689-b89ae98b8a50](https://open.patsnap.com/marketplace/mcp-servers/dcfdc2d0-9d81-4cdd-8689-b89ae98b8a50)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
