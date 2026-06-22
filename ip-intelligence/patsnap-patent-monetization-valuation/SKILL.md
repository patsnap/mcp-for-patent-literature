---
name: patsnap-patent-monetization-valuation
description: PatSnap Patent Monetization & Valuation MCP for AI agents. A tool designed for patent transactions, licensing, and commercialization-oriented valuation. It combines patent value, legal status, licensing, transfer, reexamination and invalidation proceedings, and full-text information to help users judge whether a patent is better suited for sale, licensing, or continued holding. It is useful for patent operations, asset disposal, and commercialization assessment.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-monetize
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/11227f/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Patent Monetization & Valuation

This skill connects your AI agent to **PatSnap's Patent Monetization & Valuation MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Patent Monetization & Valuation MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "patent_monetization_valuation": {
      "url": "https://connect.patsnap.com/11227f/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-monetize

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

- Use Patent Monetization & Valuation to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Monetization & Valuation.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-monetize](https://open.patsnap.com/marketplace/mcp-servers/patent-monetize)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
