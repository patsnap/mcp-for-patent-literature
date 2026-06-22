# IP & Innovation Courses

> by [PatSnap](https://www.patsnap.com)

## Product Definition

A one-stop learning entry for courses, course details, and training materials on IP and innovation. It helps teams build a structured understanding of patents, search, analysis, and business use while lowering the learning barrier for new users. It is useful for internal training, customer education, and knowledge enablement. This MCP server connects AI agents to PatSnap data and workflow capabilities for the Ip-Intelligence domain.

## Supported Tools and Query Types

- A one-stop learning entry for courses
- course details
- training materials on IP
- innovation. It helps teams build a structured understanding of patents
- search
- analysis
- business use while lowering the learning barrier for new users. It is useful for internal training
- customer education

## Data Sources and Coverage

This MCP server is powered by PatSnap proprietary databases and official platform services. Coverage depends on the enabled PatSnap product, account permissions, and API key scope.

## MCP Config JSON

```json
{
  "mcpServers": {
    "ip_innovation_courses": {
      "url": "https://connect.patsnap.com/588922/mcp",
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

- Official MCP page: [https://open.patsnap.com/marketplace/mcp-servers/172edf47-eae9-4f01-b8c0-e6018aab79bf](https://open.patsnap.com/marketplace/mcp-servers/172edf47-eae9-4f01-b8c0-e6018aab79bf)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
- PatSnap Open Platform: [https://open.patsnap.com](https://open.patsnap.com)
- Source repository: [https://github.com/patsnap/mcp](https://github.com/patsnap/mcp)
