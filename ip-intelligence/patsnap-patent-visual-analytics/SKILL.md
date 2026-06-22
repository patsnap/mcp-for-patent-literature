---
name: patsnap-patent-visual-analytics
description: PatSnap Patent Visual Analytics MCP for AI agents. Transforms patent data into more intuitive visual analysis. It supports chart-based views across trends, patent types, value, litigation, citations, and technical-effect phrase distribution so users can spot concentration, hotspots, and outliers faster. It is useful for management reporting, client presentations, and thematic analysis.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-visual
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/3fd502/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Patent Visual Analytics

This skill connects your AI agent to **PatSnap's Patent Visual Analytics MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Patent Visual Analytics MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "patent_visual_analytics": {
      "url": "https://connect.patsnap.com/3fd502/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-visual

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

- Use Patent Visual Analytics to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Visual Analytics.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-visual](https://open.patsnap.com/marketplace/mcp-servers/patent-visual)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
