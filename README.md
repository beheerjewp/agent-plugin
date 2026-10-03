# Beheer je WP — agent plugin

Beheer één WordPress-site vanuit je eigen AI-assistent (Claude Code, Codex, ChatGPT, Cursor, Grok Build of elke andere MCP-client). De assistent leest je site, zoekt content en zet wijzigingen klaar als voorstel. Jij keurt ze goed in WordPress. Niets gaat live zonder jouw akkoord.

Website: https://beheerjewp.nl · Docs: https://beheerjewp.nl/wordpress-mcp · Hulp: https://beheerjewp.nl/hulp

## Wat zit erin
- `mcp.json` / `.mcp.json` — verbinding met de hosted MCP-server `https://beheerjewp.nl/mcp` (Streamable HTTP, OAuth 2.0 met dynamic client registration; de client regelt de login).
- `skills/wordpress-beheer` — werkwijze voor lezen, zoeken en voorstellen klaarzetten.
- `skills/wordpress-seo` — werkwijze voor SEO-kansen op basis van Search Console (SEO Pro).

## Tools (11)
`get_connection_status`, `get_product_capabilities`, `get_brand_guidance`, `get_site_overview`, `list_posts`, `get_post_content`, `propose_post_update`, `get_search_console_status`, `get_search_performance`, `find_seo_opportunities`, `prepare_seo_service_request`. De laatste tool maakt alleen een overdrachtsvoorstel voor SEO-hulp; hij bestelt en betaalt niets. Alleen `propose_post_update` schrijft, en dan alleen een voorstel dat je zelf goedkeurt.

## Eerst je WordPress-site verbinden

1. Maak een account op https://beheerjewp.nl/start en voeg het exacte https-adres van je WordPress-site toe.
2. Open de website in je dashboard. Download daar het plugin-zipbestand. De WordPress-code staat al op dezelfde pagina.
3. Open in WordPress **Plugins → Nieuwe plugin → Plugin uploaden**, kies de zip, installeer en activeer **SamAutomation Sitebeheer**.
4. Open **Gereedschap → Beheer je WP**. Plak de WordPress-code en klik op **Koppel mijn website**. De code werkt één keer en is 60 minuten geldig.
5. Keer terug naar het dashboard en controleer dat de site **Verbonden** toont. Bij een verlopen of gebruikte code maak je daar een nieuwe code. Het websiteadres moet overeenkomen met je WordPress-site.

De WordPress-code is voor de plugin. Deel hem niet in een chat. Een connectorcode voor een handmatige assistentkoppeling is een andere code; die is tien minuten geldig.

## Je assistent koppelen

- **Claude Code:** voeg de remote MCP-server toe met `claude mcp add --transport http beheer-je-wp https://beheerjewp.nl/mcp`. Open daarna `/mcp` in Claude Code om de verbinding te autoriseren.
- **Codex:** gebruik `codex mcp add beheer-je-wp --url https://beheerjewp.nl/mcp` en zo nodig `codex mcp login beheer-je-wp`.
- **Claude.ai / Desktop:** voeg `https://beheerjewp.nl/mcp` toe als custom connector en volg de login.
- **Cursor / Agent Plugins-clients:** installeer deze repo via een client die pluginrepos ondersteunt, of voeg dezelfde remote MCP-URL toe.
- **Andere MCP-clients:** gebruik `https://beheerjewp.nl/mcp` met OAuth. Ondersteuning en beschikbaarheid hangen van je client af.

Log in bij Beheer je WP, kies jouw verbonden site en geef toestemming. Start met: "Controleer mijn WordPress-site en wijzig nog niets." Laat daarna een titelwijziging voor een **conceptbericht** voorstellen. Je controleert dat voorstel in WordPress onder **Gereedschap → Beheer je WP voorstellen**. Via deze publieke connector kun je geen bericht publiceren of inplannen.

## Netwerk en data
De plugin praat alleen met `https://beheerjewp.nl`. Er worden geen WordPress-wachtwoorden in de assistent opgeslagen; de koppeling gebruikt een intrekbaar OAuth-token. Privacy: https://beheerjewp.nl/privacy · Voorwaarden: https://beheerjewp.nl/voorwaarden

## Licentie
MIT (deze plugin-verpakking). De dienst zelf valt onder de voorwaarden van Beheer je WP.
