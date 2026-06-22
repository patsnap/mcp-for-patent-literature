---
name: internal-patent-data-connector
description: Provides a unified connection layer for bringing patent data into internal systems, applications, and automated workflows. It exposes commonly used capabilities such as search, legal status, transfer, licensing, pledge, classification, and bibliographic data so patent data can be embedded into existing business processes more easily. It is suitable for system integration, data platforms, and workflow automation.
homepage: https://open.patsnap.com/marketplace/mcp-servers/91e1eddf-d691-4eb7-bd36-7d76e4d1d3f9
metadata:
  author: PatSnap
  category: "Finance"
  requires:
    mcp_config: {"mcpServers": {"internal_patent_data_connector": {"url": "https://connect.patsnap.com/cac75e/mcp", "type": "streamableHttp"}}}
---

# Internal Patent Data Connector

Use this skill when a user needs Internal Patent Data Connector capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "internal_patent_data_connector": {
      "url": "https://connect.patsnap.com/cac75e/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/91e1eddf-d691-4eb7-bd36-7d76e4d1d3f9](https://open.patsnap.com/marketplace/mcp-servers/91e1eddf-d691-4eb7-bd36-7d76e4d1d3f9)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
