# ReqRes (reqres)

ReqRes (reqres.in) is a hosted REST API originally launched by Ben Howdle as a free no-auth fake-API surface for AJAX prototyping, tutorials, and frontend testing. As of the 2025 relaunch it operates as a freemium SaaS product: every request to /api/* and /app/* now requires an x-api-key header obtained via free signup at app.reqres.in, while the /agent/v1/* Agent Sandbox is open in v1 with IP-based rate limiting. The legacy demo surface (/api/users, /api/login, /api/register, /api/unknown, delayed responses) continues to return the same fixture payloads it always has — what changed is the API-key gate and the addition of persistent collections, app users, custom endpoints, and an agent-targeted sandbox with deliberate failure scenarios. ReqRes remains the default fake-API endpoint cited in countless React, Vue, Angular, and bootcamp tutorials.

**APIs.json:** [https://reqres.in/](https://reqres.in/)

## Tags

- Development
- Testing
- Prototyping
- Fake API
- REST
- Agent Sandbox

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## APIs

### ReqRes API

Hosted REST surface spanning six business areas — Legacy demo data, Authentication simulation, Collections (persistent), App Users (sessions), Custom Endpoints, and the Agent Sandbox for AI coding agents. All /api/* requires x-api-key; /app/* additionally requires a session bearer; /agent/v1/* is open in v1.

- **Human URL:** [https://reqres.in/](https://reqres.in/)
- **Base URL:** `https://reqres.in/`

#### Tags

- REST
- Fake API
- Agent Sandbox

#### Properties

- [Documentation](https://reqres.in/docs)
- [Getting Started](https://reqres.in/)
- [Sign Up](https://app.reqres.in/)
- [Pricing](https://reqres.in/pricing)
- [Blog](https://reqres.in/blog/free-api-for-testing)
- [OpenAPI](openapi/reqres-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reqres.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reqres.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/reqres-legacy-user-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-legacy-unknown-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-auth-request-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-register-response-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-login-response-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-collection-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-collection-record-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-app-user-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-app-user-login-response-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-agent-user-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reqres-agent-pagination-meta-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/reqres-legacy-user-structure.json)
- [JSON Structure](json-structure/reqres-collection-structure.json)
- [JSON Structure](json-structure/reqres-collection-record-structure.json)
- [JSON Structure](json-structure/reqres-app-user-structure.json)
- [JSON Structure](json-structure/reqres-agent-user-structure.json)
- [JSON-LD](json-ld/reqres-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/reqres-legacy-user-example.json)
- [Example](examples/reqres-legacy-unknown-example.json)
- [Example](examples/reqres-register-response-example.json)
- [Example](examples/reqres-login-response-example.json)
- [Example](examples/reqres-collection-example.json)
- [Example](examples/reqres-collection-record-example.json)
- [Example](examples/reqres-app-user-example.json)
- [Example](examples/reqres-agent-user-example.json)

## Common Properties

- [Website](https://reqres.in/)
- [Getting Started](https://reqres.in/)
- [Documentation](https://reqres.in/docs)
- [Sign Up](https://app.reqres.in/)
- [Pricing](https://reqres.in/pricing)
- [Blog](https://reqres.in/blog)
- [GitHub Repository](https://github.com/benhowdle89/reqres-demo-app)
- [GitHub Repository](https://github.com/benhowdle89/reqres-waitlist-demo)
- [Git Hub User](https://github.com/benhowdle89)
- [LinkedIn](https://www.linkedin.com/in/ben-howdle)
- [Public APIs Listing](https://github.com/public-apis/public-apis)
- [Public A P I Dev Listing](https://publicapi.dev/req-res-api)
- [Plans](plans/reqres-plans-pricing.yml)
- [Rate Limits](rate-limits/reqres-rate-limits.yml)
- [Spectral Rules](rules/reqres-rules.yml)
- [Vocabulary](vocabulary/reqres-vocabulary.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
