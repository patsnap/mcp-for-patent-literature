---
name: patsnap-patent-landscape-analytics
description: PatSnap Patent Landscape Analytics MCP for AI agents. Converts patent search results into practical patent landscape analysis. It covers filing trends, technology composition, leading applicants, jurisdiction and patent office distribution, technical branches, technology mapping, and technology life cycle to help teams understand the competitive structure and direction of a technology space. It is useful for landscape reviews, competitor analysis, portfolio planning, and early-stage research.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-landscape
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/59100a/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Patent Landscape Analytics

This skill connects your AI agent to **PatSnap's Patent Landscape Analytics MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Patent Landscape Analytics MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "patent_landscape_analytics": {
      "url": "https://connect.patsnap.com/59100a/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-landscape

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

- Use Patent Landscape Analytics to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Landscape Analytics.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-landscape](https://open.patsnap.com/marketplace/mcp-servers/patent-landscape)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
