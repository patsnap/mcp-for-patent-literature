# PatSnap Current Awareness
**PatSnap Current Awareness** is a Model Context Protocol (MCP) server for life sciences intelligence.

Tracking system for pharmaceutical industry dynamics and cutting-edge news, covering global medical news search and in-depth news detail mining. Built on PatSnap's global life sciences platform, it integrates structured and semantic search across drug, clinical, and biomedical intelligence.

## Quick Links
- [PatSnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [PatSnap Developer Portal](https://open.patsnap.com)
- [PatSnap Current Awareness MCP](https://open.patsnap.com/marketplace/mcp-servers/current-awareness)

## Setup
### 1. Get an API Key
Log in to [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):
```bash
claude mcp add --transport http current_awareness \
  "https://connect.patsnap.com/401c6d/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```
Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```
> **Other clients?** Visit the [Current Awareness page on PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/current-awareness) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `current_awareness` shows **Connected**.

## Available Tools
> **Note for AI Agents:** Each tool below documents its purpose and core parameters. For the complete input schema and constraints, refer to the official MCP server documentation on [PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/current-awareness).

### 1. `news_search`
- **Purpose**: Search news with vector similarity.
- **Parameters**:
  - `query` (string, required): Natural-language query describing the news topic.
  - `drug` (array of strings, optional): Drug name list.
  - `target` (array of strings, optional): Target name list.
  - `disease` (array of strings, optional): Disease name list.
  - `organization` (array of strings, optional): Organization name list.
  - `published_date_from` / `published_date_to` (string, optional): Publication date range.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with relevant news text chunks and similarity scores.
- **API**: `POST /api/ls/v2/news/search`
- **Usage**: Use for natural-language queries such as 'latest approvals for KRAS inhibitors'.

### 2. `news_fetch`
- **Purpose**: Batch fetch full detail records by news IDs.
- **Parameters**:
  - `news_ids` (array of strings, required): News ID list in UUID format.
- **Returns**: JSON object with full news articles.
- **API**: `POST /api/ls/v2/news/fetch`
- **Usage**: Call after `news_search` to retrieve the complete article content.

## 💡 **Need help?**
Visit: [PatSnap Life Science](https://eureka.patsnap.com/ls-landing)
or  [PatSnap Dev Portal](https://open.patsnap.com/devportal)

---
## Integration with PatSnap Skills
This server powers the following PatSnap Skills (Claude Code agents):
- **company-profiling**: uses this server's tools to retrieve life science evidence.
- **pharmaceuticals-exploration**: uses this server's tools to retrieve life science evidence.
- **disease-investigation**: uses this server's tools to retrieve life science evidence.

Each Skill automatically invokes the appropriate tools from this server when performing its analyses. You can install the Skills from the [PatSnap Skills Library](https://github.com/patsnap/skills/tree/main/life-sciences).
Or, if you use openclaw:
```bash
openclaw skills install SKILL_NAME
```

## License
MIT

---
Powered by [PatSnap](https://www.patsnap.com). Innovate with Confidence.
