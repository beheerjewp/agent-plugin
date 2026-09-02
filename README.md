# Beheer je WP — agent plugin

Beheer één WordPress-site vanuit je eigen AI-assistent (Claude Code, Codex, ChatGPT, Cursor, Grok Build of elke andere MCP-client). De assistent leest je site, zoekt content en zet wijzigingen klaar als voorstel. Jij keurt ze goed in WordPress. Niets gaat live zonder jouw akkoord.

Website: https://beheerjewp.nl · Docs: https://beheerjewp.nl/wordpress-mcp · Hulp: https://beheerjewp.nl/hulp

## Wat zit erin
- `mcp.json` / `.mcp.json` — verbinding met de hosted MCP-server `https://beheerjewp.nl/mcp` (Streamable HTTP, OAuth 2.0 met dynamic client registration; de client regelt de login).
- `skills/wordpress-beheer` — werkwijze voor lezen, zoeken en voorstellen klaarzetten.
- `skills/wordpress-seo` — werkwijze voor SEO-kansen op basis van Search Console (SEO Pro).

## Tools (10)
`get_connection_status`, `get_product_capabilities`, `get_brand_guidance`, `get_site_overview`, `list_posts`, `get_post_content`, `propose_post_update`, `get_search_console_status`, `get_search_performance`, `find_seo_opportunities`. Alleen `propose_post_update` schrijft, en dan alleen een voorstel dat je zelf goedkeurt.

## Installeren
- **Claude Code:** `claude plugin marketplace add beheerjewp/agent-plugin` en installeer `beheer-je-wp`. Of direct: `claude mcp add --transport http beheer-je-wp https://beheerjewp.nl/mcp`.
- **Codex:** `codex plugin marketplace add beheerjewp/agent-plugin`.
- **Cursor / Agent Plugins-clients:** installeer deze repo als plugin; `plugin.json` + `mcp.json` volgen de Agent Plugins 1.1.0-standaard.
- **Grok Build:** `grok plugin install https://github.com/beheerjewp/agent-plugin.git`.
- **Claude.ai / Desktop:** voeg `https://beheerjewp.nl/mcp` toe als custom connector.

Bij de eerste tool-aanroep log je in bij Beheer je WP en koppel je precies één site.

## Netwerk en data
De plugin praat alleen met `https://beheerjewp.nl`. Er worden geen WordPress-wachtwoorden in de assistent opgeslagen; de koppeling gebruikt een intrekbaar OAuth-token. Privacy: https://beheerjewp.nl/privacy · Voorwaarden: https://beheerjewp.nl/voorwaarden

## Licentie
MIT (deze plugin-verpakking). De dienst zelf valt onder de voorwaarden van Beheer je WP.
