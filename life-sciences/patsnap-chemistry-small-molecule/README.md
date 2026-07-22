# Patsnap Chemistry & Small Molecule
**Patsnap Chemistry & Small Molecule** is a Model Context Protocol (MCP) server for life sciences intelligence.

Intelligent chemical small molecule analysis platform, covering chemical structure search, structure details analysis, and ADMET property prediction. Built on Patsnap's global life sciences platform, it integrates structured and semantic search across drug, clinical, and biomedical intelligence.

## Quick Links
- [Patsnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [Patsnap Developer Portal](https://open.patsnap.com)
- [Patsnap Chemistry & Small Molecule MCP](https://open.patsnap.com/marketplace/mcp-servers/chemistry-small-molecule)

## Setup
### 1. Get an API Key
Log in to [Patsnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):
```bash
claude mcp add --transport http chemistry_small_molecule \
  "https://connect.patsnap.com/f71d33/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```
Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```
> **Other clients?** Visit the [Chemistry & Small Molecule page on Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/chemistry-small-molecule) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `chemistry_small_molecule` shows **Connected**.

## Available Tools
> **Note for AI Agents:** Each tool below documents its purpose and core parameters. For the complete input schema and constraints, refer to the official MCP server documentation on [Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/chemistry-small-molecule).

### 1. `structure_search`
- **Purpose**: Search compounds by chemical structure.
- **Parameters**:
  - `smiles` (string, required): Query structure in SMILES format.
  - `type` (string, required): Search type: `EXT` for exact match, `SIM` for similarity search.
  - `threshold` (number, optional): Similarity threshold, required when `type` is `SIM`.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with compound records matching the structure.
- **API**: `POST /api/ls/v2/structure/search`
- **Usage**: Use to find exact matches or analogs of a lead compound.

### 2. `structure_fetch`
- **Purpose**: Batch fetch full detail records by InChIKey.
- **Parameters**:
  - `inchikeys` (array of strings, required): InChIKey list. Maximum 100 identifiers per request.
- **Returns**: JSON object with full compound detail records.
- **API**: `POST /api/ls/v2/structure/fetch`
- **Usage**: Call after `structure_search` to retrieve detailed structure information.

### 3. `admet_predict`
- **Purpose**: Predict ADMET properties for a list of molecules.
- **Parameters**:
  - `smiles` (array of strings, required): List of SMILES strings. Minimum 1, maximum 100 molecules per request.
- **Returns**: JSON object with ADMET predictions for each input molecule.
- **API**: `POST /api/ls/v2/admet/predict`
- **Usage**: Use for early-stage drug-likeness and pharmacokinetic evaluation.

## 💡 **Need help?**
Visit: [Patsnap Life Science](https://eureka.patsnap.com/ls-landing)
or  [Patsnap Dev Portal](https://open.patsnap.com/devportal)

---
## Integration with Patsnap Skills
This server powers the following Patsnap Skills (Claude Code agents):
- **pharmaceuticals-exploration**: uses this server's tools to retrieve life science evidence.
- **target-intelligence**: uses this server's tools to retrieve life science evidence.

Each Skill automatically invokes the appropriate tools from this server when performing its analyses. You can install the Skills from the [Patsnap Skills Library](https://github.com/patsnap/skills/tree/main/life-sciences).
Or, if you use openclaw:
```bash
openclaw skills install SKILL_NAME
```

## License
MIT

---
Powered by [Patsnap](https://www.patsnap.com). Innovate with Confidence.
