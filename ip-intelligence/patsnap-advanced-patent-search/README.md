# Advanced Patent Search

> by [PatSnap](https://www.patsnap.com)

## Product Definition

PatSnap Advanced Patent Search MCP is a Model Context Protocol server that connects AI agents to PatSnap's Advanced Patent Search capabilities. Provides flexible and in-depth advanced patent search capabilities. It supports semantic, similarity, image, patent-number, nested-query, analytics, and keyword-assist workflows, enabling experienced users to build and refine complex search strategies efficiently. It is suitable for search specialists, analysts, and demanding research projects.

## Quick Links

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Advanced Patent Search MCP](https://open.patsnap.com/marketplace/mcp-servers/patent-search)

## Data Sources and Coverage

Powered by PatSnap's proprietary patent database, covering 200M+ patents across 170+ jurisdictions including USPTO, EPO, WIPO, and more. Updated continuously with the latest patent publications.

## Supported Tools

- Search by semantic similarity: search_patents_by_semantic
- Search by patent number      : search_patent_by_pn
- Search by image              : upload_patent_image
- Search by assignee           : search_patents_by_original_assignee, search_patents_by_current_assignee
- Nested / field query         : search_patents_nested, search_patent_field
- Analytics & count            : search_patent_count
- Keyword suggestions          : suggest_keywords

## Installation

```json
{
  "mcpServers": {
    "advanced_patent_search": {
      "url": "https://connect.patsnap.com/33072f/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [PatSnap Open Platform](https://open.patsnap.com).

## Usage Example

- Find patents filed by Tesla in the last 3 years related to solid-state battery technology.
- Search for patents similar to US10123456B2.
- How many patents were filed on autonomous driving perception systems in 2023?

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/patent-search](https://open.patsnap.com/marketplace/mcp-servers/patent-search)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com). Innovate with Confidence.
