# PatSnap Drug & Asset
**PatSnap Drug & Asset** is a Model Context Protocol (MCP) server for life sciences intelligence.

Drug and asset intelligence retrieval platform, covering drug search, drug details analysis, and development milestone tracking. Built on PatSnap's global life sciences platform, it integrates structured and semantic search across drug, clinical, and biomedical intelligence.

## Quick Links
- [PatSnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [PatSnap Developer Portal](https://open.patsnap.com)
- [PatSnap Drug & Asset MCP](https://open.patsnap.com/marketplace/mcp-servers/drug-asset)

## Setup
### 1. Get an API Key
Log in to [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):
```bash
claude mcp add --transport http drug_asset \
  "https://connect.patsnap.com/30cd71/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```
Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```
> **Other clients?** Visit the [Drug & Asset page on PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/drug-asset) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `drug_asset` shows **Connected**.

## Available Tools
> **Note for AI Agents:** Each tool below documents its purpose and core parameters. For the complete input schema and constraints, refer to the official MCP server documentation on [PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/drug-asset).

### 1. `drug_search`
- **Purpose**: Search drug assets by drug name, target, disease, organization, development phase, or milestone date.
- **Parameters**:
  - `drug` (array of strings, optional): Drug name list.
  - `target` (array of strings, optional): Target name list.
  - `disease` (array of strings, optional): Disease name list.
  - `organization` (array of strings, optional): Organization name list.
  - `highest_phase` (array of strings, optional): Development phase filter such as `discovery`, `preclinical`, `phase_1`, `phase_2`, `phase_3`, `approved`.
  - `country` (array of strings, optional): Country or region code list.
  - `key_word` (array of strings, optional): Free-text keyword for broad matching.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with `total_hits` and an array of drug records.
- **API**: `POST /api/ls/v2/drug/search`
- **Usage**: Use for structured pipeline filtering such as 'PD-1 drugs in Phase 3 in China'.

### 2. `drug_fetch`
- **Purpose**: Batch fetch full detail records by drug IDs or drug names.
- **Parameters**:
  - `drug_ids` (array of strings, optional): Drug ID list in UUID format.
  - `drug` (array of strings, optional): Drug name list.
- **Returns**: JSON object with full detail records for the requested drugs.
- **API**: `POST /api/ls/v2/drug/fetch`
- **Usage**: Call after `drug_search` to retrieve complete drug information.

### 3. `drug_milestone_fetch`
- **Purpose**: Fetch drug R&D milestone history records (timeline) for a specific drug.
- **Parameters**:
  - `drug_id` (string, optional): Drug ID in UUID format.
  - `drug` (string, optional): Drug name. Either `drug_id` or `drug` must be provided.
- **Returns**: JSON object with milestone events such as IND, Phase transitions, and approvals.
- **API**: `POST /api/ls/v2/drug/milestone/fetch`
- **Usage**: Use when the user asks about a drug's development history or key milestones.

## 💡 **Need help?**
Visit: [PatSnap Life Science](https://eureka.patsnap.com/ls-landing)
or  [PatSnap Dev Portal](https://open.patsnap.com/devportal)

---
## Integration with PatSnap Skills
This server powers the following PatSnap Skills (Claude Code agents):
- **pharmaceuticals-exploration**: uses this server's tools to retrieve life science evidence.
- **company-profiling**: uses this server's tools to retrieve life science evidence.
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
