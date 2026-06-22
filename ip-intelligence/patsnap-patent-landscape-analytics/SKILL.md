---
name: patent-landscape-analytics
description: Converts patent search results into practical patent landscape analysis. It covers filing trends, technology composition, leading applicants, jurisdiction and patent office distribution, technical branches, technology mapping, and technology life cycle to help teams understand the competitive structure and direction of a technology space. It is useful for landscape reviews, competitor analysis, portfolio planning, and early-stage research.
homepage: https://open.patsnap.com/marketplace/mcp-servers/6dd83771-70f2-46ce-b4aa-6fdf60ace3f8
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"patent_landscape_analytics": {"url": "https://connect.patsnap.com/59100a/mcp", "type": "streamableHttp"}}}
---

# Patent Landscape Analytics

Use this skill when a user needs Patent Landscape Analytics capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "patent_landscape_analytics": {
      "url": "https://connect.patsnap.com/59100a/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/6dd83771-70f2-46ce-b4aa-6fdf60ace3f8](https://open.patsnap.com/marketplace/mcp-servers/6dd83771-70f2-46ce-b4aa-6fdf60ace3f8)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
