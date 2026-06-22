---
name: patent-legal-status-annuity
description: Focused on reviewing patent legal status, annuity status, and core legal documents. It supports annuity payment information, legal status, full text, specifications, claims, and citation-related signals to help determine whether a patent remains in force and whether there are title changes or lapse risks. It is suitable for maintenance management, transaction checks, licensing review, and due diligence.
homepage: https://open.patsnap.com/marketplace/mcp-servers/cba8ca99-fcc3-4cb6-8afd-baf393151692
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"patent_legal_status_annuity": {"url": "https://connect.patsnap.com/30096b/mcp", "type": "streamableHttp"}}}
---

# Patent Legal Status & Annuity

Use this skill when a user needs Patent Legal Status & Annuity capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "patent_legal_status_annuity": {
      "url": "https://connect.patsnap.com/30096b/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/cba8ca99-fcc3-4cb6-8afd-baf393151692](https://open.patsnap.com/marketplace/mcp-servers/cba8ca99-fcc3-4cb6-8afd-baf393151692)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
