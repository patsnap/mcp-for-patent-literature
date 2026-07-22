# Patsnap Target & Disease
**Patsnap Target & Disease** is a Model Context Protocol (MCP) server for life sciences intelligence.

Target and disease profiling tool, covering target characterization, disease profiling, and epidemiology evidence retrieval. Built on Patsnap's global life sciences platform, it integrates structured and semantic search across drug, clinical, and biomedical intelligence.

## Quick Links
- [Patsnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [Patsnap Developer Portal](https://open.patsnap.com)
- [Patsnap Target & Disease MCP](https://open.patsnap.com/marketplace/mcp-servers/target-disease)

## Setup
### 1. Get an API Key
Log in to [Patsnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):
```bash
claude mcp add --transport http target_disease \
  "https://connect.patsnap.com/2a2645/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```
Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```
> **Other clients?** Visit the [Target & Disease page on Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/target-disease) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `target_disease` shows **Connected**.

## Available Tools
> **Note for AI Agents:** Each tool below documents its purpose and core parameters. For the complete input schema and constraints, refer to the official MCP server documentation on [Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/target-disease).

### 1. `target_fetch`
- **Purpose**: Batch fetch full detail records by target IDs or target names.
- **Parameters**:
  - `target_ids` (array of strings, optional): Target ID list in UUID format.
  - `target` (array of strings, optional): Target name list. Names are resolved to IDs before fetching.
- **Returns**: JSON object with full detail records for the requested targets.
- **API**: `POST /api/ls/v2/target/fetch`
- **Usage**: Call after a search or when the user asks for details on a specific target.

### 2. `disease_fetch`
- **Purpose**: Batch fetch full detail records by disease IDs or disease names.
- **Parameters**:
  - `disease_ids` (array of strings, optional): Disease ID list in UUID format.
  - `disease` (array of strings, optional): Disease name list. Names are resolved to IDs before fetching.
- **Returns**: JSON object with full detail records for the requested diseases.
- **API**: `POST /api/ls/v2/disease/fetch`
- **Usage**: Use to retrieve disease mechanisms, epidemiology, and standard-of-care details.

### 3. `epidemiology_search`
- **Purpose**: Search epidemiology data with vector similarity. Use semantic similarity to search epidemiology content.
- **Parameters**:
  - `query` (string, required): Natural-language search query describing the epidemiology evidence needed.
  - `offset` (integer, optional): Pagination offset, starting from 0.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with relevant text chunks and similarity scores.
- **API**: `POST /api/ls/v2/epidemiology/search`
- **Usage**: Use for complex natural-language queries such as 'prevalence of NASH in the United States'.

## 💡 **Need help?**
Visit: [Patsnap Life Science](https://eureka.patsnap.com/ls-landing)
or  [Patsnap Dev Portal](https://open.patsnap.com/devportal)

---
## Integration with Patsnap Skills
This server powers the following Patsnap Skills (Claude Code agents):
- **target-intelligence**: uses this server's tools to retrieve life science evidence.
- **disease-investigation**: uses this server's tools to retrieve life science evidence.
- **precision-oncology**: uses this server's tools to retrieve life science evidence.

Each Skill automatically invokes the appropriate tools from this server when performing its analyses. You can install the Skills from the [Patsnap Skills Library](https://github.com/patsnap/skills/tree/main/life-sciences).
Or, if you use openclaw:
```bash
openclaw skills install SKILL_NAME
```

## License
MIT

---
Powered by [Patsnap](https://www.patsnap.com). Innovate with Confidence.
