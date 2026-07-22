---
name: patsnap-current-awareness
description: Patsnap Current Awareness MCP for AI agents. Tracking system for pharmaceutical industry dynamics and cutting-edge news, covering global medical news search and in-depth news detail mining.
homepage: https://open.patsnap.com/marketplace/mcp-servers/current-awareness
metadata:
  author: Patsnap
  category: "Life Science"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/401c6d/logic-mcp?apikey=YOUR_API_KEY"
---
## Setup
Get your API Key at https://open.patsnap.com

# Patsnap Current Awareness

This skill connects your AI agent to **Patsnap's Current Awareness MCP server** — providing professional-grade life sciences intelligence.

Tracking system for pharmaceutical industry dynamics and cutting-edge news, covering global medical news search and in-depth news detail mining.

## Prerequisites

This skill requires the **Patsnap Current Awareness MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "current_awareness": {
      "url": "https://connect.patsnap.com/401c6d/logic-mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).
For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/current-awareness

---

## Instructions for AI Agents

### Step 1: Normalize Entities First
Before executing any search or fetch operation, normalize targets, drugs, diseases, companies, and clinical trial IDs to Patsnap internal IDs when possible. This improves retrieval accuracy.

### Step 2: Choose the Right Tool
Select search tools for discovery and corresponding `_fetch` tools for full records. Use vector search tools for natural-language evidence queries.

### Step 3: Fetch Full Records
Search tools return summary results with IDs. Follow up with the appropriate `_fetch` tool when the user needs complete details.

### Step 4: Synthesize and Structure Output
Lead with key findings, cite sources, highlight data gaps, and use tables for comparisons.

---

## Example Workflows

### Competitive Monitoring
1. Search `news_search` for a competitor or drug class.
2. Fetch full articles with `news_fetch`.
3. Summarize key developments and market signals.

---

## Resources

- **Patsnap Life Sciences**: [eureka.patsnap.com/ls-landing](https://eureka.patsnap.com/ls-landing)
- **MCP Server**: [open.patsnap.com/marketplace/mcp-servers](https://open.patsnap.com/marketplace/mcp-servers/current-awareness)
- **API Docs**: [open.patsnap.com/devportal](https://open.patsnap.com/devportal)
