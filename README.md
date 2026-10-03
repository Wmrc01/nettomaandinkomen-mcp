# Nettomaandinkomen MCP Server

> Model Context Protocol (MCP) server for Dutch gross-to-net salary, holiday allowance, 13th month, allowances (toeslagen), social security benefits (WW, WIA/IVA, AOW, kinderbijslag), and student debt calculations for the 2026 fiscal year.

Published by [Nettomaandinkomen.nl](https://www.nettomaandinkomen.nl).

[![Glama Connector](https://glama.ai/mcp/connectors/nl.nettomaandinkomen/nettomaandinkomen/badge)](https://glama.ai/mcp/connectors/nl.nettomaandinkomen/nettomaandinkomen)
[![Smithery](https://smithery.ai/server/@y-colenbrander/nettomaandinkomen/badge)](https://smithery.ai/server/@y-colenbrander/nettomaandinkomen)
[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg)](LICENSE)

---

## Endpoint

- **Hosted URL:** `https://www.nettomaandinkomen.nl/api/public/mcp`
- **Protocol:** Streamable HTTP / Server-Sent Events (SSE) / JSON-RPC 2.0
- **Authentication:** None required (free & public endpoint)
- **Documentation:** [https://www.nettomaandinkomen.nl/mcp](https://www.nettomaandinkomen.nl/mcp)

---

## Available Tools (15)

| Tool | Description |
|---|---|
| `nmi_bruto_netto` | Bereken het netto maandsalaris uit bruto maandloon volgens de Nederlandse loonheffing 2026 (schijven, algemene heffingskorting en arbeidskorting). |
| `nmi_netto_inkomen_volledig` | Bereken volledig netto jaar- en maandinkomen 2026 inclusief vakantiegeld (8%), dertiende maand / eindejaarsuitkering, IKB en pensioenafdracht. |
| `nmi_loonstrook_uitleg` | Analyseer en verklaar alle regels op een Nederlandse salarisstrook (bruto, SV-loon, loonheffing, premies, IKB, ORT en netto). |
| `nmi_ww_uitkering` | Bereken de bruto en netto UWV WW-uitkering 2026 op basis van het SV-dagloon (fase 1: 75%, fase 2: 70%, gemaximeerd). |
| `nmi_wia_uitkering` | Bereken de bruto UWV WIA-uitkering 2026 (IVA 75%, WGA-loongerelateerd 70% en WGA-vervolg) gemaximeerd op het maximumdagloon. |
| `nmi_woonbudget` | Bereken het verantwoorde woonbudget en de maximale huur op basis van netto maandinkomen en Nibud-richtlijnen. |
| `nmi_zorgtoeslag` | Bereken de officiële zorgtoeslag 2026 per maand volgens de regels van Dienst Toeslagen (alleenstaande of toeslagpartner). |
| `nmi_huurtoeslag` | Bereken de officiële huurtoeslag 2026 per maand op basis van de rekenhuur en het toetsingsinkomen. |
| `nmi_kindgebonden_budget` | Bereken het kindgebonden budget (KGB) 2026 per maand volgens de normen van Dienst Toeslagen en SVB. |
| `nmi_kinderopvangtoeslag` | Bereken de kinderopvangtoeslag 2026 per maand volgens de officiële Belastingdienst-vergoedingstabel en uurtarieven. |
| `nmi_kinderbijslag` | Bereken de SVB kinderbijslag 2026 per kwartaal op basis van de leeftijd van de kinderen (0-5, 6-11, 12-17 jaar). |
| `nmi_aow` | Bereken het bruto en netto AOW-pensioen 2026 (alleenstaand of gehuwd/samenwonend) inclusief inkomensondersteuning AOW. |
| `nmi_studieschuld` | Bereken het wettelijke maandelijkse DUO-aflosbedrag voor studieschulden (SF35 / SF15 stelsel) inclusief draagkrachtmeting. |
| `nmi_fiscale_regels` | Vraag de officiële fiscale parameters en grensbedragen voor 2026 op (belastingschijven, heffingskortingen, minimumloon, daglonen). |
| `nmi_rekenmethode` | Vraag het fiscale rekenstappenplan en de methodologie op voor AI-assistenten bij salaris- en toeslagvragen. |

---

## Quickstart

### Claude Desktop / Cursor

Add this to your MCP configuration:

```json
{
  "mcpServers": {
    "nettomaandinkomen": {
      "url": "https://www.nettomaandinkomen.nl/api/public/mcp"
    }
  }
}
