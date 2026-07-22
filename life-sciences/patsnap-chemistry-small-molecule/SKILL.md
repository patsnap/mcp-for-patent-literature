---
name: patsnap-chemistry-small-molecule
description: Patsnap Chemistry & Small Molecule MCP for AI agents. Intelligent chemical small molecule analysis platform, covering chemical structure search, structure details analysis, and ADMET property prediction.
homepage: https://open.patsnap.com/marketplace/mcp-servers/chemistry-small-molecule
metadata:
  author: Patsnap
  category: "Life Science"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/f71d33/logic-mcp?apikey=YOUR_API_KEY"
---
## Setup
Get your API Key at https://open.patsnap.com

# Patsnap Chemistry & Small Molecule

This skill connects your AI agent to **Patsnap's Chemistry & Small Molecule MCP server** — providing professional-grade life sciences intelligence.

Intelligent chemical small molecule analysis platform, covering chemical structure search, structure details analysis, and ADMET property prediction.

## Prerequisites

This skill requires the **Patsnap Chemistry & Small Molecule MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "chemistry_small_molecule": {
      "url": "https://connect.patsnap.com/f71d33/logic-mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).
For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/chemistry-small-molecule

---

## Instructions for AI Agents

### Step 1: Chemical Entity Recognition
When a user mentions a chemical name, drug, or SMILES string, resolve it to a standard structure or identifier.

### Step 2: Structure Search
Use `structure_search` for exact matches or similarity analogs. Fetch full details with `structure_fetch`.

### Step 3: Property Prediction
Use `admet_predict` to evaluate drug-likeness and pharmacokinetic properties.

### Step 4: Output Synthesis
Present SMILES/InChI, scaffold descriptions, and tabular comparisons of analogs.

---

## Example Workflows

### Lead Optimization
1. Run `structure_search` with a lead SMILES.
2. Fetch analog details with `structure_fetch`.
3. Predict ADMET with `admet_predict` to prioritize candidates.

---

## Resources

- **Patsnap Life Sciences**: [eureka.patsnap.com/ls-landing](https://eureka.patsnap.com/ls-landing)
- **MCP Server**: [open.patsnap.com/marketplace/mcp-servers](https://open.patsnap.com/marketplace/mcp-servers/chemistry-small-molecule)
- **API Docs**: [open.patsnap.com/devportal](https://open.patsnap.com/devportal)
