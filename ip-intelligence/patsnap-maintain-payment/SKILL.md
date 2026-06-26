---
name: patsnap-maintain-payment
description: PatSnap Maintain Payment MCP for AI agents. A global patent search tool for freedom-to-operate assessment. It supports query-based, semantic, and image search, and can be combined with patent family, legal status, and analytics views to help users identify patents that may create FTO barriers more systematically. It is suitable for pre-launch assessment, RD route selection, and legal support.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-fto
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/e5851d/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Maintain Payment

This skill connects your AI agent to **PatSnap's Maintain Payment MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Maintain Payment MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "maintain_payment": {
      "url": "https://connect.patsnap.com/e5851d/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-fto

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

- Use Maintain Payment to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Maintain Payment.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-fto](https://open.patsnap.com/marketplace/mcp-servers/patent-fto)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
