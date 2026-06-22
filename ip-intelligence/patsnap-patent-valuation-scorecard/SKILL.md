---
name: patsnap-patent-valuation-scorecard
description: PatSnap Patent Valuation Scorecard MCP for AI agents. Breaks patent value into multiple scoring dimensions such as technology, legal strength and stability, market relevance, strategy, protection scope, and commercialization outlook. This helps users compare patent quality and business potential in a more structured way instead of relying on a single signal. It is useful for project screening, asset tiering, transaction review, and portfolio management.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-value
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/67d1b4/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Patent Valuation Scorecard

This skill connects your AI agent to **PatSnap's Patent Valuation Scorecard MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Patent Valuation Scorecard MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "patent_valuation_scorecard": {
      "url": "https://connect.patsnap.com/67d1b4/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-value

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

- Use Patent Valuation Scorecard to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Valuation Scorecard.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-value](https://open.patsnap.com/marketplace/mcp-servers/patent-value)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
