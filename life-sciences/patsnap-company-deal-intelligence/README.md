# PatSnap Company & Deal Intelligence
**PatSnap Company & Deal Intelligence** is a Model Context Protocol (MCP) server for life sciences intelligence.

Intangible asset and commercial intelligence archive tool for pharmaceutical enterprises, covering organization profiles, R&D pipelines, deal records, and financial report evidence queries. Built on PatSnap's global life sciences platform, it integrates structured and semantic search across drug, clinical, and biomedical intelligence.

## Quick Links
- [PatSnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [PatSnap Developer Portal](https://open.patsnap.com)
- [PatSnap Company & Deal Intelligence MCP](https://open.patsnap.com/marketplace/mcp-servers/company-deal-intelligence)

## Setup
### 1. Get an API Key
Log in to [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):
```bash
claude mcp add --transport http company_deal_intelligence \
  "https://connect.patsnap.com/1f8934/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```
Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```
> **Other clients?** Visit the [Company & Deal Intelligence page on PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/company-deal-intelligence) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `company_deal_intelligence` shows **Connected**.

## Available Tools
> **Note for AI Agents:** Each tool below documents its purpose and core parameters. For the complete input schema and constraints, refer to the official MCP server documentation on [PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/company-deal-intelligence).

### 1. `organization_fetch`
- **Purpose**: Batch fetch full detail records by organization IDs or organization names.
- **Parameters**:
  - `organization_ids` (array of strings, optional): Organization ID list in UUID format.
  - `organization` (array of strings, optional): Organization name list.
- **Returns**: JSON object with full organization profiles.
- **API**: `POST /api/ls/v2/organization/fetch`
- **Usage**: Use to retrieve company background, pipeline overview, and portfolio details.

### 2. `organization_pipeline_fetch`
- **Purpose**: Fetch drug pipeline records for an organization.
- **Parameters**:
  - `organization_id` (string, optional): Organization ID in UUID format.
  - `organization` (string, optional): Organization name. Must provide exactly one of `organization_id` or `organization`.
- **Returns**: JSON object with pipeline assets for the organization.
- **API**: `POST /api/ls/v2/organization/pipeline/fetch`
- **Usage**: Use when the user asks about a company's R&D pipeline.

### 3. `drug_deal_search`
- **Purpose**: Search drug deal information such as licensing, collaboration, acquisition, or option deals.
- **Parameters**:
  - `drug` (array of strings, optional): Drug name list.
  - `target` (array of strings, optional): Target name list.
  - `disease` (array of strings, optional): Disease name list.
  - `organization` (array of strings, optional): Company name list.
  - `deal_type` (array of strings, optional): Deal type filter.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with deal records.
- **API**: `POST /api/ls/v2/drug-deal/search`
- **Usage**: Use for BD queries such as 'ADC licensing deals in US after 2021'.

### 4. `drug_deal_fetch`
- **Purpose**: Batch fetch full detail records by drug deal IDs.
- **Parameters**:
  - `deal_ids` (array of strings, required): Drug deal ID list in UUID format.
- **Returns**: JSON object with full deal details.
- **API**: `POST /api/ls/v2/drug-deal/fetch`
- **Usage**: Call after `drug_deal_search` to retrieve complete deal terms and parties.

### 5. `financial_report_search`
- **Purpose**: Search financial reports and prospectuses with vector similarity.
- **Parameters**:
  - `query` (string, required): Natural-language query describing the financial evidence needed.
  - `organization` (array of strings, optional): Organization name list.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with relevant financial report text chunks.
- **API**: `POST /api/ls/v2/financial-report/search`
- **Usage**: Use for questions such as 'What did the company report about its oncology revenue?'.

## 💡 **Need help?**
Visit: [PatSnap Life Science](https://eureka.patsnap.com/ls-landing)
or  [PatSnap Dev Portal](https://open.patsnap.com/devportal)

---
## Integration with PatSnap Skills
This server powers the following PatSnap Skills (Claude Code agents):
- **company-profiling**: uses this server's tools to retrieve life science evidence.
- **pharmaceuticals-exploration**: uses this server's tools to retrieve life science evidence.
- **target-intelligence**: uses this server's tools to retrieve life science evidence.

Each Skill automatically invokes the appropriate tools from this server when performing its analyses. You can install the Skills from the [PatSnap Skills Library](https://github.com/patsnap/skills/tree/main/life-sciences).
Or, if you use openclaw:
```bash
openclaw skills install SKILL_NAME
```

## License
MIT

---
Powered by [PatSnap](https://www.patsnap.com). Innovate with Confidence.
