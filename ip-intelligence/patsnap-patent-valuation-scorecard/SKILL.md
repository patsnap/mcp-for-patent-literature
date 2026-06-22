---
name: patent-valuation-scorecard
description: Breaks patent value into multiple scoring dimensions such as technology, legal strength and stability, market relevance, strategy, protection scope, and commercialization outlook. This helps users compare patent quality and business potential in a more structured way instead of relying on a single signal. It is useful for project screening, asset tiering, transaction review, and portfolio management.
homepage: https://open.patsnap.com/marketplace/mcp-servers/ff5b188b-48c5-49ce-aaa7-0b1294a89d55
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"patent_valuation_scorecard": {"url": "https://connect.patsnap.com/67d1b4/mcp", "type": "streamableHttp"}}}
---

# Patent Valuation Scorecard

Use this skill when a user needs Patent Valuation Scorecard capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "patent_valuation_scorecard": {
      "url": "https://connect.patsnap.com/67d1b4/mcp",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

## Instructions

- Normalize the user's entities before detailed retrieval when the MCP provides normalization tools.
- Prefer search tools for broad discovery and fetch/detail tools for complete records.
- Cite returned record names, IDs, patents, papers, trials, or company names when available.

## Resources

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/ff5b188b-48c5-49ce-aaa7-0b1294a89d55](https://open.patsnap.com/marketplace/mcp-servers/ff5b188b-48c5-49ce-aaa7-0b1294a89d55)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
