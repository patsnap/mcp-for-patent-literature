# PatSnap Chemical Molecular

**PatSnap Chemical Molecular** is a Model Context Protocol (MCP) server that equips AI agents with chemical intelligence capabilities, covering compound structure search, fragment analysis, and ADMET property prediction. Built on PatSnap's global life sciences platform, it accelerates molecular evaluation and lead optimization in early-stage drug discovery.

## Quick Links
- [PatSnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [PatSnap Developer Portal](https://open.patsnap.com)
- [PatSnap Biology Modality MCP](https://open.patsnap.com/marketplace/mcp-servers/chemical-molecular)

## Setup

### 1. Get an API Key
Log in to [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):

```bash
claude mcp add --transport http chemical_molecular \
  "https://connect.patsnap.com/713886/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```

Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```

> **Other clients?** Visit the [Chemical Molecular page on PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/chemical-molecular) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `chemical_molecular` shows **Connected**.

## Available Tools

> **Note for AI Agents:** Each tool below documents its exact parameters, types, and constraints as shown in the official PatSnap Marketplace. Pay close attention to required vs. optional parameters.

### 1. `ls_chemical_search`
- **Purpose**: Search compounds by chemical structure, supporting both exact match and similarity search against PatSnap's chemical database.
- **Parameters**:
  - `smiles` (string, required): Query structure in SMILES format. Example: `"CC(=O)OC1=C(C=CC=C1)C(O)=O"`.
  - `type` (string, required): Search type: `"EXT"` for exact match, `"SIM"` for similarity search.
  - `threshold` (number, optional): Similarity threshold, required when `type` is `"SIM"`. Example: `0.99`.
  - `include_tautomer` (boolean, optional): Whether to include tautomers in results.
  - `include_isotope` (boolean, optional): Whether to include isotope variants.
  - `include_charge` (boolean, optional): Whether to include charge variants.
  - `include_stereo` (boolean, optional): Whether to include stereoisomers.
  - `include_radical` (boolean, optional): Whether to include radical variants.
  - `include_multi_component` (boolean, optional): Whether to include multi-component compounds. Valid for `"EXT"` type only.
  - `offset` (integer, optional): Pagination offset, starting from 0.
  - `limit` (integer, optional): Page size. Example: `20`.
- **Returns**: JSON object with `total_hits` (integer) and `results` (array of compound records with SMILES, identifiers, and match details).
- **API**: `POST /api/ls/chemical/search`
- **Usage**: Use `"EXT"` to find exact compound matches across the database. Use `"SIM"` with a `threshold` to find structurally similar molecules for lead hopping or SAR studies.

### 2. `ls_chemical_mcs_analyze`
- **Purpose**: Analyze fragment composition across multiple chemical structures, identifying common scaffolds and fragment distribution frequencies.
- **Parameters**:
  - `structures` (array of strings, required): List of SMILES structures to analyze. Must contain at least one valid SMILES string. Example: `["CCO", "CC(C)O", "c1ccccc1"]`.
- **Returns**: JSON object containing fragment analysis results with identified common substructures and their occurrence frequencies across the input set.
- **API**: `POST /api/ls/chemical/mcs/analyze`
- **Usage**: Use when comparing a set of active compounds to identify conserved pharmacophores or recurring structural motifs.

### 3. `ls_admet_predict`
- **Purpose**: Predict ADMET (Absorption, Distribution, Metabolism, Excretion, Toxicity) properties for a batch of small molecules using the ADMET-AI model.
- **Parameters**:
  - `smiles` (array of strings, required): List of SMILES molecular formula strings. Minimum 1, maximum 100 molecules per request. Example: `["CC(=O)Oc1ccccc1C(=O)O"]`.
- **Returns**: JSON object with predictions for each input molecule, including absorption, distribution, metabolism, excretion, and toxicity property scores.
- **API**: `POST /api/ls/admet/predict`
- **Usage**: Use for early-stage drug-likeness evaluation, filtering virtual screening hits, or prioritizing candidates before synthesis.

## 💡 **Need help?**
Visit: [PatSnap Life Science](https://eureka.patsnap.com/ls-landing) 
or  [PatSnap Dev Portal](https://open.patsnap.com/devportal)

---

## Integration with PatSnap Skills
This server powers the chemical intelligence layer for the following PatSnap Skills (Claude Code agents):
- **pharmaceuticals-exploration**: uses chemical structure search and ADMET prediction to evaluate drug candidates and explore molecular properties.

Each Skill automatically invokes the appropriate tools from this server when performing its analyses. You can install the Skills from the [PatSnap Skills Library](https://github.com/patsnap/skills/tree/main/life-sciences).
Or, if you use openclaw:
```bash
openclaw skills install SKILL_NAME
```

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com). Innovate with Confidence.
