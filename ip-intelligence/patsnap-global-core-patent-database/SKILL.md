---
name: global-core-patent-database
description: A core patent data tool for high-frequency patent workflows. It supports search, full text and drawings, legal status, licensing, transfer, pledge, and reexamination and invalidation proceeding information, helping teams complete patent checks and fact verification efficiently. It is suitable for daily search, case research, legal support, and operational analysis.
homepage: https://open.patsnap.com/marketplace/mcp-servers/8dc7ef1d-d900-4c6d-bec6-2a9c03e7456b
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"global_core_patent_database": {"url": "https://connect.patsnap.com/1458a4/mcp", "type": "streamableHttp"}}}
---

# Global Core Patent Database

Use this skill when a user needs Global Core Patent Database capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "global_core_patent_database": {
      "url": "https://connect.patsnap.com/1458a4/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/8dc7ef1d-d900-4c6d-bec6-2a9c03e7456b](https://open.patsnap.com/marketplace/mcp-servers/8dc7ef1d-d900-4c6d-bec6-2a9c03e7456b)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
