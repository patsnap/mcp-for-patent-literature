# Innovation Report Generator

> by [PatSnap](https://www.patsnap.com)

## Product Definition

Turns analytical results into deliverable reports and task-based outputs. It supports enterprise reports, patent value reports, and novelty-check reports for technical ideas, with download and similar-patent comparison support to help teams produce standardized materials more efficiently. It is suitable for client delivery, internal reporting, and pre-sales support. This MCP server connects AI agents to PatSnap data and workflow capabilities for the R&D-Innovation domain.

## Supported Tools and Query Types

- Turns analytical results into deliverable reports
- task-based outputs. It supports enterprise reports
- patent value reports
- novelty-check reports for technical ideas
- with download
- similar-patent comparison support to help teams produce standardized materials more efficiently. It is suitable for client delivery
- internal reporting
- pre-sales support

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "innovation_report_generator": {
      "url": "https://connect.patsnap.com/1fadfc/mcp",
      "type": "streamableHttp"
    }
  }
}
```

## Simplest Usage Example

1. Get a PatSnap API key from [PatSnap Open Platform](https://open.patsnap.com).
2. Replace `$PATSNAP_API_KEY` or `YOUR_API_KEY` in the MCP config.
3. Add the config to an MCP-compatible client.
4. Ask a simple domain question, such as: `Search recent records related to this target, drug, company, or patent topic.`

## Related Links

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/8929e1a2-7b3b-4f9d-9bf2-2e5e29524bd3](https://open.patsnap.com/marketplace/mcp-servers/8929e1a2-7b3b-4f9d-9bf2-2e5e29524bd3)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
