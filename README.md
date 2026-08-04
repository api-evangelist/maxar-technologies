# Maxar Technologies (maxar-technologies)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Maxar Technologies was a publicly traded Earth-imaging and space-systems company formed from the 2017 merger of MacDonald, Dettwiler and Associates (MDA) with DigitalGlobe (founded 1992 in Oakland, California). In December 2022 private-equity firm Advent International agreed to take Maxar private in a USD 6.4 billion cash deal that closed in May 2023, after which Advent split the company into two operating units: Maxar Intelligence (imagery and geospatial software in Westminster, Colorado) and Maxar Space Systems (satellite manufacturing in Palo Alto, California). On 1 October 2025 both units rebranded — Maxar Intelligence became Vantor and Maxar Space Systems became Lanteris Space Systems. On 13 January 2026 Intuitive Machines completed the acquisition of Lanteris from Advent for approximately USD 800 million, leaving Vantor as the sole remaining Advent-owned successor of the Maxar brand. The public developer surface for the original Maxar APIs — imagery search, streaming (WMS/WMTS/WFS), tasking, ordering, monitoring, authentication and account services — is now delivered through the Vantor Hub (hub.vantor.com / pro.maxar.com) and the Maxar Geospatial Platform (MGP) SDKs (Python, Java, R). The Maxar Open Data Program continues to publish a public STAC catalog of pre-/post-event high-resolution imagery on AWS Open Data.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/maxar-technologies/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/maxar-technologies/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Satellite Imagery
- Earth Observation
- Geospatial
- Remote Sensing
- Spatial Intelligence
- Defense
- Intelligence
- WorldView
- STAC
- OGC
- WMS
- WMTS
- WFS
- Tasking
- Basemaps
- Vantor
- Lanteris
- Advent International
- Private Equity

## Timestamps

- **Created:** 2026-05-22
- **Modified:** 2026-05-23

## APIs

### Vantor Hub Authentication API

OAuth-style token service that issues bearer access tokens for use with every other Vantor Hub API (Discovery, Account Services, Streaming). Documented at hub.vantor.com/docs/authentication and delivered via the Vantor Hub developer portal (formerly developers.maxar.com).

- **Human URL:** [https://hub.vantor.com/docs/authentication/](https://hub.vantor.com/docs/authentication/)
- **Base URL:** `https://api.maxar.com`

#### Tags

- Authentication
- OAuth
- Tokens
- Vantor Hub

#### Properties

- [Documentation](https://hub.vantor.com/docs/authentication/)
- [Developer Portal](https://hub.vantor.com/)
- [OpenAPI](openapi/authentication-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/authentication.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/authentication.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Capability](capabilities/shared/authentication.yaml)

### Vantor Hub Discovery API

Search and discovery API across Vantor's "125+ petabytes of imagery and derivatives" — high-resolution electro-optical imagery from the WorldView and GeoEye constellations, WorldView Legion (six next-generation satellites launched 2024-2026), basemaps and derivative analytic products. STAC-aligned search by area of interest, time window, sensor, cloud cover, resolution and other filters.

- **Human URL:** [https://hub.vantor.com/docs/discovery/](https://hub.vantor.com/docs/discovery/)
- **Base URL:** `https://api.maxar.com/discovery/v1`

#### Tags

- Discovery
- Search
- STAC
- Imagery
- Catalog

#### Properties

- [Documentation](https://hub.vantor.com/docs/discovery/)
- [OpenAPI](openapi/discovery-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/discovery.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/discovery.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Capability](capabilities/shared/discovery.yaml)

### Vantor Hub Account Services API

Administrative account-management API for Vantor Hub customers — manage users, roles, organisation entitlements, credit balances and API keys against the Vantor Hub tenant. Documented as the Account Services / Admin API under the Vantor Hub developer portal.

- **Human URL:** [https://hub.vantor.com/docs/admin/](https://hub.vantor.com/docs/admin/)
- **Base URL:** `https://api.maxar.com/admin/v1`

#### Tags

- Admin
- Accounts
- Users
- Entitlements

#### Properties

- [Documentation](https://hub.vantor.com/docs/admin/)
- [OpenAPI](openapi/admin-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Capability](capabilities/shared/admin.yaml)

### Maxar Geospatial Platform Streaming API

OGC-standards Streaming services exposing Maxar's current and historical imagery as WMS (Web Map Service), WMTS (Web Map Tile Service) and WFS (Web Feature Service) layers — supports GetCapabilities, GetMap, GetTile, GetFeature and bulk image download. Surfaced through the MGP_SDK Python, Java and R clients.

- **Human URL:** [https://maxar-geospatial-platform.readthedocs.io/en/latest/](https://maxar-geospatial-platform.readthedocs.io/en/latest/)
- **Base URL:** `https://securewatch.maxar.com/earthservice`

#### Tags

- Streaming
- WMS
- WMTS
- WFS
- OGC
- Imagery

#### Properties

- [Documentation](https://maxar-geospatial-platform.readthedocs.io/en/latest/)
- [SDK](https://github.com/Maxar-Corp/maxar-geospatial-platform)
- [OpenAPI](openapi/streaming-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/streaming.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/streaming.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Capability](capabilities/shared/streaming.yaml)

### Maxar Geospatial Platform Ordering API

Order management API for placing, tracking and retrieving deliveries of Maxar archive imagery — supports asynchronous orders against the WorldView / GeoEye / WorldView Legion archive with output to S3 or direct download. Exposed via the MGP_SDK Interface.ordering surface.

- **Human URL:** [https://maxar-geospatial-platform.readthedocs.io/en/latest/](https://maxar-geospatial-platform.readthedocs.io/en/latest/)
- **Base URL:** `https://api.maxar.com/order/v1`

#### Tags

- Ordering
- Archive
- Imagery
- Async

#### Properties

- [Documentation](https://maxar-geospatial-platform.readthedocs.io/en/latest/)
- [SDK](https://github.com/Maxar-Corp/maxar-geospatial-platform)
- [OpenAPI](openapi/ordering-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ordering.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ordering.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Capability](capabilities/shared/ordering.yaml)

### Maxar Geospatial Platform Tasking API

Real-time tasking API for commissioning new satellite collections over an area of interest using the Vantor Constellation (WorldView-1/2/3, GeoEye-1 and the six-satellite WorldView Legion next-generation fleet delivering 30 cm-class native resolution). Supports priority levels, collection windows and delivery targets.

- **Human URL:** [https://maxar-geospatial-platform.readthedocs.io/en/latest/](https://maxar-geospatial-platform.readthedocs.io/en/latest/)
- **Base URL:** `https://api.maxar.com/tasking/v1`

#### Tags

- Tasking
- Collection
- WorldView Legion
- Real-Time

#### Properties

- [Documentation](https://maxar-geospatial-platform.readthedocs.io/en/latest/)
- [SDK](https://github.com/Maxar-Corp/maxar-geospatial-platform)
- [OpenAPI](openapi/tasking-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tasking.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tasking.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Capability](capabilities/shared/tasking.yaml)

### Maxar Geospatial Platform Monitoring API

Monitoring API for standing watches over user-defined areas of interest — receive notifications when new imagery is collected, when collection windows close, and when analytic detections fire. Exposed via the MGP_SDK Interface.monitoring surface.

- **Human URL:** [https://maxar-geospatial-platform.readthedocs.io/en/latest/](https://maxar-geospatial-platform.readthedocs.io/en/latest/)
- **Base URL:** `https://api.maxar.com/monitoring/v1`

#### Tags

- Monitoring
- Notifications
- AOI
- Webhooks

#### Properties

- [Documentation](https://maxar-geospatial-platform.readthedocs.io/en/latest/)
- [SDK](https://github.com/Maxar-Corp/maxar-geospatial-platform)
- [OpenAPI](openapi/monitoring-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monitoring.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monitoring.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Capability](capabilities/shared/monitoring.yaml)

### Maxar Vivid Basemap API

Vivid is Maxar's cloud-free, color-balanced basemap product — a global mosaic refreshed from the WorldView archive. The Vivid Basemap API exposes the basemap as OGC tile and feature services through the MGP streaming surface. Documented as part of the Vantor "Dynamic Foundation" product family.

- **Human URL:** [https://vantor.com/](https://vantor.com/)
- **Base URL:** `https://securewatch.maxar.com/earthservice`

#### Tags

- Basemaps
- Vivid
- Mosaic
- Streaming

#### Properties

- [Documentation](https://maxar-geospatial-platform.readthedocs.io/en/latest/)
- [SDK](https://github.com/Maxar-Corp/maxar-geospatial-platform)
- [Capability](capabilities/shared/basemaps.yaml)
- [Postman Collection](collections/admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/authentication.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/authentication.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/discovery.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/discovery.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monitoring.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monitoring.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/ordering.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ordering.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/streaming.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/streaming.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/tasking.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tasking.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Maxar Content Catalog API

Legacy Maxar Content Catalog API — the canonical search index against the WorldView / GeoEye / IKONOS / QuickBird archive. Generated from Maxar's published OpenAPI spec (doc.content.maxar.com/maxar-content- catalog.html) and wrapped by the open-source `maxarcat` Python client.

- **Human URL:** [https://doc.content.maxar.com/maxar-content-catalog.html](https://doc.content.maxar.com/maxar-content-catalog.html)
- **Base URL:** `https://api.content.maxar.com/catalog`

#### Tags

- Catalog
- Search
- Archive
- Legacy

#### Properties

- [Documentation](https://doc.content.maxar.com/maxar-content-catalog.html)
- [SDK](https://github.com/Maxar-Corp/maxarcat)
- [Package](https://pypi.org/project/maxarcat)
- [Capability](capabilities/shared/catalog.yaml)
- [Postman Collection](collections/admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/authentication.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/authentication.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/discovery.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/discovery.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monitoring.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monitoring.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/ordering.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ordering.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/streaming.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/streaming.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/tasking.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tasking.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Maxar Open Data STAC Catalog

Free, public STAC (SpatioTemporal Asset Catalog) of pre- and post-event high-resolution Maxar imagery published in support of emergency planning, risk assessment, damage assessment and recovery. Hosted on AWS Open Data as Cloud Optimized GeoTIFFs (COGs) with STAC JSON metadata and mirrored via the community `opengeos/maxar-open-data` index.

- **Human URL:** [https://github.com/opengeos/maxar-open-data](https://github.com/opengeos/maxar-open-data)
- **Base URL:** `https://maxar-opendata.s3.amazonaws.com`

#### Tags

- Open Data
- STAC
- COG
- Disaster Response
- AWS Open Data

#### Properties

- [Documentation](https://github.com/opengeos/maxar-open-data)
- [Catalog](https://maxar-opendata.s3.amazonaws.com/events/catalog.json)
- [License](https://creativecommons.org/licenses/by-nc/4.0/)
- [Postman Collection](collections/admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/authentication.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/authentication.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/discovery.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/discovery.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monitoring.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monitoring.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/ordering.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ordering.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/streaming.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/streaming.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/tasking.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tasking.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Maxar Transform API

Transform API exposes image transformation primitives (reproject, tile, mosaic, format-convert) over Maxar imagery. A TypeScript client (@maxar/transform-api) and OpenLayers helpers are published from github.com/Maxar-Corp/transform-api-ts and transform-ol-ts.

- **Human URL:** [https://github.com/Maxar-Corp/transform-api-ts](https://github.com/Maxar-Corp/transform-api-ts)
- **Base URL:** `https://api.maxar.com/transform/v1`

#### Tags

- Transform
- Imagery
- Reproject
- Tiles

#### Properties

- [SDK](https://github.com/Maxar-Corp/transform-api-ts)
- [SDK](https://github.com/Maxar-Corp/transform-ol-ts)
- [Package](https://www.npmjs.com/package/@maxar/transform-api)
- [Postman Collection](collections/admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/authentication.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/authentication.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/discovery.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/discovery.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monitoring.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monitoring.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/ordering.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ordering.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/streaming.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/streaming.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/tasking.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tasking.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://vantor.com/)
- [Legacy Website](https://www.maxar.com/)
- [Developer Portal](https://hub.vantor.com/)
- [Legacy Developer Portal](https://pro.maxar.com/)
- [Documentation](https://hub.vantor.com/docs/)
- [SDK](https://github.com/Maxar-Corp/maxar-geospatial-platform)
- [SDK](https://github.com/Maxar-Corp/maxar-geospatial-platform-java)
- [SDK](https://github.com/Maxar-Corp/maxar-geospatial-platform-r)
- [SDK](https://github.com/Maxar-Corp/maxarcat)
- [Package](https://pypi.org/project/MGP-SDK/)
- [Package](https://cran.r-project.org/web/packages/MGPSDK/index.html)
- [Git Hub](https://github.com/Maxar-Corp)
- [Git Hub Legacy](https://github.com/DigitalGlobe)
- [Git Hub Analytics](https://github.com/maxar-analytics)
- [Status Page](https://hub-status.vantor.com/)
- [Changelog](https://hub.vantor.com/docs/release-notes)
- [Integrations](https://hub.vantor.com/docs/integrations/qgis)
- [Integrations](https://hub.vantor.com/docs/integrations/arcgispro)
- [Sample Projects](https://hub.vantor.com/sample-projects/)
- [A P I Collection](https://hub.vantor.com/docs/developer-tools/api-collection)
- [Login](https://hub.vantor.com/)
- [Login](https://discover.vantor.com/)
- [Contact](https://vantor.com/get-started/)
- [Open Data](https://github.com/opengeos/maxar-open-data)
- [Successor Intelligence](https://vantor.com/)
- [Successor Space Systems](https://en.wikipedia.org/wiki/Lanteris_Space_Systems)
- [Owner](https://www.adventinternational.com/)
- [Acquirer Space Systems](https://www.intuitivemachines.com/)
- [Wikipedia](https://en.wikipedia.org/wiki/Vantor_(company))
- [Wikipedia Lanteris](https://en.wikipedia.org/wiki/Lanteris_Space_Systems)
- [Plans](plans/maxar-technologies-plans-pricing.yml)
- [Rate Limits](rate-limits/maxar-technologies-rate-limits.yml)
- [Fin Ops](finops/maxar-technologies-finops.yml)
- [Vocabulary](vocabulary/maxar-technologies-vocabulary.yml)
- [JSON-LD](json-ld/maxar-technologies-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
