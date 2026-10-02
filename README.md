# UCP agent profile — FLCPA product ID app

Public [Universal Commerce Protocol](https://ucp.dev) agent profile for FLCPA's product ID app.
It declares catalog capabilities only (search, lookup, and Shopify's catalog extensions) — no cart,
checkout or orders.

## URL to send in `meta.ucp-agent.profile`

Served through jsDelivr, pinned to a commit:

https://cdn.jsdelivr.net/gh/flcpa-ai/ucp-agent-profile@abec1e8e688589b63fe9d8b471eef6b9971c431d/flcpa-catalog-agent.json

The UCP spec requires profiles to be served with `Cache-Control: public, max-age>=60` and Shopify
also requires `Content-Type: application/json`. jsDelivr meets both. GitHub Pages does not (it sends
`max-age=600` without `public`), and raw gist/GitHub URLs serve `text/plain`.

## Changing the profile

A commit-pinned jsDelivr URL is immutable. After changing the JSON, commit, then point
`UCP_PROFILE_URL` at the new commit SHA. The source of truth is `profile/flcpa-catalog-agent.json`
in the app's own repository; update both together.
