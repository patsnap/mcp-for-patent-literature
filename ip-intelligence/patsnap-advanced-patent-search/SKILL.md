---
name: advanced-patent-search
description: Provides flexible and in-depth advanced patent search capabilities. It supports semantic, similarity, image, patent-number, nested-query, analytics, and keyword-assist workflows, enabling experienced users to build and refine complex search strategies efficiently. It is suitable for search specialists, analysts, and demanding research projects.
homepage: https://open.patsnap.com/marketplace/mcp-servers/1f837249-fce5-4ae3-96b5-1d9038ec41d5
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"advanced_patent_search": {"url": "https://connect.patsnap.com/33072f/mcp", "type": "streamableHttp"}}}
---

# Advanced Patent Search

Use this skill when a user needs Advanced Patent Search capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "advanced_patent_search": {
      "url": "https://connect.patsnap.com/33072f/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/1f837249-fce5-4ae3-96b5-1d9038ec41d5](https://open.patsnap.com/marketplace/mcp-servers/1f837249-fce5-4ae3-96b5-1d9038ec41d5)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
