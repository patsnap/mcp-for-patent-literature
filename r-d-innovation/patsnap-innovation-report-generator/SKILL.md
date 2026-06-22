---
name: patsnap-innovation-report-generator
description: PatSnap Innovation Report Generator MCP for AI agents. Turns analytical results into deliverable reports and task-based outputs. It supports enterprise reports, patent value reports, and novelty-check reports for technical ideas, with download and similar-patent comparison support to help teams produce standardized materials more efficiently. It is suitable for client delivery, internal reporting, and pre-sales support.
homepage: https://open.patsnap.com/marketplace/mcp-servers/report-gen
metadata:
  author: PatSnap
  category: "R&D Innovation"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/1fadfc/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Innovation Report Generator

This skill connects your AI agent to **PatSnap's Innovation Report Generator MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for R&D Innovation tasks.

## Prerequisites

This skill requires the **PatSnap Innovation Report Generator MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "innovation_report_generator": {
      "url": "https://connect.patsnap.com/1fadfc/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/report-gen

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

- Use Innovation Report Generator to search for the most relevant records for my topic.
- Summarize the top results and cite the returned record names or IDs.
- Compare the findings and suggest follow-up queries.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/report-gen](https://open.patsnap.com/marketplace/mcp-servers/report-gen)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
