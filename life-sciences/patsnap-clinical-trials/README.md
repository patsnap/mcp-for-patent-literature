# PatSnap Clinical Trials
**PatSnap Clinical Trials** is a Model Context Protocol (MCP) server for life sciences intelligence.

Intelligent clinical trial retrieval system, covering registered trial tracking, trial details and results analysis, and supporting clinical semantic search. Built on PatSnap's global life sciences platform, it integrates structured and semantic search across drug, clinical, and biomedical intelligence.

## Quick Links
- [PatSnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [PatSnap Developer Portal](https://open.patsnap.com)
- [PatSnap Clinical Trials MCP](https://open.patsnap.com/marketplace/mcp-servers/clinical-trials)

## Setup
### 1. Get an API Key
Log in to [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):
```bash
claude mcp add --transport http clinical_trials \
  "https://connect.patsnap.com/051cd3/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```
Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```
> **Other clients?** Visit the [Clinical Trials page on PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/clinical-trials) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `clinical_trials` shows **Connected**.

## Available Tools
> **Note for AI Agents:** Each tool below documents its purpose and core parameters. For the complete input schema and constraints, refer to the official MCP server documentation on [PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/clinical-trials).

### 1. `clinical_trial_search`
- **Purpose**: Search registered clinical trials by study drug, control drug, target, disease, sponsor, phase, or geography.
- **Parameters**:
  - `drug` (array of strings, optional): Main study drug name list.
  - `control_drug` (array of strings, optional): Control drug name list.
  - `target` (array of strings, optional): Target name list.
  - `disease` (array of strings, optional): Disease name list.
  - `organization` (array of strings, optional): Sponsor organization name list.
  - `phase` (array of strings, optional): Clinical phase filter.
  - `study_status` (array of strings, optional): Trial status filter.
  - `country` (array of strings, optional): Country or region code list.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with trial records.
- **API**: `POST /api/ls/v2/clinical-trial/search`
- **Usage**: Use for structured trial filtering such as 'Phase 2 EGFR trials in US'.

### 2. `clinical_trial_fetch`
- **Purpose**: Batch fetch full detail records by clinical trial IDs or registration numbers.
- **Parameters**:
  - `trial_ids` (array of strings, optional): Clinical trial ID list in UUID format.
  - `registration_number` (array of strings, optional): Registration number list such as NCT numbers.
- **Returns**: JSON object with full trial details.
- **API**: `POST /api/ls/v2/clinical-trial/fetch`
- **Usage**: Call after `clinical_trial_search` to retrieve complete trial information.

### 3. `clinical_trial_result_search`
- **Purpose**: Search published or indexed clinical trial results by drug, target, disease, sponsor, phase, or evaluation outcome.
- **Parameters**:
  - `drug` (array of strings, optional): Main study drug name list.
  - `target` (array of strings, optional): Target name list.
  - `disease` (array of strings, optional): Disease name list.
  - `phase` (array of strings, optional): Clinical phase filter.
  - `general_evaluation` (array of strings, optional): Overall trial evaluation filter.
  - `published_date_from` / `published_date_to` (string, optional): Result publication date range.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with clinical trial result records.
- **API**: `POST /api/ls/v2/clinical-trial-result/search`
- **Usage**: Use for result-centric questions such as 'Phase 3 PD-1 trial results in melanoma'.

### 4. `clinical_trial_result_fetch`
- **Purpose**: Batch fetch full detail records by clinical trial result IDs.
- **Parameters**:
  - `result_ids` (array of strings, required): Clinical trial result ID list in UUID format.
- **Returns**: JSON object with full trial result details.
- **API**: `POST /api/ls/v2/clinical-trial-result/fetch`
- **Usage**: Call after `clinical_trial_result_search` to retrieve complete result data.

## 💡 **Need help?**
Visit: [PatSnap Life Science](https://eureka.patsnap.com/ls-landing)
or  [PatSnap Dev Portal](https://open.patsnap.com/devportal)

---
## Integration with PatSnap Skills
This server powers the following PatSnap Skills (Claude Code agents):
- **pharmaceuticals-exploration**: uses this server's tools to retrieve life science evidence.
- **precision-oncology**: uses this server's tools to retrieve life science evidence.
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
