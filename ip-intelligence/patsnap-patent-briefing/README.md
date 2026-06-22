# Patent Briefing

> by [PatSnap](https://www.patsnap.com)

## Product Definition

PatSnap Patent Briefing MCP is a Model Context Protocol server that connects AI agents to PatSnap's Patent Briefing capabilities. A quick-read tool for understanding a patent or patent family. It brings together bibliographic data, legal status, family information, the three core technical elements, drawings, and translations of specifications, abstracts, and claims so that even users without a patent background can grasp the key points quickly. It is useful for internal communication, early screening, patent training, and client briefings.

## Quick Links

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Patent Briefing MCP](https://open.patsnap.com/marketplace/mcp-servers/patent-briefing)

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
    "patent_briefing": {
      "url": "https://connect.patsnap.com/958a46/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [PatSnap Open Platform](https://open.patsnap.com).

## Usage Example

- Use Patent Briefing to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Briefing.

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/patent-briefing](https://open.patsnap.com/marketplace/mcp-servers/patent-briefing)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com) ? Innovate with Confidence.
