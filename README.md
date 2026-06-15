# Track-POD (track-pod)

Track-POD is a cloud-based delivery management platform that combines route planning and optimization with electronic proof of delivery (ePOD), driver tracking, and last-mile customer notifications. The platform serves 10,000+ companies globally with a freemium model — the mobile driver app is free on iOS and Android, while the web dispatcher dashboard is sold on per-driver (Advanced, Advanced Plus, Ultimate, Enterprise) and per-order (S, M, L, XL) plans. Track-POD exposes a documented REST API (Track-POD API 2.0) with an OpenAPI 3.0 specification, JSON and XML payloads, X-API-KEY authentication, a public sandbox environment, and webhooks for ten event types covering orders, routes, and statuses. Common use cases include automated order import from e-commerce platforms (WooCommerce, Magento, Shopify, BigCommerce) and accounting/CRM systems (QuickBooks, Xero, Zoho, Microsoft Dynamics, Salesforce), real-time route dispatch and tracking, geotagged and signed proof of delivery, and PDF/shipping-label generation. Track-POD also ships no-code integrations via Zapier and Integrately.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/track-pod/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/track-pod/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- Delivery
- Last Mile
- Logistics
- Proof Of Delivery
- Electronic Proof Of Delivery
- EPOD
- Route Planning
- Route Optimization
- Dispatch
- Fleet Management
- Driver Tracking
- Courier
- Field Service
- Transportation
- Shipping

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Track-POD API

Track-POD API 2.0 is a JSON/XML REST API for delivery management. It covers eight resource families — Address, Driver, Order, RejectReason, Route, Test, Vehicle, and VehicleCheck — across 58 operations. Authentication uses an X-API-KEY header issued from Settings > Integrations > Web API. The same surface is offered against a sandbox tenant at api.sandbox.track-pod.com. Rate limits are 20 requests per second / 400 requests per minute. Restricted API keys can be scoped by IP address, HTTP method, and domain.

- **Human URL:** [https://api.track-pod.com/index.html](https://api.track-pod.com/index.html)
- **Base URL:** `https://api.track-pod.com`

#### Tags

- Delivery
- Orders
- Routes
- Drivers
- Vehicles
- Proof Of Delivery

#### Properties

- [Documentation](https://api.track-pod.com/index.html)
- [Sandbox](https://api.sandbox.track-pod.com/index.html)
- [OpenAPI](openapi/track-pod-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/track-pod.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/track-pod.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/track-pod-order-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/track-pod-route-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/track-pod-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/track-pod-rules.yml)
- [Example](examples/track-pod-create-order-example.json)
- [Vocabulary](vocabulary/track-pod-vocabulary.yml)

## Common Properties

- [Website](https://www.track-pod.com)
- [Documentation](https://api.track-pod.com/index.html)
- [Sandbox](https://api.sandbox.track-pod.com/index.html)
- [Getting Started](https://track-pod.freshdesk.com/support/solutions/articles/103000049813-track-pod-api-integration)
- [Authentication](https://track-pod.freshdesk.com/support/solutions/articles/103000049813-track-pod-api-integration)
- [Features](https://www.track-pod.com/features/)
- [Pricing](https://www.track-pod.com/pricing-delivery-app/)
- [Plans](plans/track-pod-plans-pricing.yml)
- [Rate Limits](rate-limits/track-pod-rate-limits.yml)
- [Fin Ops](finops/track-pod-finops.yml)
- [Webhooks](https://www.track-pod.com/blog/webhooks-api-integration/)
- [Integrations](https://www.track-pod.com/integrations/)
- [Zapier](https://zapier.com/apps/track-pod/integrations)
- [Help Center](https://track-pod.freshdesk.com/support/home)
- [Blog](https://www.track-pod.com/blog/)
- [Contact Us](https://www.track-pod.com/contact-us/)
- [Privacy Policy](https://www.track-pod.com/privacy-policy/)
- [Terms of Service](https://www.track-pod.com/terms-of-service/)
- [Sign Up](https://www.track-pod.com/free-trial/)
- [LinkedIn](https://www.linkedin.com/company/track-pod/)
- [Twitter](https://twitter.com/TrackPodApp)
- [Facebook](https://www.facebook.com/TrackPod/)
- [YouTube](https://www.youtube.com/c/TrackPod)
- [App Store](https://apps.apple.com/us/app/track-pod-driver-pod-app/id1112930649)
- [Play Store](https://play.google.com/store/apps/details?id=com.trackpod.android)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
