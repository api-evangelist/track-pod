# Track-POD

Track-POD is a cloud-based delivery management platform combining route planning and optimization with electronic proof of delivery (ePOD), driver tracking, and last-mile customer notifications. The Track-POD API 2.0 exposes the platform's order, route, driver, vehicle, and inspection data via a documented REST surface with JSON/XML, X-API-KEY authentication, and a public sandbox tenant.

- Website — https://www.track-pod.com
- API documentation — https://api.track-pod.com/index.html
- Sandbox — https://api.sandbox.track-pod.com/index.html
- Pricing — https://www.track-pod.com/pricing-delivery-app/

## API Surface

| Resource family | Operations | Notes |
| --- | --- | --- |
| Address | 1 | Upsert customer address records used by orders and routes |
| Driver | 7 | List/CRUD by id or username |
| Order | 27 | Create, bulk-create (≤500), update, lookup by Number/Id/TrackId/Date, Complete, Reject, POD PDF, shipping label |
| RejectReason | 1 | Catalog of rejection reasons |
| Route | 28 | CRUD, attach orders, start/ready/close, track, export workflow, custom-field patches |
| Test | 1 | Auth + rate-limit self-check |
| Vehicle | 5 | List/CRUD |
| VehicleCheck | 3 | Driver walk-around inspections by vehicle or date |

Total: **58 documented operations** across 8 resource families (OpenAPI 3.0.4).

## Webhooks

Track-POD delivers webhooks for 10 event types: `Create order`, `Update order`, `Delete order`, `Create route`, `Update route`, `Delete route`, `Update order status`, `Start route`, `Close route`, `Optimize route`. Payloads carry `Metadata` + `Data` sections and failed deliveries are retried up to five times.

## Authentication and Limits

- **Auth** — `X-API-KEY` header, issued from `Settings > Integrations > Web API`. Restricted keys can be scoped by IP address, HTTP method, and domain.
- **Rate limits** — 20 requests/second and 400 requests/minute per API key.
- **Bulk import** — Up to 500 orders per `POST /Order/Bulk` call.

## Pricing (May 2026)

Track-POD ships two parallel pricing families:

| Plan | Family | Rate (annual / monthly) | Included orders | Web users |
| --- | --- | --- | --- | --- |
| Advanced | Per driver | $49 / $59 per driver/mo | 6,000/mo | 7 |
| Advanced Plus | Per driver | $69 / $79 per driver/mo | unlimited | 50 |
| Ultimate | Per driver | $89 / $99 per driver/mo | unlimited | 100 |
| Enterprise | Per driver | Custom (20+ drivers) | unlimited | unlimited |
| S Plan | Per order | $285/mo ($0.19/order) | 1,500/mo | 50 |
| M Plan | Per order | $510/mo ($0.17/order) | 3,000/mo | 50 |
| L Plan | Per order | $900/mo ($0.15/order) | 6,000/mo | 50 |
| XL Plan | Per order | $1,440/mo ($0.12/order) | 12,000/mo | 100 |

## Repository Contents

| Path | What's in it |
| --- | --- |
| [apis.yml](apis.yml) | APIs.json provider record |
| [openapi/track-pod-openapi.yml](openapi/track-pod-openapi.yml) | OpenAPI 3.0.4 spec mirrored from `api.track-pod.com/swagger/v1/swagger.json` |
| [capabilities/](capabilities/) | Naftiko capability definitions for Orders, Routes, Drivers, Vehicles, Addresses, Vehicle Checks |
| [json-schema/](json-schema/) | JSON Schemas for Order, Route, and VehicleCheck |
| [json-structure/](json-structure/) | Functional grouping of Order properties |
| [json-ld/track-pod-context.jsonld](json-ld/track-pod-context.jsonld) | JSON-LD context aligning Track-POD entities with schema.org |
| [examples/](examples/) | Request/response examples for creating and completing orders |
| [rules/track-pod-rules.yml](rules/track-pod-rules.yml) | Spectral ruleset enforcing Track-POD API conventions |
| [vocabulary/track-pod-vocabulary.yml](vocabulary/track-pod-vocabulary.yml) | Domain vocabulary covering delivery, ePOD, lifecycle, and pricing terms |
| [plans/track-pod-plans-pricing.yml](plans/track-pod-plans-pricing.yml) | API Commons Plans 0.1 reconciliation of Track-POD pricing |
| [rate-limits/track-pod-rate-limits.yml](rate-limits/track-pod-rate-limits.yml) | API Commons Rate Limits 0.1 record of throttling and quotas |
| [finops/track-pod-finops.yml](finops/track-pod-finops.yml) | FOCUS-aligned FinOps mapping for Track-POD billing |

## Maintainer

Kin Lane — API Evangelist — kin@apievangelist.com
