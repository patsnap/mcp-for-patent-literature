---
name: scientific-literature-journals
description: Provides a unified search entry for scientific literature, journals, authors, institutions, and citation information. It helps users find relevant research quickly, identify key authors and organizations, and understand the influence of a study through citation signals. It is suitable for topic research, literature reviews, scientific intelligence, and study planning.
homepage: https://open.patsnap.com/marketplace/mcp-servers/dcfdc2d0-9d81-4cdd-8689-b89ae98b8a50
metadata:
  author: PatSnap
  category: "R&D-Innovation"
  requires:
    mcp_config: {"mcpServers": {"scientific_literature_journals": {"url": "https://connect.patsnap.com/eba075/mcp", "type": "streamableHttp"}}}
---

# Scientific Literature & Journals

Use this skill when a user needs Scientific Literature & Journals capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "scientific_literature_journals": {
      "url": "https://connect.patsnap.com/eba075/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/dcfdc2d0-9d81-4cdd-8689-b89ae98b8a50](https://open.patsnap.com/marketplace/mcp-servers/dcfdc2d0-9d81-4cdd-8689-b89ae98b8a50)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
