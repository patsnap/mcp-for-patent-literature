# Patent Valuation Scorecard

> by [PatSnap](https://www.patsnap.com)

## Product Definition

PatSnap Patent Valuation Scorecard MCP is a Model Context Protocol server that connects AI agents to PatSnap's Patent Valuation Scorecard capabilities. Breaks patent value into multiple scoring dimensions such as technology, legal strength and stability, market relevance, strategy, protection scope, and commercialization outlook. This helps users compare patent quality and business potential in a more structured way instead of relying on a single signal. It is useful for project screening, asset tiering, transaction review, and portfolio management.

## Quick Links

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Patent Valuation Scorecard MCP](https://open.patsnap.com/marketplace/mcp-servers/patent-value)

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
    "patent_valuation_scorecard": {
      "url": "https://connect.patsnap.com/67d1b4/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [PatSnap Open Platform](https://open.patsnap.com).

## Usage Example

- Use Patent Valuation Scorecard to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Valuation Scorecard.

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/patent-value](https://open.patsnap.com/marketplace/mcp-servers/patent-value)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com) ? Innovate with Confidence.
