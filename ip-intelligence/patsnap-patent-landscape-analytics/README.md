# Patent Landscape Analytics

> by [PatSnap](https://www.patsnap.com)

## Product Definition

PatSnap Patent Landscape Analytics MCP is a Model Context Protocol server that connects AI agents to PatSnap's Patent Landscape Analytics capabilities. Converts patent search results into practical patent landscape analysis. It covers filing trends, technology composition, leading applicants, jurisdiction and patent office distribution, technical branches, technology mapping, and technology life cycle to help teams understand the competitive structure and direction of a technology space. It is useful for landscape reviews, competitor analysis, portfolio planning, and early-stage research.

## Quick Links

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Patent Landscape Analytics MCP](https://open.patsnap.com/marketplace/mcp-servers/patent-landscape)

## Data Sources and Coverage

Powered by PatSnap's proprietary patent database, covering 200M+ patents across 170+ jurisdictions including USPTO, EPO, WIPO, and more. Updated continuously with the latest patent publications.

## Supported Tools

- Search and discovery: semantic, keyword, identifier, or fielded search workflows
- Retrieval and detail: fetch complete records or supporting details when available
- Analytics and synthesis: summarize, compare, count, or structure retrieved results

## Installation

```json
{
  "mcpServers": {
    "patent_landscape_analytics": {
      "url": "https://connect.patsnap.com/59100a/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [PatSnap Open Platform](https://open.patsnap.com).

## Usage Example

- Use Patent Landscape Analytics to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Landscape Analytics.

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/patent-landscape](https://open.patsnap.com/marketplace/mcp-servers/patent-landscape)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com). Innovate with Confidence.
