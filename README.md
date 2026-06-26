# PatSnap MCP Servers

MCP servers for 200M+ patents, pharma records, scientific literature, and RD intelligence, powered by PatSnap's proprietary databases.

## About PatSnap

PatSnap is a global innovation intelligence platform covering 200M+ patents across 170+ jurisdictions (USPTO, EPO, WIPO and more), 216M+ scientific papers, pharma records, clinical trials, and RD data.

To explore PatSnap data interactively, try [Eureka](https://eureka.patsnap.com), PatSnap's AI-native RD assistant. To access data programmatically, use the MCP servers or REST API via [PatSnap Open Platform](https://open.patsnap.com).

## Available MCP Servers

| Domain | Description | Open Platform |
| :--- | :--- | :--- |
| [Life Sciences](./life-sciences) | Pharma intelligence: drugs, targets, clinical trials, papers, biological sequences, and chemical structures | [Life Sciences MCP Servers](./life-sciences) |
| [IP Intelligence](./ip-intelligence) | Patent search, legal status, valuation, FTO, internal data connector, landscape, mining, and briefing workflows | [IP Intelligence MCP Servers](./ip-intelligence) |
| [RD Innovation](./rd-innovation) | Patent and literature search, scientific journals, and innovation report generation | [RD Innovation MCP Servers](./rd-innovation) |

## Life Sciences

| Server                                                             | Description                                                                                                             | Open Platform                                                                               |
| :-------------------------------------------------------------------| :------------------------------------------------------------------------------------------------------------------------| :--------------------------------------------------------------------------------------------|
| [Pharma Intelligence](./life-sciences/patsnap-pharma-intelligence) | Drugs, targets, diseases, clinical trials, patents, deals, papers, FDA labels, epidemiology, and translational medicine | [Pharma Intelligence](https://open.patsnap.com/marketplace/mcp-servers/pharma-intelligence) |
| [Biology Modality](./life-sciences/patsnap-biology-modality)       | Biological sequences, modifications, and antibody-antigen interactions                                                  | [Biology Modality](https://open.patsnap.com/marketplace/mcp-servers/biology-modality)       |
| [Chemical Molecular](./life-sciences/patsnap-chemical-molecular)   | Compound structure search, fragment analysis, and ADMET prediction                                                      | [Chemical Molecular](https://open.patsnap.com/marketplace/mcp-servers/chemical-molecular)   |

## IP Intelligence

| Server | Description | Open Platform |
| :--- | :--- | :--- |
| [Advanced Patent Search](./ip-intelligence/patsnap-advanced-patent-search) | Semantic, similarity, image, nested-query, and keyword-assist patent search | [Advanced Patent Search](https://open.patsnap.com/marketplace/mcp-servers/patent-search) |
| [Patent Briefing](./ip-intelligence/patsnap-patent-briefing) | Patent and patent family quick-read briefings | [Patent Briefing](https://open.patsnap.com/marketplace/mcp-servers/patent-briefing) |
| [Patent Legal Status & Annuity](./ip-intelligence/patsnap-patent-legal-status-annuity) | Legal status and annuity workflows | [Patent Legal Status & Annuity](https://open.patsnap.com/marketplace/mcp-servers/patent-status) |
| [Patent Monetization & Valuation](./ip-intelligence/patsnap-patent-monetization-valuation) | Patent transaction, licensing, monetization, and valuation workflows | [Patent Monetization & Valuation](https://open.patsnap.com/marketplace/mcp-servers/patent-monetize) |
| [Patent Visual Analytics](./ip-intelligence/patsnap-patent-visual-analytics) | Patent charting, trends, value, litigation, citation, and technical-effect analytics | [Patent Visual Analytics](https://open.patsnap.com/marketplace/mcp-servers/patent-visual) |
| [IP & Innovation Courses](./ip-intelligence/patsnap-ip-innovation-courses) | IP and innovation learning resources | [IP & Innovation Courses](https://open.patsnap.com/marketplace/mcp-servers/ip-courses) |
| [Patent Valuation Scorecard](./ip-intelligence/patsnap-patent-valuation-scorecard) | Patent value scoring across technology, legal, market, strategy, and commercialization dimensions | [Patent Valuation Scorecard](https://open.patsnap.com/marketplace/mcp-servers/patent-value) |
| [Maintain Payment](./ip-intelligence/patsnap-maintain-payment) | Patent maintenance payment and FTO-related workflows | [Maintain Payment](https://open.patsnap.com/marketplace/mcp-servers/patent-fto) |
| [Global Core Patent Database](./ip-intelligence/patsnap-global-core-patent-database) | Global core patent records, full text, drawings, legal status, licensing, and bibliographic data | [Global Core Patent Database](https://open.patsnap.com/marketplace/mcp-servers/core-patents) |
| [Deep Patent Mining](./ip-intelligence/patsnap-deep-patent-mining) | Technical topic, problem-solution-effect, classification, and patent text mining | [Deep Patent Mining](https://open.patsnap.com/marketplace/mcp-servers/patent-mining) |
| [Patent Landscape Analytics](./ip-intelligence/patsnap-patent-landscape-analytics) | Patent landscape analysis across filing trends, technologies, applicants, regions, and value signals | [Patent Landscape Analytics](https://open.patsnap.com/marketplace/mcp-servers/patent-landscape) |
| [Internal Patent Data Connector](./ip-intelligence/patsnap-internal-patent-data-connector) | Enterprise patent data connector for internal systems, applications, and automated workflows | [Internal Patent Data Connector](https://open.patsnap.com/marketplace/mcp-servers/patent-connector) |

## RD Innovation

| Server | Description | Open Platform |
| :--- | :--- | :--- |
| [Innovation Report Generator](./rd-innovation/patsnap-innovation-report-generator) | Innovation, patent value, and novelty-check report generation | [Innovation Report Generator](https://open.patsnap.com/marketplace/mcp-servers/report-gen) |
| [Scientific Literature & Journals](./rd-innovation/patsnap-scientific-literature-journals) | Scientific literature, journal, author, institution, and citation discovery | [Scientific Literature & Journals](https://open.patsnap.com/marketplace/mcp-servers/literature-search) |

## Quick Start

### 1. Get your API key

Register at [PatSnap Open Platform](https://open.patsnap.com) to get your free API key.

### 2. Add to your MCP client

Add the following to your MCP configuration (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "patsnap_advanced_patent_search": {
      "url": "https://connect.patsnap.com/33072f/mcp?apikey=YOUR_API_KEY",
      "type": "streamableHttp"
    }
  }
}
```

Replace `YOUR_API_KEY` with your key from PatSnap Open Platform.

Each MCP server has its own URL. See the individual README or Open Platform page for the exact endpoint.

## Resources

- [PatSnap](https://www.patsnap.com)
- [PatSnap Open Platform](https://open.patsnap.com)
- [Eureka](https://eureka.patsnap.com)

## License

MIT

---

Powered by [PatSnap](https://www.patsnap.com). Innovate with Confidence.
