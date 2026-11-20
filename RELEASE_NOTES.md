## Hazards and alerts API endpoints, snapshot 15 Nov 2026

- 53,354 endpoints passed a keyless data call, tested 14–15 Nov 2026 (IST)
- 6,381 services · 190 country codes · 45,322 keyless JSON rows

### Download

- `Hazards_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz`: the full list, 53,354 rows, 2.6 MB gzipped (17.5 MB as CSV), SHA-256 `b2e2b0a96ee49f39008d0a8d6dbcff44e9a78e6f42efd07dd944e19bcf16f00f`
- `SHA256SUMS.txt`: the checksum of that file

Check the download in the folder that holds both files:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
shasum -a 256 -c SHA256SUMS.txt      # macOS
certutil -hashfile Hazards_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz SHA256   # Windows: compare with SHA256SUMS.txt
```

Then `gunzip Hazards_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz` and pass the CSV path to the examples or to `node tools/test-endpoints.mjs`. The repository itself holds a 1,000-row sample and the services list.

### What's in it for you

- 🤖 Agent tools: 25,041 · Wrap one layer or warning feed as a get_hazard_at tool: pass a region code, or a point for a map layer, and return the hazard class, warning level or outlook category with a timeout. The tested layer queries return a few attribute rows and no geometry; set `returnGeometry=true` and add `geometry=lon,lat&geometryType=esriGeometryPoint&inSR=4326&spatialRel=esriSpatialRelIntersects` to ask about one place.
- 📱 App features: 283 · Show the alerts in force for a place: map the user's county or region to its zone code, fetch that alert or warning URL, and list event, severity and expiry time on a card or map.
- 🧠 Grounding and data pipelines: 6,858 · Load hazard zones on a schedule into your own store, so answers about the hazard at an address cite a dated source and a layer name.
- 🧪 Evals and testing: 53,354 · Run your hazard tool against a fixed set of URLs across formats; check that event, hazard class or warning level parse, and keep last_tested as the baseline for your own re-tests.

### Changes

- First release
- Left out: 1,180 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 982 class-exercise copies of the same few ArcGIS Online layers (Miami Beach sea level rise, high-risk areas without shelter, flooded areas, sea level rise and storm surge maps) across many organisations, many with a person's name in the title.
- Left out: 10 layers marked editable in the title (they can hold entries that people added).
- Left out: 155 ArcGIS layers that keep a form's default service name (they can hold people's form answers).
- Left out: 716 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 79 ArcGIS layers that hold reports, comments, submissions or form responses sent in by the public.
- Left out: 140 class-exercise copies of the same few wildfire layers in one ArcGIS Online organisation, many with a person's name in the title.
- Overlap: 1,549 of these URLs are also in 190k-weather-apis-for-agents.
- Overlap: 379 of these URLs are also in 270k-transit-apis-for-agents.
- Overlap: 6,148 of these URLs are also in 270k-water-apis-for-agents.
- Overlap: 116 of these URLs are also in 130k-finance-economy-apis-for-agents.
- Overlap: 62 of these URLs are also in 130k-india-apis-for-agents.
- Overlap: 549 of these URLs are also in 86k-oceans-apis-for-agents.
- Overlap: 57 of these URLs are also in 20k-air-quality-apis-for-agents.
- Overlap: 45,322 of these URLs are also in 2.5m-agent-ready-apis.
- Overlap: 6,246 of these URLs are also in 6.5k-wildfire-apis-for-agents.
- Overlap: 83 of these URLs are also in 24k-traffic-apis-for-agents.
- Overlap: 39 of these URLs are also in 12k-parking-apis-for-agents.
- Overlap: 10,315 of these URLs are also in 10k-earthquake-apis-for-agents.
- Overlap: 5,042 of these URLs are also in 5.2k-volcano-tsunami-apis-for-agents.
- Overlap: 1 of these URLs is also in 17k-bike-share-apis-for-agents.

On the date in last_tested (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The format column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 14–15 Nov 2026; snapshot 15 Nov 2026.

For the latest tested endpoints, search agentpopulation.com/apis. This pack is a snapshot from 15 Nov 2026.

Credit: Hazards and alerts API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 15 Nov 2026.

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · corrections: [@agentpopulation](https://x.com/agentpopulation) on X
