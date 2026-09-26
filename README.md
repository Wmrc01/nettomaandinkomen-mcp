# Nettomaandinkomen MCP Server

> Model Context Protocol (MCP) server for Dutch gross-to-net salary, holiday allowance, 13th month, WW unemployment benefits, and WIA/IVA disability calculations for the 2026 fiscal year.

Published by [Nettomaandinkomen.nl](https://www.nettomaandinkomen.nl).

[![Glama Connector](https://glama.ai/mcp/connectors/nl.nettomaandinkomen/nettomaandinkomen/badge)](https://glama.ai/mcp/connectors/nl.nettomaandinkomen/nettomaandinkomen)
[![Smithery](https://smithery.ai/server/@y-colenbrander/nettomaandinkomen/badge)](https://smithery.ai/server/@y-colenbrander/nettomaandinkomen)
[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg)](LICENSE)

---

## Endpoint

- **Hosted URL:** `https://www.nettomaandinkomen.nl/api/public/mcp`
- **Protocol:** Server-Sent Events (SSE) / JSON-RPC 2.0 (Streamable HTTP)
- **Authentication:** None required (free & public endpoint)
- **Documentation:** [https://www.nettomaandinkomen.nl/mcp](https://www.nettomaandinkomen.nl/mcp)

---

## Available Tools

| Tool | Description |
|---|---|
| `bruto-netto` | Calculates Dutch net monthly salary from gross income for 2026, including payroll tax, general tax credit, and labour tax credit. |
| `netto-inkomen` | Calculates complete net income including holiday allowance (8%), 13th month / year-end bonus, and optional pension deduction. |
| `ww-uitkering` | Calculates Dutch WW unemployment benefit based on historical daily wage (dagloon), capped at the legal maximum for 2026. |
| `wia-uitkering` | Estimates Dutch WIA / IVA disability benefit based on the UWV disability percentage and maximum daily wage. |

---

## Quickstart

### Claude Desktop

Add this to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "nettomaandinkomen": {
      "url": "https://www.nettomaandinkomen.nl/api/public/mcp"
    }
  }
}
