# PatSnap Biology Modality

**PatSnap Biology Modality** is a Model Context Protocol (MCP) server that equips AI agents with direct, structured access to biological sequence data, modification records, and antibody-antigen interactions. It enables sequence similarity searching, post-translational modification queries, and antibody discovery across PatSnap's global patent and literature corpus of over 200M+ records.

## Quick Links
- [PatSnap Life Science Home](https://eureka.patsnap.com/ls-landing)
- [PatSnap Developer Portal](https://open.patsnap.com)
- [PatSnap Biology Modality MCP](https://open.patsnap.com/marketplace/mcp-servers/biology-modality)

## Setup

### 1. Get an API Key
Log in to [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key (format: `sk-xxxxxxxxxxxx`).

### 2. Connect the MCP Server
Run the following command in your terminal (requires [Claude Code](https://claude.ai) or any MCP-compatible client):

```bash
claude mcp add --transport http biology_modality \
  "https://connect.patsnap.com/06e741/Logic-mcp?apiKey=$PATSNAP_API_KEY"
```

Set your API key as an environment variable:
```bash
export PATSNAP_API_KEY=your-key-here
```

> **Other clients?** Visit the [Biology Modality page on PatSnap Marketplace](https://open.patsnap.com/marketplace/mcp-servers/biology-modality) and select your agent (Cursor, API, etc.) from the bottom-right corner to get the appropriate configuration snippet.

### 3. Verify
In Claude Code, type `/mcp` and confirm `biology_modality` shows **Connected**.

## Available Tools

> **Note for AI Agents:** Sequence and modification searches use an asynchronous job model: submit a job, poll for completion, then fetch results. `ls_antibody_antigen_search` returns results synchronously. Each tool below documents its exact parameters, types, and constraints as shown in the official PatSnap Marketplace.

### 1. `ls_sequence_search_submit`
- **Purpose**: Submit a biological sequence search job (protein or nucleotide) against PatSnap's patent and literature sequence database.
- **Parameters**:
  - `query_type` (string, required): Target sequence type to match against. One of `"NUCLEOTIDE"`, `"PROTEIN"`.
  - `sequence` (string, required): Single query sequence string.
  - `sequence_type` (string, required): Type of the query sequence provided. One of `"NUCLEOTIDE"`, `"PROTEIN"`.
  - `database` (array of strings, optional): Target database list. Supported values: `["ALLPATENT"]`, `["CLAIMS"]`, or both `["ALLPATENT", "CLAIMS"]`.
  - `perc_identity` (object, optional): Identity filter. Format: `{"start": <int>, "end": <int>}` (range 0-100).
  - `qcov_hsp_perc` (object, optional): Query coverage filter. Format: `{"start": <int>, "end": <int>}`.
  - `scov_hsp_perc` (object, optional): Subject coverage filter. Format: `{"start": <int>, "end": <int>}`.
  - `evalue` (number, optional): Expect threshold for alignment significance.
  - `subject_length` (object, optional): Subject length filter. Format: `{"start": <int>, "end": <int>}`.
  - `q_perc_identity` (object, optional): Query identity filter. Format: `{"start": <int>, "end": <int>}`.
  - `s_perc_identity` (object, optional): Subject identity filter. Format: `{"start": <int>, "end": <int>}`.
  - `with_gaps` (boolean, optional): Whether sequence alignment includes gaps.
  - `limit` (integer, optional): Maximum number of results returned internally by the backend task.
- **Returns**: JSON object with `job_id` (string), `status` (string), `submitted_at` (string, ISO timestamp).
- **API**: `POST /api/Ls/sequence/job`
- **Usage**: Use to initiate a similarity search. Afterwards, poll `ls_sequence_search_check_status` with the returned `job_id` until `status` is `"success"`, then retrieve results with `ls_sequence_search_get_results`.

### 2. `ls_sequence_search_check_status`
- **Purpose**: Check the current status of a previously submitted sequence or modification search job.
- **Parameters**:
  - `job_id` (string, required): Backend search job ID obtained from `ls_sequence_search_submit` or `ls_modification_search_submit`.
- **Returns**: JSON object with `job_id` (string), `status` (enum: "pending", "running", "success", "failed"), `progress` (integer, 0-100), and optionally `message` (string) on failure.
- **API**: `GET /api/Ls/sequence/job/status`
- **Usage**: Poll this endpoint until `status` becomes `"success"` before calling `ls_sequence_search_get_results`. Avoid calling the results tool while status is still "running" or "pending".

### 3. `ls_sequence_search_get_results`
- **Purpose**: Fetch the final results of a completed sequence or modification search job.
- **Parameters**:
  - `job_id` (string, required): Backend search job ID.
  - `offset` (integer, optional): Result offset for pagination, starting from 0.
  - `limit` (integer, optional): Page size for the downstream query (number of rows to return).
  - `sort_field` (string, optional): Field to sort by.
  - `order` (string, optional): Sort order, supports `"DESC"` or `"ASC"`.
  - `perc_identity` (object, optional): Identity filter on results, format `{"start": <number>, "end": <number>}`.
  - `qcov_hsp_perc` (object, optional): Query coverage filter, same format.
  - `scov_hsp_perc` (object, optional): Subject coverage filter, same format.
  - `q_perc_identity` (object, optional): Query identity filter, same format.
  - `s_perc_identity` (object, optional): Subject identity filter, same format.
- **Returns**: JSON object containing `job_id`, `total_hits` (integer), and `results` (array of matching records with fields like `patent_id`, `seq_id`, `identity`, `alignment`, `organism`, `annotation`).
- **API**: `GET /api/Ls/sequence/job/result`
- **Usage**: Call only after the job status is `"success"`. Use `offset` and `limit` for pagination.

### 4. `ls_modification_search_submit`
- **Purpose**: Submit a search job for biological sequences filtered by post-translational modification conditions, optionally combined with a query sequence.
- **Parameters**:
  - `sequence_type` (string, required): Sequence type, supports `"NUCLEOTIDE"` or `"PROTEIN"`.
  - `database` (array of strings, required): Target database list, e.g., `["ALLPATENT"]`, `["CLAIMS"]`, or both.
  - `modification_location` (array of objects, required): List of modification filters. Each object supports keys: `location`, `modification_name`, `operation`, `match_type`. (Refer to Marketplace for exact schema details.)
  - `sequence` (string, optional): Optional query sequence string used for alignment narrowing.
  - `subject_length` (object, optional): Subject length filter, format `{"start": <int>, "end": <int>}`.
  - `limit` (integer, optional): Maximum returned result count for the backend task.
- **Returns**: JSON object with `job_id` (string), `status` (string), `submitted_at` (string).
- **API**: `POST /api/Ls/modification/job`
- **Usage**: Use for PTM-specific searches. Follow the same submit, check status, get results workflow. Poll `ls_sequence_search_check_status` and then fetch with `ls_sequence_search_get_results`.

### 5. `ls_antibody_antigen_search`
- **Purpose**: Synchronously search for antibodies associated with a target antigen, with optional facet filters.
- **Parameters**:
  - `target_name` (string, required): Antigen target name (exact or keyword lookup).
  - `filter` (object, optional): Facet filters. Supported fields: `target_name`, `source`, `antigen_species`, `antibody_name`.
  - `offset` (integer, optional): Pagination offset, starting from 0.
  - `limit` (integer, optional): Page size for the downstream query.
- **Returns**: JSON object with `total_hits` (integer), `results` (array of antibody records containing `antibody_name`, `antigen`, `source`, `antibody_type`, `patent_id`, `binding_affinity`, `sequences`).
- **API**: `GET /api/Ls/antibody-antigen/search`
- **Usage**: Use for antibody discovery or prior art searches. This tool returns results directly without polling; it is synchronous.

## 💡 **Need help?**
Visit: [PatSnap Life Science](https://eureka.patsnap.com/ls-landing) 
or  [PatSnap Dev Portal](https://open.patsnap.com/devportal)

---

## Integration with PatSnap Skills
This server powers the biological sequence and antibody discovery layer for the following PatSnap Skills (Claude Code agents):
- **target-intelligence**: uses sequence search to find patents covering biological sequences related to therapeutic targets.
- **pharmaceuticals-exploration**: uses antibody-antigen search to discover antibody-based therapeutics.

Each Skill automatically invokes the appropriate tools from this server when performing its analyses. You can install the Skills from the [PatSnap Skills Library](https://github.com/patsnap/skills/tree/main/life-sciences). 
Or, if you use openclaw:
```bash
openclaw skills install SKILL_NAME
```

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com). Innovate with Confidence.
