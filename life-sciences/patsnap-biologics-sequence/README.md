# Patsnap Biologics & Sequence
**Patsnap Biologics & Sequence** is a Model Context Protocol (MCP) server for life sciences intelligence.

Intelligent platform for biological sequences and macromolecules, covering antibody-antigen interaction discovery, full-lifecycle sequence search, sequence fetching and alignment, and modification status analysis. Built on Patsnap's global life sciences platform, it integrates structured and semantic search across drug, clinical, and biomedical intelligence.

## Quick Links
- [Patsnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [Patsnap Developer Portal](https://open.patsnap.com)
- [Patsnap Biologics & Sequence MCP](https://open.patsnap.com/marketplace/mcp-servers/biologics-sequence)

## Setup
### 1. Get an API Key
Log in to [Patsnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):
```bash
claude mcp add --transport http biologics_sequence \
  "https://connect.patsnap.com/ab57ab/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```
Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=sk-your-key-here
```
> **Other clients?** Visit the [Biologics & Sequence page on Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/biologics-sequence) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `biologics_sequence` shows **Connected**.

## Available Tools
> **Note for AI Agents:** Each tool below documents its purpose and core parameters. For the complete input schema and constraints, refer to the official MCP server documentation on [Patsnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/biologics-sequence).

### 1. `sequence_search_submit`
- **Purpose**: Submit a bio sequence search job.
- **Parameters**:
  - `query_type` (string, required): Target sequence type. One of `NUCLEOTIDE` or `PROTEIN`.
  - `sequence` (string, required): Single query sequence string.
  - `sequence_type` (string, required): Type of the query sequence. One of `NUCLEOTIDE` or `PROTEIN`.
  - `database` (array of strings, optional): Target database list such as `ALLPATENT`, `CLAIMS`.
  - `limit` (integer, optional): Maximum number of results returned internally.
- **Returns**: JSON object with `job_id`, `status`, and `submitted_at`.
- **API**: `POST /api/ls/v2/sequence/search/submit`
- **Usage**: Use to initiate a similarity search. Then poll status and fetch results.

### 2. `sequence_search_check_status`
- **Purpose**: Check the current status of a submitted sequence or modification search job.
- **Parameters**:
  - `job_id` (string, required): Backend search job ID.
- **Returns**: JSON object with `job_id`, `status`, `progress`, and optional `message`.
- **API**: `GET /api/ls/v2/sequence/search/status`
- **Usage**: Poll until `status` becomes `success` before fetching results.

### 3. `sequence_search_get_results`
- **Purpose**: Fetch the final results of a completed sequence or modification search job.
- **Parameters**:
  - `job_id` (string, required): Backend search job ID.
  - `offset` (integer, optional): Result offset for pagination.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with matching sequence records.
- **API**: `GET /api/ls/v2/sequence/search/results`
- **Usage**: Call only after the job status is `success`.

### 4. `sequence_fetch`
- **Purpose**: Batch fetch full detail records by sequence number.
- **Parameters**:
  - `sequence_numbers` (array of strings, required): Sequence number list. Maximum 100 per request.
- **Returns**: JSON object with full sequence detail records.
- **API**: `POST /api/ls/v2/sequence/fetch`
- **Usage**: Use to retrieve detailed sequence information after search.

### 5. `sequence_alignment`
- **Purpose**: Run sequence alignment.
- **Parameters**:
  - `alignment_type` (string, required): `PSA` for pairwise or `MSA` for multiple sequence alignment.
  - `query_sequence` (string, required for PSA): Query sequence string.
  - `subject_sequences` (array of strings, required): Subject sequence list.
- **Returns**: JSON object with alignment results.
- **API**: `POST /api/ls/v2/sequence/alignment`
- **Usage**: Use when the user wants to compare biological sequences directly.

### 6. `modification_search_submit`
- **Purpose**: Submit a search for bio sequence records filtered by modification conditions.
- **Parameters**:
  - `sequence_type` (string, required): Sequence type. One of `NUCLEOTIDE` or `PROTEIN`.
  - `database` (array of strings, required): Target database list.
  - `modification_location` (array of objects, required): List of modification filters.
  - `sequence` (string, optional): Optional query sequence for alignment narrowing.
- **Returns**: JSON object with `job_id`, `status`, and `submitted_at`.
- **API**: `POST /api/ls/v2/modification/search/submit`
- **Usage**: Use for PTM-specific searches. Follow the submit-check-results workflow.

### 7. `antibody_antigen_search`
- **Purpose**: Search for antibodies associated with a target antigen.
- **Parameters**:
  - `target_name` (string, required): Antigen target name.
  - `filter` (object, optional): Facet filters such as source, antibody species, antibody name.
  - `offset` (integer, optional): Pagination offset.
  - `limit` (integer, optional): Page size.
- **Returns**: JSON object with antibody records.
- **API**: `GET /api/ls/v2/antibody-antigen/search`
- **Usage**: Use for antibody discovery or prior-art searches.

## 💡 **Need help?**
Visit: [Patsnap Life Science](https://eureka.patsnap.com/ls-landing)
or  [Patsnap Dev Portal](https://open.patsnap.com/devportal)

---
## Integration with Patsnap Skills
This server powers the following Patsnap Skills (Claude Code agents):
- **target-intelligence**: uses this server's tools to retrieve life science evidence.
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
