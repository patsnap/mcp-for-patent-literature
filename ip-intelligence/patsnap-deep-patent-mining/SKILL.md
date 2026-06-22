---
name: patsnap-deep-patent-mining
description: PatSnap Deep Patent Mining MCP for AI agents. Designed for deeper mining of technical content from patent text and classification data. It supports analysis of technology topics, the three technical elements of problem-solution-effect, strategic emerging industries, materials, application areas, and classification explanations, helping users move from patent retrieval to real technical understanding. It is useful for technology breakdown, domain research, and R&D inspiration.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-mining
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/7cc6ae/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Deep Patent Mining

This skill connects your AI agent to **PatSnap's Deep Patent Mining MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Deep Patent Mining MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "deep_patent_mining": {
      "url": "https://connect.patsnap.com/7cc6ae/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-mining

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

- Use Deep Patent Mining to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Deep Patent Mining.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-mining](https://open.patsnap.com/marketplace/mcp-servers/patent-mining)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
