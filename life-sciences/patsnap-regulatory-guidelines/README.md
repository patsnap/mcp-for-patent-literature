# Patsnap Regulatory & Guidelines
**Patsnap Regulatory & Guidelines** is a Model Context Protocol (MCP) server for life sciences intelligence.

Evidence query tool for regulatory policies and clinical norms, covering semantic evidence retrieval for clinical guidelines and FDA drug labels. Built on Patsnap's global life sciences platform, it integrates structured and semantic search across drug, clinical, and biomedical intelligence.

## Quick Links
- [Patsnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [Patsnap Developer Portal](https://open.patsnap.com)
- [Patsnap Regulatory & Guidelines MCP](https://open.patsnap.com/marketplace/mcp-servers/regulatory-guidelines)

## Setup
### 1. Get an API Key
Log in to [Patsnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):
```bash
claude mcp add --transport http regulatory_guidelines \
  "https://connect.patsnap.com/6415c2/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```
Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```
> **Other clients?** Visit the [Regulatory & Guidelines page on Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/regulatory-guidelines) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `regulatory_guidelines` shows **Connected**.

## Available Tools
> **Note for AI Agents:** Each tool below documents its purpose and core parameters. For the complete input schema and constraints, refer to the official MCP server documentation on [Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/regulatory-guidelines).

### 1. `fda_label_search`
- **Purpose**: Search FDA drug labels with vector similarity.
- **Parameters**:
  - `query` (string, required): Natural-language query describing the label evidence needed.
  - `drug` (array of strings, optional): Drug name list to constrain results.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with relevant FDA label text chunks and similarity scores.
- **API**: `POST /api/ls/v2/fda-label/search`
- **Usage**: Use for questions such as 'What are the boxed warnings for pembrolizumab?'.

### 2. `clinical_guideline_search`
- **Purpose**: Search clinical guidelines with vector similarity.
- **Parameters**:
  - `query` (string, required): Natural-language query describing the guideline evidence needed.
  - `disease` (array of strings, optional): Disease name list to constrain results.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with relevant clinical guideline text chunks and similarity scores.
- **API**: `POST /api/ls/v2/clinical-guideline/search`
- **Usage**: Use for questions such as 'What is the first-line treatment for EGFR-mutant NSCLC?'.

## 💡 **Need help?**
Visit: [Patsnap Life Science](https://eureka.patsnap.com/ls-landing)
or  [Patsnap Dev Portal](https://open.patsnap.com/devportal)

---
## Integration with Patsnap Skills
This server powers the following Patsnap Skills (Claude Code agents):
- **disease-investigation**: uses this server's tools to retrieve life science evidence.
- **precision-oncology**: uses this server's tools to retrieve life science evidence.
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
