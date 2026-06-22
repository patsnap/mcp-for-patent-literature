---
name: patent-visual-analytics
description: Transforms patent data into more intuitive visual analysis. It supports chart-based views across trends, patent types, value, litigation, citations, and technical-effect phrase distribution so users can spot concentration, hotspots, and outliers faster. It is useful for management reporting, client presentations, and thematic analysis.
homepage: https://open.patsnap.com/marketplace/mcp-servers/29ec8427-6e8a-4125-a246-10af19b24001
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"patent_visual_analytics": {"url": "https://connect.patsnap.com/3fd502/mcp", "type": "streamableHttp"}}}
---

# Patent Visual Analytics

Use this skill when a user needs Patent Visual Analytics capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "patent_visual_analytics": {
      "url": "https://connect.patsnap.com/3fd502/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/29ec8427-6e8a-4125-a246-10af19b24001](https://open.patsnap.com/marketplace/mcp-servers/29ec8427-6e8a-4125-a246-10af19b24001)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
