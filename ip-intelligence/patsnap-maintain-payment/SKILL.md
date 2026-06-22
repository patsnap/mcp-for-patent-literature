---
name: maintain-payment
description: A global patent search tool for freedom-to-operate assessment. It supports query-based, semantic, and image search, and can be combined with patent family, legal status, and analytics views to help users identify patents that may create FTO barriers more systematically. It is suitable for pre-launch assessment, R&D route selection, and legal support.
homepage: https://open.patsnap.com/marketplace/mcp-servers/aae364b6-a111-4e17-a99f-d7b74539cfa3
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"maintain_payment": {"url": "https://connect.patsnap.com/e5851d/mcp", "type": "streamableHttp"}}}
---

# Maintain Payment

Use this skill when a user needs Maintain Payment capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "maintain_payment": {
      "url": "https://connect.patsnap.com/e5851d/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/aae364b6-a111-4e17-a99f-d7b74539cfa3](https://open.patsnap.com/marketplace/mcp-servers/aae364b6-a111-4e17-a99f-d7b74539cfa3)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
