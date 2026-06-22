# Maintain Payment

> by [PatSnap](https://www.patsnap.com)

## Product Definition

PatSnap Maintain Payment MCP is a Model Context Protocol server that connects AI agents to PatSnap's Maintain Payment capabilities. A global patent search tool for freedom-to-operate assessment. It supports query-based, semantic, and image search, and can be combined with patent family, legal status, and analytics views to help users identify patents that may create FTO barriers more systematically. It is suitable for pre-launch assessment, R&D route selection, and legal support.

## Quick Links

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Maintain Payment MCP](https://open.patsnap.com/marketplace/mcp-servers/patent-fto)

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
    "maintain_payment": {
      "url": "https://connect.patsnap.com/e5851d/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [PatSnap Open Platform](https://open.patsnap.com).

## Usage Example

- Use Maintain Payment to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Maintain Payment.

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/patent-fto](https://open.patsnap.com/marketplace/mcp-servers/patent-fto)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com) ? Innovate with Confidence.
