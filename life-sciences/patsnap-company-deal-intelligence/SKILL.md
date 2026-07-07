---
name: patsnap-company-deal-intelligence
description: PatSnap Company & Deal Intelligence MCP for AI agents. Intangible asset and commercial intelligence archive tool for pharmaceutical enterprises, covering organization profiles, R&D pipelines, deal records, and financial report evidence queries.
homepage: https://open.patsnap.com/marketplace/mcp-servers/company-deal-intelligence
metadata:
  author: PatSnap
  category: "Life Science"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/1f8934/logic-mcp?apikey=YOUR_API_KEY"
---
## Setup
Get your API Key at https://open.patsnap.com

# PatSnap Company & Deal Intelligence

This skill connects your AI agent to **PatSnap's Company & Deal Intelligence MCP server** — providing professional-grade life sciences intelligence.

Intangible asset and commercial intelligence archive tool for pharmaceutical enterprises, covering organization profiles, R&D pipelines, deal records, and financial report evidence queries.

## Prerequisites

This skill requires the **PatSnap Company & Deal Intelligence MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "company_deal_intelligence": {
      "url": "https://connect.patsnap.com/1f8934/logic-mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).
For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/company-deal-intelligence

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

### Company Profile
1. Use `organization_fetch` to retrieve company details.
2. Fetch pipeline with `organization_pipeline_fetch`.
3. Search `drug_deal_search` for recent BD activity.

### Deal Benchmarking
1. Search `drug_deal_search` by target or disease area.
2. Fetch full deal terms with `drug_deal_fetch`.
3. Compare deal values and structures across assets.

---

## Resources

- **PatSnap Life Sciences**: [eureka.patsnap.com/ls-landing](https://eureka.patsnap.com/ls-landing)
- **MCP Server**: [open.patsnap.com/marketplace/mcp-servers](https://open.patsnap.com/marketplace/mcp-servers/company-deal-intelligence)
- **API Docs**: [open.patsnap.com/devportal](https://open.patsnap.com/devportal)
