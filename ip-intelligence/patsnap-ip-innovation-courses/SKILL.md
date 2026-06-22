---
name: patsnap-ip-innovation-courses
description: PatSnap IP & Innovation Courses MCP for AI agents. A one-stop learning entry for courses, course details, and training materials on IP and innovation. It helps teams build a structured understanding of patents, search, analysis, and business use while lowering the learning barrier for new users. It is useful for internal training, customer education, and knowledge enablement.
homepage: https://open.patsnap.com/marketplace/mcp-servers/ip-courses
metadata:
  author: PatSnap
  category: "IP Intelligence"
  version: 1.0.0
  requires:
    mcp_endpoint: "https://connect.patsnap.com/588922/mcp?apikey=YOUR_API_KEY"
---

## Setup
Get your API Key at https://open.patsnap.com

# IP & Innovation Courses

This skill connects your AI agent to **PatSnap's IP & Innovation Courses MCP server**.

With this skill, your agent can use PatSnap data and workflow capabilities for IP Intelligence tasks.

## Prerequisites

This skill requires the **PatSnap IP & Innovation Courses MCP server** to be configured in your environment:

```json
{
  "mcpServers": {
    "ip_innovation_courses": {
      "url": "https://connect.patsnap.com/588922/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Get your API key at [open.patsnap.com](https://open.patsnap.com).

For the full list of available tools and input parameters, refer to the official MCP server documentation:
https://open.patsnap.com/marketplace/mcp-servers/ip-courses

---

## Instructions for AI Agents

### Step 1: Understand the user's search intent
Identify the target entities, date ranges, owners, patent numbers, technologies, or document types in the user's request.

### Step 2: Choose the right workflow
Use semantic, fielded, identifier-based, analytics, or retrieval workflows according to the task and available MCP tools.

### Step 3: Synthesize and cite
Present results in a structured format and cite returned patent numbers, record IDs, titles, organizations, or source names when available.

---

## Example Workflows

- Use IP & Innovation Courses to analyze recent patent activity for a target technology.
- Find relevant patents and summarize the key applicants, dates, and technical themes.
- Compare the most important records returned by IP & Innovation Courses.

## Resources

- **MCP Server**: [https://open.patsnap.com/marketplace/mcp-servers/ip-courses](https://open.patsnap.com/marketplace/mcp-servers/ip-courses)
- **PatSnap Open Platform**: [open.patsnap.com](https://open.patsnap.com)
- PatSnap: [https://www.patsnap.com](https://www.patsnap.com)
