---
name: patsnap-clinical-trials
description: Patsnap Clinical Trials MCP for AI agents. Intelligent clinical trial retrieval system, covering registered trial tracking, trial details and results analysis, and supporting clinical semantic search.
homepage: https://open.patsnap.com/marketplace/mcp-servers/clinical-trials
metadata:
  author: Patsnap
  category: "Life Science"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/051cd3/logic-mcp?apikey=YOUR_API_KEY"
---
## Setup
Get your API Key at https://open.patsnap.com

# Patsnap Clinical Trials

This skill connects your AI agent to **Patsnap's Clinical Trials MCP server** — providing professional-grade life sciences intelligence.

Intelligent clinical trial retrieval system, covering registered trial tracking, trial details and results analysis, and supporting clinical semantic search.

## Prerequisites

This skill requires the **Patsnap Clinical Trials MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "clinical_trials": {
      "url": "https://connect.patsnap.com/051cd3/logic-mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).
For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/clinical-trials

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

### Trial Landscape
1. Search `clinical_trial_search` by drug, disease, and phase.
2. Fetch trial details with `clinical_trial_fetch`.
3. Search results with `clinical_trial_result_search` for published outcomes.

---

## Resources

- **Patsnap Life Sciences**: [eureka.patsnap.com/ls-landing](https://eureka.patsnap.com/ls-landing)
- **MCP Server**: [open.patsnap.com/marketplace/mcp-servers](https://open.patsnap.com/marketplace/mcp-servers/clinical-trials)
- **API Docs**: [open.patsnap.com/devportal](https://open.patsnap.com/devportal)
