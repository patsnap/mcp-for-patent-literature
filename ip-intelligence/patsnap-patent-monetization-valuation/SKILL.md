---
name: patent-monetization-valuation
description: A tool designed for patent transactions, licensing, and commercialization-oriented valuation. It combines patent value, legal status, licensing, transfer, reexamination and invalidation proceedings, and full-text information to help users judge whether a patent is better suited for sale, licensing, or continued holding. It is useful for patent operations, asset disposal, and commercialization assessment.
homepage: https://open.patsnap.com/marketplace/mcp-servers/1c20be56-30a5-4917-b5dd-f88986fbe9f8
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"patent_monetization_valuation": {"url": "https://connect.patsnap.com/11227f/mcp", "type": "streamableHttp"}}}
---

# Patent Monetization & Valuation

Use this skill when a user needs Patent Monetization & Valuation capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "patent_monetization_valuation": {
      "url": "https://connect.patsnap.com/11227f/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/1c20be56-30a5-4917-b5dd-f88986fbe9f8](https://open.patsnap.com/marketplace/mcp-servers/1c20be56-30a5-4917-b5dd-f88986fbe9f8)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
