---
name: patsnap-internal-patent-data-connector
description: PatSnap Internal Patent Data Connector MCP for AI agents. Provides a unified connection layer for bringing patent data into internal systems, applications, and automated workflows. It exposes commonly used capabilities such as search, legal status, transfer, licensing, pledge, classification, and bibliographic data so patent data can be embedded into existing business processes more easily. It is suitable for system integration, data platforms, and workflow automation.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-connector
metadata:
  author: PatSnap
  category: "Finance"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/cac75e/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Internal Patent Data Connector

This skill connects your AI agent to **PatSnap's Internal Patent Data Connector MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for Finance tasks.

## Prerequisites

This skill requires the **PatSnap Internal Patent Data Connector MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "internal_patent_data_connector": {
      "url": "https://connect.patsnap.com/cac75e/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-connector

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

- Use Internal Patent Data Connector to search for the most relevant records for my topic.
- Summarize the top results and cite the returned record names or IDs.
- Compare the findings and suggest follow-up queries.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-connector](https://open.patsnap.com/marketplace/mcp-servers/patent-connector)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
