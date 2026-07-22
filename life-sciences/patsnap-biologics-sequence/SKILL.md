---
name: patsnap-biologics-sequence
description: Patsnap Biologics & Sequence MCP for AI agents. Intelligent platform for biological sequences and macromolecules, covering antibody-antigen interaction discovery, full-lifecycle sequence search, sequence fetching and alignment, and modification status analysis.
homepage: https://open.patsnap.com/marketplace/mcp-servers/biologics-sequence
metadata:
  author: Patsnap
  category: "Life Science"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/ab57ab/logic-mcp?apikey=YOUR_API_KEY"
---
## Setup
Get your API Key at https://open.patsnap.com

# Patsnap Biologics & Sequence

This skill connects your AI agent to **Patsnap's Biologics & Sequence MCP server** — providing professional-grade life sciences intelligence.

Intelligent platform for biological sequences and macromolecules, covering antibody-antigen interaction discovery, full-lifecycle sequence search, sequence fetching and alignment, and modification status analysis.

## Prerequisites

This skill requires the **Patsnap Biologics & Sequence MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "biologics_sequence": {
      "url": "https://connect.patsnap.com/ab57ab/logic-mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).
For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/biologics-sequence

---

## Instructions for AI Agents

### Step 1: Sequence Identification
When a user provides a protein or nucleotide sequence or a gene name, normalize the entity to a standard ID or sequence before searching.

### Step 2: Submit Asynchronous Searches
For `sequence_search_submit` and `modification_search_submit`, capture the returned `job_id` and poll `sequence_search_check_status` until `status` is `success` before fetching results.

### Step 3: Fetch and Analyze
Use `sequence_search_get_results`, `sequence_fetch`, or `sequence_alignment` to retrieve and compare records. For antibody discovery, use `antibody_antigen_search` directly.

### Step 4: Output Synthesis
Present sequence data with alignments, functional annotations, and IP landscape summaries.

---

## Example Workflows

### Antibody FTO Check
1. Submit `sequence_search_submit` with the antibody sequence.
2. Poll `sequence_search_check_status` until success.
3. Fetch results and assess high-identity patents.

### Antibody Discovery
1. Use `antibody_antigen_search` for antibodies against a target antigen.
2. Fetch sequences with `sequence_fetch`.
3. Align candidates with `sequence_alignment`.

---

## Resources

- **Patsnap Life Sciences**: [eureka.patsnap.com/ls-landing](https://eureka.patsnap.com/ls-landing)
- **MCP Server**: [open.patsnap.com/marketplace/mcp-servers](https://open.patsnap.com/marketplace/mcp-servers/biologics-sequence)
- **API Docs**: [open.patsnap.com/devportal](https://open.patsnap.com/devportal)
