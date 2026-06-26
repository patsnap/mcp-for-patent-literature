---
name: patsnap-scientific-literature-journals
description: PatSnap Scientific Literature & Journals MCP for AI agents. Provides a unified search entry for scientific literature, journals, authors, institutions, and citation information. It helps users find relevant research quickly, identify key authors and organizations, and understand the influence of a study through citation signals. It is suitable for topic research, literature reviews, scientific intelligence, and study planning.
homepage: https://open.patsnap.com/marketplace/mcp-servers/literature-search
metadata:
  author: PatSnap
  category: "RD Innovation"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/eba075/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Scientific Literature & Journals

This skill connects your AI agent to **PatSnap's Scientific Literature & Journals MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for RD Innovation tasks.

## Prerequisites

This skill requires the **PatSnap Scientific Literature & Journals MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "scientific_literature_journals": {
      "url": "https://connect.patsnap.com/eba075/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/literature-search

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

- Use Scientific Literature & Journals to search for the most relevant records for my topic.
- Summarize the top results and cite the returned record names or IDs.
- Compare the findings and suggest follow-up queries.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/literature-search](https://open.patsnap.com/marketplace/mcp-servers/literature-search)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
