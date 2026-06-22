---
name: innovation-report-generator
description: Turns analytical results into deliverable reports and task-based outputs. It supports enterprise reports, patent value reports, and novelty-check reports for technical ideas, with download and similar-patent comparison support to help teams produce standardized materials more efficiently. It is suitable for client delivery, internal reporting, and pre-sales support.
homepage: https://open.patsnap.com/marketplace/mcp-servers/8929e1a2-7b3b-4f9d-9bf2-2e5e29524bd3
metadata:
  author: PatSnap
  category: "R&D-Innovation"
  requires:
    mcp_config: {"mcpServers": {"innovation_report_generator": {"url": "https://connect.patsnap.com/1fadfc/mcp", "type": "streamableHttp"}}}
---

# Innovation Report Generator

Use this skill when a user needs Innovation Report Generator capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "innovation_report_generator": {
      "url": "https://connect.patsnap.com/1fadfc/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/8929e1a2-7b3b-4f9d-9bf2-2e5e29524bd3](https://open.patsnap.com/marketplace/mcp-servers/8929e1a2-7b3b-4f9d-9bf2-2e5e29524bd3)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
