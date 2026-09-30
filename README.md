# UCP agent profile — FLCPA product ID app

Public [Universal Commerce Protocol](https://ucp.dev) agent profile for FLCPA's product ID app.
Shopify's Catalog MCPs fetch it from the URL sent in `meta.ucp-agent.profile`:

https://flcpa.github.io/ucp-agent-profile/flcpa-catalog-agent.json

It declares catalog capabilities only (search, lookup, and Shopify's catalog extensions) — no cart,
checkout or orders. Served by GitHub Pages because Shopify requires `Content-Type: application/json`.
The source of truth is `profile/flcpa-catalog-agent.json` in the app's own repository; update both together.
