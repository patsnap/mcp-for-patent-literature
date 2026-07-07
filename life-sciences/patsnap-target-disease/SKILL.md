---
name: patsnap-target-disease
description: PatSnap Target & Disease MCP for AI agents. Target and disease profiling tool, covering target characterization, disease profiling, and epidemiology evidence retrieval.
homepage: https://open.patsnap.com/marketplace/mcp-servers/target-disease
metadata:
  author: PatSnap
  category: "Life Science"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/2a2645/logic-mcp?apikey=YOUR_API_KEY"
---
## Setup
Get your API Key at https://open.patsnap.com

# PatSnap Target & Disease

This skill connects your AI agent to **PatSnap's Target & Disease MCP server** — providing professional-grade life sciences intelligence.

Target and disease profiling tool, covering target characterization, disease profiling, and epidemiology evidence retrieval.

## Prerequisites

This skill requires the **PatSnap Target & Disease MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "target_disease": {
      "url": "https://connect.patsnap.com/2a2645/logic-mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).
For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/target-disease

---

## Instructions for AI Agents

### Step 1: Normalize Entities First
Before executing any search or fetch operation, normalize targets, drugs, diseases, companies, and clinical trial IDs to PatSnap internal IDs when possible. This improves retrieval accuracy.

### Step 2: Choose the Right Tool
Select search tools for discovery and corresponding `_fetch` tools for full records. Use vector search tools for natural-language evidence queries.

### Step 3: Fetch Full Records
Search tools return summary results with IDs. Follow up with the appropriate `_fetch` tool when the user needs complete details.

### Step 4: Synthesize and Structure Output
Lead with key findings, cite sources, highlight data gaps, and use tables for comparisons.

---

## Example Workflows

### Target Prioritization
1. Normalize the target name with `ls_ner_nor_normalize`.
2. Use `target_fetch` to retrieve target structure and druggability data.
3. Search `epidemiology_search` for disease burden evidence.

### Disease Landscape
1. Normalize the disease name.
2. Use `disease_fetch` to retrieve disease profile and standard of care.
3. Cross-reference epidemiology evidence to assess unmet need.

---

## Resources

- **PatSnap Life Sciences**: [eureka.patsnap.com/ls-landing](https://eureka.patsnap.com/ls-landing)
- **MCP Server**: [open.patsnap.com/marketplace/mcp-servers](https://open.patsnap.com/marketplace/mcp-servers/target-disease)
- **API Docs**: [open.patsnap.com/devportal](https://open.patsnap.com/devportal)
