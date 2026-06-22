# Patent Visual Analytics

> by [PatSnap](https://www.patsnap.com)

## Product Definition

PatSnap Patent Visual Analytics MCP is a Model Context Protocol server that connects AI agents to PatSnap's Patent Visual Analytics capabilities. Transforms patent data into more intuitive visual analysis. It supports chart-based views across trends, patent types, value, litigation, citations, and technical-effect phrase distribution so users can spot concentration, hotspots, and outliers faster. It is useful for management reporting, client presentations, and thematic analysis.

## Quick Links

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Patent Visual Analytics MCP](https://open.patsnap.com/marketplace/mcp-servers/patent-visual)

## Data Sources and Coverage

Powered by PatSnap's proprietary patent database, covering 200M+ patents across 170+ jurisdictions including USPTO, EPO, WIPO, and more. Updated continuously with the latest patent publications.

## Supported Tools

- Search and discovery — semantic, keyword, identifier, or fielded search workflows
- Retrieval and detail — fetch complete records or supporting details when available
- Analytics and synthesis — summarize, compare, count, or structure retrieved results

## Installation

```json
{
  "mcpServers": {
    "patent_visual_analytics": {
      "url": "https://connect.patsnap.com/3fd502/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [PatSnap Open Platform](https://open.patsnap.com).

## Usage Example

- Use Patent Visual Analytics to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Visual Analytics.

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/patent-visual](https://open.patsnap.com/marketplace/mcp-servers/patent-visual)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com) ? Innovate with Confidence.
