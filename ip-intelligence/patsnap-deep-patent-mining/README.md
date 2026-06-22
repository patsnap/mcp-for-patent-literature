# Deep Patent Mining

> by [PatSnap](https://www.patsnap.com)

## Product Definition

PatSnap Deep Patent Mining MCP is a Model Context Protocol server that connects AI agents to PatSnap's Deep Patent Mining capabilities. Designed for deeper mining of technical content from patent text and classification data. It supports analysis of technology topics, the three technical elements of problem-solution-effect, strategic emerging industries, materials, application areas, and classification explanations, helping users move from patent retrieval to real technical understanding. It is useful for technology breakdown, domain research, and R&D inspiration.

## Quick Links

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Deep Patent Mining MCP](https://open.patsnap.com/marketplace/mcp-servers/patent-mining)

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
    "deep_patent_mining": {
      "url": "https://connect.patsnap.com/7cc6ae/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [PatSnap Open Platform](https://open.patsnap.com).

## Usage Example

- Use Deep Patent Mining to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Deep Patent Mining.

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/patent-mining](https://open.patsnap.com/marketplace/mcp-servers/patent-mining)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com) ? Innovate with Confidence.
