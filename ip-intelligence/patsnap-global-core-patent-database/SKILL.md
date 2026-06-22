---
name: patsnap-global-core-patent-database
description: PatSnap Global Core Patent Database MCP for AI agents. A core patent data tool for high-frequency patent workflows. It supports search, full text and drawings, legal status, licensing, transfer, pledge, and reexamination and invalidation proceeding information, helping teams complete patent checks and fact verification efficiently. It is suitable for daily search, case research, legal support, and operational analysis.
homepage: https://open.patsnap.com/marketplace/mcp-servers/core-patents
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/1458a4/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Global Core Patent Database

This skill connects your AI agent to **PatSnap's Global Core Patent Database MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Global Core Patent Database MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "global_core_patent_database": {
      "url": "https://connect.patsnap.com/1458a4/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/core-patents

---

## Instructions for AI Agents

### Step 1: Understand the user's search intent
Identify the target entities, date ranges, owners, patent numbers, technologies, or document types in the user's request.

### Step 2: Choose the right workflow
Use semantic, fielded, identifier-based, analytics, or retrieval workflows according to the task and available MCP tools.

### Step 3: Synthesize and cite
Present results in a structured format and cite returned patent numbers, record IDs, titles, organizations, or source names when available.

---

## Example Workflows

- Use Global Core Patent Database to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Global Core Patent Database.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/core-patents](https://open.patsnap.com/marketplace/mcp-servers/core-patents)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
