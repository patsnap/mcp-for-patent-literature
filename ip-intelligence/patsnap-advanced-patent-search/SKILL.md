---
name: patsnap-advanced-patent-search
description: PatSnap Advanced Patent Search MCP for AI agents. Provides flexible and in-depth advanced patent search capabilities. It supports semantic, similarity, image, patent-number, nested-query, analytics, and keyword-assist workflows, enabling experienced users to build and refine complex search strategies efficiently. It is suitable for search specialists, analysts, and demanding research projects.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-search
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/33072f/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Advanced Patent Search

This skill connects your AI agent to **PatSnap's Advanced Patent Search MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Advanced Patent Search MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "advanced_patent_search": {
      "url": "https://connect.patsnap.com/33072f/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-search

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

- Find patents filed by Tesla in the last 3 years related to solid-state battery technology.
- Search for patents similar to US10123456B2.
- How many patents were filed on autonomous driving perception systems in 2023?

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-search](https://open.patsnap.com/marketplace/mcp-servers/patent-search)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
