# Patent Legal Status & Annuity

> by [PatSnap](https://www.patsnap.com)

## Product Definition

PatSnap Patent Legal Status & Annuity MCP is a Model Context Protocol server that connects AI agents to PatSnap's Patent Legal Status & Annuity capabilities. Focused on reviewing patent legal status, annuity status, and core legal documents. It supports annuity payment information, legal status, full text, specifications, claims, and citation-related signals to help determine whether a patent remains in force and whether there are title changes or lapse risks. It is suitable for maintenance management, transaction checks, licensing review, and due diligence.

## Quick Links

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Patent Legal Status & Annuity MCP](https://open.patsnap.com/marketplace/mcp-servers/patent-status)

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
    "patent_legal_status_annuity": {
      "url": "https://connect.patsnap.com/30096b/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [PatSnap Open Platform](https://open.patsnap.com).

## Usage Example

- Use Patent Legal Status & Annuity to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Legal Status & Annuity.

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/patent-status](https://open.patsnap.com/marketplace/mcp-servers/patent-status)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com) ? Innovate with Confidence.
