---
name: ip-innovation-courses
description: A one-stop learning entry for courses, course details, and training materials on IP and innovation. It helps teams build a structured understanding of patents, search, analysis, and business use while lowering the learning barrier for new users. It is useful for internal training, customer education, and knowledge enablement.
homepage: https://open.patsnap.com/marketplace/mcp-servers/172edf47-eae9-4f01-b8c0-e6018aab79bf
metadata:
  author: PatSnap
  category: "Ip-Intelligence"
  requires:
    mcp_config: {"mcpServers": {"ip_innovation_courses": {"url": "https://connect.patsnap.com/588922/mcp", "type": "streamableHttp"}}}
---

# IP & Innovation Courses

Use this skill when a user needs IP & Innovation Courses capabilities through PatSnap MCP.

## Setup

Configure the MCP server in your client:

```json
{
  "mcpServers": {
    "ip_innovation_courses": {
      "url": "https://connect.patsnap.com/588922/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/172edf47-eae9-4f01-b8c0-e6018aab79bf](https://open.patsnap.com/marketplace/mcp-servers/172edf47-eae9-4f01-b8c0-e6018aab79bf)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
