# PatSnap Life Sciences MCP Servers
> by [PatSnap Life Sciences](https://eureka.patsnap.com/ls-landing)

Official Model Context Protocol (MCP) servers for Life Sciences, powered by PatSnap's proprietary biomedical and pharmaceutical intelligence platform. These servers give AI agents direct, structured access to comprehensive drug, target, disease, clinical trial, patent, scientific literature, biological sequence, chemical structure, and real-world evidence data.

## Available MCP Servers

| Server | Focus | Tools | Quick Link |
| --- | --- | --- | --- |
| **Pharma Intelligence** | Drugs, targets, diseases, clinical trials, patents, papers, deals, FDA labels, epidemiology, HEOR, financial reports, news, translational medicine | 28 | [Pharma Intelligence](https://open.patsnap.com/marketplace/mcp-servers/pharma-intelligence) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-pharma-intelligence) |
| **Biology Modality** | Biological sequences, modifications, antibody-antigen interactions | 5 | [Biology Modality](https://open.patsnap.com/marketplace/mcp-servers/biology-modality) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-biology-modality) |
| **Chemical Molecular** | Compound structure search, fragment analysis, ADMET prediction | 3 | [Chemical Molecular](https://open.patsnap.com/marketplace/mcp-servers/chemical-molecular) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-chemical-molecular) |
| **Target & Disease** | Target characterization, disease profiling, epidemiology evidence | 3 | [Target & Disease](https://open.patsnap.com/marketplace/mcp-servers/target-disease) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-target-disease) |
| **Scientific & Translational Evidence** | Translational medicine records and academic publication evidence | 2 | [Scientific & Translational Evidence](https://open.patsnap.com/marketplace/mcp-servers/scientific-translational-evidence) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-scientific-translational-evidence) |
| **Regulatory & Guidelines** | Clinical guidelines and FDA drug label semantic search | 2 | [Regulatory & Guidelines](https://open.patsnap.com/marketplace/mcp-servers/regulatory-guidelines) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-regulatory-guidelines) |
| **Drug & Asset** | Drug search, details, and development milestone tracking | 3 | [Drug & Asset](https://open.patsnap.com/marketplace/mcp-servers/drug-asset) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-drug-asset) |
| **Current Awareness** | Global medical news search and full-article fetch | 2 | [Current Awareness](https://open.patsnap.com/marketplace/mcp-servers/current-awareness) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-current-awareness) |
| **Company & Deal Intelligence** | Organization profiles, pipelines, deals, financial reports | 5 | [Company & Deal Intelligence](https://open.patsnap.com/marketplace/mcp-servers/company-deal-intelligence) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-company-deal-intelligence) |
| **Clinical Trials** | Registered trial tracking, results, and clinical semantic search | 4 | [Clinical Trials](https://open.patsnap.com/marketplace/mcp-servers/clinical-trials) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-clinical-trials) |
| **Chemistry & Small Molecule** | Chemical structure search, structure details, ADMET prediction | 3 | [Chemistry & Small Molecule](https://open.patsnap.com/marketplace/mcp-servers/chemistry-small-molecule) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-chemistry-small-molecule) |
| **Biologics & Sequence** | Biological sequence search, alignment, modification, antibody discovery | 7 | [Biologics & Sequence](https://open.patsnap.com/marketplace/mcp-servers/biologics-sequence) Or [Repo](https://github.com/patsnap/mcp/tree/main/life-sciences/patsnap-biologics-sequence) |

## Setup

All servers follow the same three-step pattern. You can connect one or all of them depending on your use case.

### 1. Get an API Key
Log in to the [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Servers
Run the following commands in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):

```bash
# Pharma Intelligence
claude mcp add --transport http pharma_intelligence \
  "https://connect.patsnap.com/096456/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Biology Modality
claude mcp add --transport http biology_modality \
  "https://connect.patsnap.com/06e741/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Chemical Molecular
claude mcp add --transport http chemical_molecular \
  "https://connect.patsnap.com/713886/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Target & Disease
claude mcp add --transport http target_disease \
  "https://connect.patsnap.com/2a2645/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Scientific & Translational Evidence
claude mcp add --transport http scientific_translational_evidence \
  "https://connect.patsnap.com/9c333c/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Regulatory & Guidelines
claude mcp add --transport http regulatory_guidelines \
  "https://connect.patsnap.com/6415c2/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Drug & Asset
claude mcp add --transport http drug_asset \
  "https://connect.patsnap.com/30cd71/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Current Awareness
claude mcp add --transport http current_awareness \
  "https://connect.patsnap.com/401c6d/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Company & Deal Intelligence
claude mcp add --transport http company_deal_intelligence \
  "https://connect.patsnap.com/1f8934/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Clinical Trials
claude mcp add --transport http clinical_trials \
  "https://connect.patsnap.com/051cd3/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Chemistry & Small Molecule
claude mcp add --transport http chemistry_small_molecule \
  "https://connect.patsnap.com/f71d33/Logic-mcp?apiKey=$PATSNAP_API_KEY"

# Biologics & Sequence
claude mcp add --transport http biologics_sequence \
  "https://connect.patsnap.com/ab57ab/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```

Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```

> **Other clients?** Visit the individual server pages on [PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm that the added servers show **Connected**.

## PatSnap Skills Integration

These MCP servers power [PatSnap Skills](https://github.com/patsnap/skills/tree/main/life-sciences), domain-specific AI agents purpose-built for common life sciences workflows. Install them directly into your AI agent for turnkey analysis capabilities.

| Skill | Description | Requires |
|---|---|---|
| **target-intelligence** | Comprehensive target evaluation including tractability, competitive landscape, and biology evidence | Target & Disease, Biologics & Sequence, Pharma Intelligence |
| **pharmaceuticals-exploration** | Drug candidate assessment covering structure-activity, clinical properties, and development progress | Drug & Asset, Clinical Trials, Chemistry & Small Molecule, Pharma Intelligence |
| **biomarker-investigation** | Biomarker discovery, validation, and clinical utility analysis across disease areas | Scientific & Translational Evidence, Pharma Intelligence |
| **disease-investigation** | Disease landscape characterization including epidemiology, pipeline, and standard of care | Target & Disease, Clinical Trials, Regulatory & Guidelines, Pharma Intelligence |
| **company-profiling** | In-depth company analysis covering pipeline, portfolio, partnerships, and patent strategy | Company & Deal Intelligence, Current Awareness, Pharma Intelligence |
| **precision-oncology** | Precision medicine insights for oncology including targeted therapies and biomarker-matched trials | Target & Disease, Clinical Trials, Pharma Intelligence |

To install all skills:
```bash
npx skills add https://github.com/patsnap/skills/tree/main/life-sciences --all
```

## Resources

- [PatSnap Developer Portal](https://open.patsnap.com): manage API keys and explore available services
- [PatSnap MCP Marketplace](https://open.patsnap.com/marketplace/mcp-servers): full list of available MCP servers
- [PatSnap Life Sciences](https://eureka.patsnap.com/ls-landing): learn more about PatSnap's life sciences platform
- [PatSnap Skills Library](https://github.com/patsnap/skills): installable domain-specific AI agent skills
- [PatSnap MCP Server Source](https://github.com/patsnap/mcp): source code for all MCP servers

## License

MIT

---
Powered by [PatSnap](https://www.patsnap.com). Innovate with Confidence.
