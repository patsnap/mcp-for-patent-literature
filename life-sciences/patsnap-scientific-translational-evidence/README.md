# Patsnap Scientific & Translational Evidence
**Patsnap Scientific & Translational Evidence** is a Model Context Protocol (MCP) server for life sciences intelligence.

Retrieval platform focusing on scientific literature and translational outcomes, covering academic publication queries and translational medicine record tracking. Built on Patsnap's global life sciences platform, it integrates structured and semantic search across drug, clinical, and biomedical intelligence.

## Quick Links
- [Patsnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [Patsnap Developer Portal](https://open.patsnap.com)
- [Patsnap Scientific & Translational Evidence MCP](https://open.patsnap.com/marketplace/mcp-servers/scientific-translational-evidence)

## Setup
### 1. Get an API Key
Log in to [Patsnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):
```bash
claude mcp add --transport http scientific_translational_evidence \
  "https://connect.patsnap.com/9c333c/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```
Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```
> **Other clients?** Visit the [Scientific & Translational Evidence page on Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/scientific-translational-evidence) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `scientific_translational_evidence` shows **Connected**.

## Available Tools
> **Note for AI Agents:** Each tool below documents its purpose and core parameters. For the complete input schema and constraints, refer to the official MCP server documentation on [Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/scientific-translational-evidence).

### 1. `translational_medicine_search`
- **Purpose**: Search translational medicine information by drug, target, disease, sponsor organization, or publication window.
- **Parameters**:
  - `drug` (array of strings, optional): Drug name list.
  - `target` (array of strings, optional): Target name list.
  - `disease` (array of strings, optional): Disease name list.
  - `organization` (array of strings, optional): Sponsor organization name list.
  - `published_date_from` / `published_date_to` (string, optional): Publication date range. Format: `YYYY-MM-DD`.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with translational medicine records matching the query.
- **API**: `POST /api/ls/v2/translational-medicine/search`
- **Usage**: Use after entity extraction to narrow results to a specific disease area, sponsor, or publication window.

### 2. `translational_medicine_fetch`
- **Purpose**: Batch fetch full detail records by translational medicine IDs.
- **Parameters**:
  - `translational_medicine_ids` (array of strings, required): Translational medicine record ID list in UUID format.
- **Returns**: JSON object with full detail records.
- **API**: `POST /api/ls/v2/translational-medicine/fetch`
- **Usage**: Call after `translational_medicine_search` to retrieve complete record details.

## 💡 **Need help?**
Visit: [Patsnap Life Science](https://eureka.patsnap.com/ls-landing)
or  [Patsnap Dev Portal](https://open.patsnap.com/devportal)

---
## Integration with Patsnap Skills
This server powers the following Patsnap Skills (Claude Code agents):
- **biomarker-investigation**: uses this server's tools to retrieve life science evidence.
- **target-intelligence**: uses this server's tools to retrieve life science evidence.
- **pharmaceuticals-exploration**: uses this server's tools to retrieve life science evidence.

Each Skill automatically invokes the appropriate tools from this server when performing its analyses. You can install the Skills from the [Patsnap Skills Library](https://github.com/patsnap/skills/tree/main/life-sciences).
Or, if you use openclaw:
```bash
openclaw skills install SKILL_NAME
```

## License
MIT

---
Powered by [Patsnap](https://www.patsnap.com). Innovate with Confidence.
