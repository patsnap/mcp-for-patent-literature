---
name: patsnap-patent-briefing
description: PatSnap Patent Briefing MCP for AI agents. A quick-read tool for understanding a patent or patent family. It brings together bibliographic data, legal status, family information, the three core technical elements, drawings, and translations of specifications, abstracts, and claims so that even users without a patent background can grasp the key points quickly. It is useful for internal communication, early screening, patent training, and client briefings.
homepage: https://open.patsnap.com/marketplace/mcp-servers/patent-briefing
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/958a46/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# Patent Briefing

This skill connects your AI agent to **PatSnap's Patent Briefing MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap Patent Briefing MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "patent_briefing": {
      "url": "https://connect.patsnap.com/958a46/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/patent-briefing

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

- Use Patent Briefing to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by Patent Briefing.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/patent-briefing](https://open.patsnap.com/marketplace/mcp-servers/patent-briefing)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
