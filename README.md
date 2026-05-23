# Maxar Technologies

Maxar Technologies was a publicly traded Earth-imaging and space-systems company formed from the 2017 merger of MacDonald, Dettwiler and Associates (MDA) with DigitalGlobe (founded 1992 in Oakland, California). In **December 2022 private-equity firm Advent International agreed to take Maxar private in a USD 6.4 billion cash deal that closed in May 2023**, after which Advent split the company into **Maxar Intelligence** (imagery and geospatial software, Westminster, Colorado) and **Maxar Space Systems** (satellite manufacturing, Palo Alto, California).

On **1 October 2025** both units rebranded — **Maxar Intelligence became Vantor** and **Maxar Space Systems became Lanteris Space Systems**. On **13 January 2026 Intuitive Machines completed the acquisition of Lanteris from Advent for approximately USD 800 million**, leaving **Vantor as the sole remaining Advent-owned successor of the Maxar brand**.

This profile documents the public developer API surface that Maxar / Vantor expose — the Vantor Hub APIs (Authentication, Discovery, Account Services), the Maxar Geospatial Platform (Streaming, Ordering, Tasking, Monitoring, Vivid basemaps), the legacy Maxar Content Catalog API, the open-source Transform API tooling, and the free Maxar Open Data STAC catalog on AWS Open Data.

**URLs:**
- Vantor (Intelligence): https://vantor.com/
- Lanteris Space Systems (Manufacturing, now Intuitive Machines): https://en.wikipedia.org/wiki/Lanteris_Space_Systems
- Developer portal: https://hub.vantor.com/ (also reachable at https://pro.maxar.com/)

## Scope

- **Type:** Index
- **Position:** Consuming
- **Access:** 3rd-Party

## Corporate Lineage

| Year | Event |
| ---- | ----- |
| 1992 | DigitalGlobe founded in Oakland, California by Walter Scott |
| 2017 | MDA acquires DigitalGlobe; combined entity renamed Maxar Technologies (HQ Westminster, CO) |
| Dec 2022 | Advent International announces $6.4B cash deal to take Maxar private |
| May 2023 | Advent acquisition closes |
| Sep 2023 | Maxar split into Maxar Intelligence and Maxar Space Systems |
| Oct 1 2025 | Maxar Intelligence → **Vantor**; Maxar Space Systems → **Lanteris Space Systems** |
| Jan 13 2026 | Intuitive Machines completes acquisition of Lanteris for ~$800M |

## Tags

Satellite Imagery, Earth Observation, Geospatial, Remote Sensing, Spatial Intelligence, Defense, Intelligence, WorldView, STAC, OGC, WMS, WMTS, WFS, Tasking, Basemaps, Vantor, Lanteris, Advent International, Private Equity

## APIs

### Vantor Hub Authentication API
OAuth-style token service issuing bearer access tokens for every other Hub API.
- **Docs:** https://hub.vantor.com/docs/authentication/
- **OpenAPI:** [openapi/authentication-openapi.yml](openapi/authentication-openapi.yml)
- **Capability:** [capabilities/shared/authentication.yaml](capabilities/shared/authentication.yaml)

### Vantor Hub Discovery API
STAC-aligned search across Vantor's "125+ petabytes of imagery and derivatives" — WorldView, GeoEye and WorldView Legion imagery plus Vivid basemaps and derivative analytics.
- **Docs:** https://hub.vantor.com/docs/discovery/
- **OpenAPI:** [openapi/discovery-openapi.yml](openapi/discovery-openapi.yml)
- **Capability:** [capabilities/shared/discovery.yaml](capabilities/shared/discovery.yaml)

### Vantor Hub Account Services API
Administrative account-management — users, roles, entitlements, credit balances and API keys.
- **Docs:** https://hub.vantor.com/docs/admin/
- **OpenAPI:** [openapi/admin-openapi.yml](openapi/admin-openapi.yml)
- **Capability:** [capabilities/shared/admin.yaml](capabilities/shared/admin.yaml)

### Maxar Geospatial Platform Streaming API
OGC WMS, WMTS and WFS services backed by securewatch.maxar.com; surfaced through the MGP_SDK Python, Java and R clients.
- **Docs:** https://maxar-geospatial-platform.readthedocs.io/en/latest/
- **OpenAPI:** [openapi/streaming-openapi.yml](openapi/streaming-openapi.yml)
- **Capability:** [capabilities/shared/streaming.yaml](capabilities/shared/streaming.yaml)

### Maxar Geospatial Platform Ordering API
Asynchronous orders against the WorldView / GeoEye / Legion archive with S3 or direct-download delivery.
- **OpenAPI:** [openapi/ordering-openapi.yml](openapi/ordering-openapi.yml)
- **Capability:** [capabilities/shared/ordering.yaml](capabilities/shared/ordering.yaml)

### Maxar Geospatial Platform Tasking API
Real-time tasking on the Vantor Constellation (WorldView-1/2/3, GeoEye-1 and the six-satellite WorldView Legion fleet delivering 30 cm-class native resolution).
- **OpenAPI:** [openapi/tasking-openapi.yml](openapi/tasking-openapi.yml)
- **Capability:** [capabilities/shared/tasking.yaml](capabilities/shared/tasking.yaml)

### Maxar Geospatial Platform Monitoring API
Stand watches over user-defined AOIs; receive notifications for new images, closed windows and analytic detections.
- **OpenAPI:** [openapi/monitoring-openapi.yml](openapi/monitoring-openapi.yml)
- **Capability:** [capabilities/shared/monitoring.yaml](capabilities/shared/monitoring.yaml)

### Maxar Vivid Basemap API
Global cloud-free, color-balanced basemap product exposed through MGP streaming.
- **Capability:** [capabilities/shared/basemaps.yaml](capabilities/shared/basemaps.yaml)

### Maxar Content Catalog API
Legacy Maxar Content Catalog API (doc.content.maxar.com/maxar-content-catalog.html), wrapped by the open-source `maxarcat` Python client.
- **SDK:** https://github.com/Maxar-Corp/maxarcat
- **Capability:** [capabilities/shared/catalog.yaml](capabilities/shared/catalog.yaml)

### Maxar Open Data STAC Catalog
Free public STAC catalog of pre-/post-event high-resolution imagery on AWS Open Data under CC-BY-NC 4.0.
- **Catalog:** https://maxar-opendata.s3.amazonaws.com/events/catalog.json
- **Index:** https://github.com/opengeos/maxar-open-data

### Maxar Transform API
Image transformation primitives (reproject, tile, mosaic, format-convert) — TypeScript clients published by Maxar-Corp.
- **SDK:** https://github.com/Maxar-Corp/transform-api-ts

## SDKs & Tooling

| SDK | Language | Coverage | Source |
| --- | -------- | -------- | ------ |
| MGP_SDK | Python | Streaming, Discovery, Ordering, Tasking, Monitoring, Account | [github.com/Maxar-Corp/maxar-geospatial-platform](https://github.com/Maxar-Corp/maxar-geospatial-platform) · [pypi.org/project/MGP-SDK](https://pypi.org/project/MGP-SDK/) |
| maxar-portal-java | Java | OGC Streaming (WMS/WMTS/WFS), Basemaps, Analytics | [github.com/Maxar-Corp/maxar-geospatial-platform-java](https://github.com/Maxar-Corp/maxar-geospatial-platform-java) |
| MGPSDK | R | Streaming, Account | [cran.r-project.org/web/packages/MGPSDK](https://cran.r-project.org/web/packages/MGPSDK/index.html) |
| maxarcat | Python | Legacy Content Catalog | [github.com/Maxar-Corp/maxarcat](https://github.com/Maxar-Corp/maxarcat) |
| @maxar/transform-api | TypeScript | Transform API | [github.com/Maxar-Corp/transform-api-ts](https://github.com/Maxar-Corp/transform-api-ts) |
| transform-ol-ts | TypeScript | OpenLayers helpers for Transform API | [github.com/Maxar-Corp/transform-ol-ts](https://github.com/Maxar-Corp/transform-ol-ts) |

## Integrations

- **QGIS Plugin** — https://hub.vantor.com/docs/integrations/qgis
- **ArcGIS Pro Plugin** — https://hub.vantor.com/docs/integrations/arcgispro
- **API Collection** — https://hub.vantor.com/docs/developer-tools/api-collection

## Common Resources

- [Vantor (corporate)](https://vantor.com/)
- [Legacy Maxar site](https://www.maxar.com/) (redirects to vantor.com)
- [Vantor Hub developer portal](https://hub.vantor.com/)
- [Legacy Maxar developer portal](https://pro.maxar.com/)
- [Hub Status Page](https://hub-status.vantor.com/)
- [Vantor Wikipedia](https://en.wikipedia.org/wiki/Vantor_(company))
- [Lanteris Space Systems Wikipedia](https://en.wikipedia.org/wiki/Lanteris_Space_Systems)
- [Advent International (owner)](https://www.adventinternational.com/)
- [Intuitive Machines (acquired Lanteris)](https://www.intuitivemachines.com/)
- GitHub orgs: [Maxar-Corp](https://github.com/Maxar-Corp) · [maxar-analytics](https://github.com/maxar-analytics) (archived) · [DigitalGlobe](https://github.com/DigitalGlobe) (legacy)

## Artifacts

### OpenAPI (7 specs)

- [Authentication](openapi/authentication-openapi.yml)
- [Discovery](openapi/discovery-openapi.yml)
- [Account Services / Admin](openapi/admin-openapi.yml)
- [Streaming (WMS/WMTS/WFS)](openapi/streaming-openapi.yml)
- [Ordering](openapi/ordering-openapi.yml)
- [Tasking](openapi/tasking-openapi.yml)
- [Monitoring](openapi/monitoring-openapi.yml)

### Naftiko Capabilities (8 shared + 1 workflow)

- Shared per-API: [authentication](capabilities/shared/authentication.yaml), [discovery](capabilities/shared/discovery.yaml), [admin](capabilities/shared/admin.yaml), [streaming](capabilities/shared/streaming.yaml), [ordering](capabilities/shared/ordering.yaml), [tasking](capabilities/shared/tasking.yaml), [monitoring](capabilities/shared/monitoring.yaml), [basemaps](capabilities/shared/basemaps.yaml), [catalog](capabilities/shared/catalog.yaml)
- Workflow: [satellite-imagery-pipeline](capabilities/satellite-imagery-pipeline.yaml) — discovery → estimate → order → poll → monitor, with tasking fallback when the archive is insufficient

### JSON Schema

- [STAC Item Schema](json-schema/maxar-technologies-stac-item-schema.json)
- [Order Schema](json-schema/maxar-technologies-order-schema.json)
- [Task Schema](json-schema/maxar-technologies-task-schema.json)
- [Monitor Schema](json-schema/maxar-technologies-monitor-schema.json)

### JSON Structure

- [STAC Item Structure](json-structure/maxar-technologies-stac-item-structure.json)
- [Order Structure](json-structure/maxar-technologies-order-structure.json)
- [Task Structure](json-structure/maxar-technologies-task-structure.json)

### JSON-LD

- [Maxar Technologies Context](json-ld/maxar-technologies-context.jsonld) — maps Vantor / Maxar concepts (corporate lineage, satellites, STAC, orders/tasks/monitors) to schema.org and STAC.

### Examples

- [auth-token-request](examples/auth-token-request.json) / [auth-token-response](examples/auth-token-response.json)
- [discovery-search-request](examples/discovery-search-request.json) / [discovery-search-response](examples/discovery-search-response.json)
- [order-place-request](examples/order-place-request.json) / [order-place-response](examples/order-place-response.json)
- [task-submit-request](examples/task-submit-request.json)
- [monitor-create-request](examples/monitor-create-request.json)

### Spectral Rules

- [maxar-technologies-rules.yml](rules/maxar-technologies-rules.yml) — HTTPS-only servers, bearer auth, Title-Case summaries/tags, camelCase operationIds.

### Vocabulary

- [maxar-technologies-vocabulary.yml](vocabulary/maxar-technologies-vocabulary.yml) — corporate lineage, satellites, products, API standards.

### Commercial

- [Plans & Pricing](plans/maxar-technologies-plans-pricing.yml) — Open Data (free, CC-BY-NC 4.0), Hub trial, MGP commercial (contact-sales), government & defense.
- [Rate Limits](rate-limits/maxar-technologies-rate-limits.yml) — not publicly published; documented as known unknowns.
- [FinOps](finops/maxar-technologies-finops.yml) — cost surface reconstructable from Account Services credit balance + per-order/task cost fields; no public FOCUS-conformant billing feed.

## Notable Absences

- **No public OpenAPI specs** published by Vantor on the developer portal; specs in this profile are reconstructed from documented endpoints, SDK shapes and OAuth/STAC conventions.
- **No public per-endpoint pricing or rate-limits** — everything routes through a "Contact Sales" funnel.
- **No public RSS / Atom feed** on hub.vantor.com or vantor.com/insights.
- **No active Maxar GitHub org for SDK PRs** — most repos in maxar-analytics are archived; Maxar-Corp activity is selective.
