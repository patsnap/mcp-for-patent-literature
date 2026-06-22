---
name: deep-patent-mining
description: Designed for deeper mining of technical content from patent text and classification data. It supports analysis of technology topics, the three technical elements of problem-solution-effect, strategic emerging industries, materials, application areas, and classification explanations, helping users move from patent retrieval to real technical understanding. It is useful for technology breakdown, domain research, and R&D inspiration.
homepage: https://open.patsnap.com/marketplace/mcp-servers/d1f84e46-f494-4927-aba8-94eeaef94c55
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"deep_patent_mining": {"url": "https://connect.patsnap.com/7cc6ae/mcp", "type": "streamableHttp"}}}
---

# Deep Patent Mining

Use this skill when a user needs Deep Patent Mining capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "deep_patent_mining": {
      "url": "https://connect.patsnap.com/7cc6ae/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/d1f84e46-f494-4927-aba8-94eeaef94c55](https://open.patsnap.com/marketplace/mcp-servers/d1f84e46-f494-4927-aba8-94eeaef94c55)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
