---
name: patsnap-patent-legal-status-annuity
description: PatSnap Patent Legal Status & Annuity MCP for AI agents. Focused on reviewing patent legal status, annuity status, and core legal documents. It supports annuity payment information, legal status, full text, specifications, claims, and citation-related signals to help determine whether a patent remains in force and whether there are title changes or lapse risks. It is suitable for maintenance management, transaction checks, licensing review, and due diligence.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-status
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/30096b/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Patent Legal Status & Annuity

This skill connects your AI agent to **PatSnap's Patent Legal Status & Annuity MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Patent Legal Status & Annuity MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "patent_legal_status_annuity": {
      "url": "https://connect.patsnap.com/30096b/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-status

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

- Use Patent Legal Status & Annuity to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Legal Status & Annuity.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-status](https://open.patsnap.com/marketplace/mcp-servers/patent-status)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
