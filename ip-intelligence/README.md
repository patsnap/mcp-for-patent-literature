# PatSnap IP Intelligence MCP Servers

> by [PatSnap](https://www.patsnap.com)

Official Model Context Protocol (MCP) servers for IP Intelligence, powered by PatSnap's proprietary intelligence platform. These servers give AI agents structured access to PatSnap data, search, analytics, and workflow capabilities for this domain.

## Available MCP Servers

| Server | Focus | Quick Link |
|---|---|---|
| **Advanced Patent Search** | Provides flexible and in-depth advanced patent search capabilities. It supports semantic, similarity, image, patent-number, nested-query,... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/1f837249-fce5-4ae3-96b5-1d9038ec41d5) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-advanced-patent-search) |
| **Deep Patent Mining** | Designed for deeper mining of technical content from patent text and classification data. It supports analysis of technology topics, the... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/d1f84e46-f494-4927-aba8-94eeaef94c55) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-deep-patent-mining) |
| **Global Core Patent Database** | A core patent data tool for high-frequency patent workflows. It supports search, full text and drawings, legal status, licensing, transfe... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/8dc7ef1d-d900-4c6d-bec6-2a9c03e7456b) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-global-core-patent-database) |
| **IP & Innovation Courses** | A one-stop learning entry for courses, course details, and training materials on IP and innovation. It helps teams build a structured und... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/172edf47-eae9-4f01-b8c0-e6018aab79bf) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-ip-innovation-courses) |
| **Maintain Payment** | A global patent search tool for freedom-to-operate assessment. It supports query-based, semantic, and image search, and can be combined w... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/aae364b6-a111-4e17-a99f-d7b74539cfa3) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-maintain-payment) |
| **Patent Briefing** | A quick-read tool for understanding a patent or patent family. It brings together bibliographic data, legal status, family information, t... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/e54e3afc-df5c-47e9-878f-1e7bb38a7275) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-patent-briefing) |
| **Patent Landscape Analytics** | Converts patent search results into practical patent landscape analysis. It covers filing trends, technology composition, leading applica... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/6dd83771-70f2-46ce-b4aa-6fdf60ace3f8) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-patent-landscape-analytics) |
| **Patent Legal Status & Annuity** | Focused on reviewing patent legal status, annuity status, and core legal documents. It supports annuity payment information, legal status... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/cba8ca99-fcc3-4cb6-8afd-baf393151692) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-patent-legal-status-annuity) |
| **Patent Monetization & Valuation** | A tool designed for patent transactions, licensing, and commercialization-oriented valuation. It combines patent value, legal status, lic... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/1c20be56-30a5-4917-b5dd-f88986fbe9f8) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-patent-monetization-valuation) |
| **Patent Valuation Scorecard** | Breaks patent value into multiple scoring dimensions such as technology, legal strength and stability, market relevance, strategy, protec... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/ff5b188b-48c5-49ce-aaa7-0b1294a89d55) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-patent-valuation-scorecard) |
| **Patent Visual Analytics** | Transforms patent data into more intuitive visual analysis. It supports chart-based views across trends, patent types, value, litigation,... | [Marketplace](https://open.patsnap.com/marketplace/mcp-servers/29ec8427-6e8a-4125-a246-10af19b24001) Or [Repo](https://github.com/patsnap/mcp/tree/main/ip-intelligence/patsnap-patent-visual-analytics) |

## Setup

All servers follow the same setup pattern. You can connect one or all of them depending on your use case.

### 1. Get an API Key

Log in to the [PatSnap Developer Platform](https://open.patsnap.com), go to **API Keys**, and create a new key.

### 2. Connect the MCP Servers

Run the following commands in your terminal with an MCP-compatible client:

```bash
# Advanced Patent Search
claude mcp add --transport http advanced_patent_search \
  "https://connect.patsnap.com/33072f/mcp"

# Deep Patent Mining
claude mcp add --transport http deep_patent_mining \
  "https://connect.patsnap.com/7cc6ae/mcp"

# Global Core Patent Database
claude mcp add --transport http global_core_patent_database \
  "https://connect.patsnap.com/1458a4/mcp"

# IP & Innovation Courses
claude mcp add --transport http ip_innovation_courses \
  "https://connect.patsnap.com/588922/mcp"

# Maintain Payment
claude mcp add --transport http maintain_payment \
  "https://connect.patsnap.com/e5851d/mcp"

# Patent Briefing
claude mcp add --transport http patent_briefing \
  "https://connect.patsnap.com/958a46/mcp"

# Patent Landscape Analytics
claude mcp add --transport http patent_landscape_analytics \
  "https://connect.patsnap.com/59100a/mcp"

# Patent Legal Status & Annuity
claude mcp add --transport http patent_legal_status_annuity \
  "https://connect.patsnap.com/30096b/mcp"

# Patent Monetization & Valuation
claude mcp add --transport http patent_monetization_valuation \
  "https://connect.patsnap.com/11227f/mcp"

# Patent Valuation Scorecard
claude mcp add --transport http patent_valuation_scorecard \
  "https://connect.patsnap.com/67d1b4/mcp"

# Patent Visual Analytics
claude mcp add --transport http patent_visual_analytics \
  "https://connect.patsnap.com/3fd502/mcp"
```

Set your API key as an environment variable:

```bash
export PATSNAP_API_KEY=sk-your-key-here
```

### 3. Verify

In your MCP-compatible client, confirm that the added servers show as connected.

## Resources

- [PatSnap](https://www.patsnap.com)
- [PatSnap Developer Portal](https://open.patsnap.com)
- [PatSnap MCP Marketplace](https://open.patsnap.com/marketplace/mcp-servers)
- [PatSnap MCP Server Source](https://github.com/patsnap/mcp)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com) ? Innovate with Confidence.
