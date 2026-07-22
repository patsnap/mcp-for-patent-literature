---
name: patsnap-drug-asset
description: Patsnap Drug & Asset MCP for AI agents. Drug and asset intelligence retrieval platform, covering drug search, drug details analysis, and development milestone tracking.
homepage: https://open.patsnap.com/marketplace/mcp-servers/drug-asset
metadata:
  author: Patsnap
  category: "Life Science"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/30cd71/logic-mcp?apikey=YOUR_API_KEY"
---
## Setup
Get your API Key at https://open.patsnap.com

# Patsnap Drug & Asset

This skill connects your AI agent to **Patsnap's Drug & Asset MCP server** — providing professional-grade life sciences intelligence.

Drug and asset intelligence retrieval platform, covering drug search, drug details analysis, and development milestone tracking.

## Prerequisites

This skill requires the **Patsnap Drug & Asset MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "drug_asset": {
      "url": "https://connect.patsnap.com/30cd71/logic-mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).
For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/drug-asset

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

### Asset Due Diligence
1. Use `drug_search` to locate the asset and its competitors.
2. Fetch full details with `drug_fetch`.
3. Retrieve `drug_milestone_fetch` for development timeline.

---

## Resources

- **Patsnap Life Sciences**: [eureka.patsnap.com/ls-landing](https://eureka.patsnap.com/ls-landing)
- **MCP Server**: [open.patsnap.com/marketplace/mcp-servers](https://open.patsnap.com/marketplace/mcp-servers/drug-asset)
- **API Docs**: [open.patsnap.com/devportal](https://open.patsnap.com/devportal)
