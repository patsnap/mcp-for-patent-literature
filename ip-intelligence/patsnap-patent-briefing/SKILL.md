---
name: patent-briefing
description: A quick-read tool for understanding a patent or patent family. It brings together bibliographic data, legal status, family information, the three core technical elements, drawings, and translations of specifications, abstracts, and claims so that even users without a patent background can grasp the key points quickly. It is useful for internal communication, early screening, patent training, and client briefings.
homepage: https://open.patsnap.com/marketplace/mcp-servers/e54e3afc-df5c-47e9-878f-1e7bb38a7275
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"patent_briefing": {"url": "https://connect.patsnap.com/958a46/mcp", "type": "streamableHttp"}}}
---

# Patent Briefing

Use this skill when a user needs Patent Briefing capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "patent_briefing": {
      "url": "https://connect.patsnap.com/958a46/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/e54e3afc-df5c-47e9-878f-1e7bb38a7275](https://open.patsnap.com/marketplace/mcp-servers/e54e3afc-df5c-47e9-878f-1e7bb38a7275)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
