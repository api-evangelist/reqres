# ReqRes (reqres)

ReqRes (reqres.in) is a hosted REST API originally launched by Ben Howdle as a free no-auth fake-API surface for AJAX prototyping, tutorials, and frontend testing. As of the 2025 relaunch it operates as a freemium SaaS product: every request to /api/* and /app/* now requires an x-api-key header obtained via free signup at app.reqres.in, while the /agent/v1/* Agent Sandbox is open in v1 with IP-based rate limiting. The legacy demo surface (/api/users, /api/login, /api/register, /api/unknown, delayed responses) continues to return the same fixture payloads it always has — what changed is the API-key gate and the addition of persistent collections, app users, custom endpoints, and an agent-targeted sandbox with deliberate failure scenarios. ReqRes remains the default fake-API endpoint cited in countless React, Vue, Angular, and bootcamp tutorials.

**URL:** [Visit APIs.json URL](https://reqres.in/)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Development, Testing, Prototyping, Fake API, REST, Agent Sandbox

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## APIs

### ReqRes API

Hosted REST surface spanning six business areas — Legacy demo data, Authentication simulation, Collections (persistent), App Users (sessions), Custom Endpoints, and the Agent Sandbox for AI coding agents. All /api/* requires x-api-key; /app/* additionally requires a session bearer; /agent/v1/* is open in v1.

**Human URL:** [https://reqres.in/](https://reqres.in/)

#### Tags:

 - REST, Fake API, Agent Sandbox

#### Properties

- [Documentation](https://reqres.in/docs)
- [GettingStarted](https://reqres.in/)
- [SignUp](https://app.reqres.in/)
- [Pricing](https://reqres.in/pricing)
- [Blog](https://reqres.in/blog/free-api-for-testing)
- [OpenAPI](openapi/reqres-openapi.yml)
- [Legacy User Schema](json-schema/reqres-legacy-user-schema.json)
- [Legacy Unknown (Resource) Schema](json-schema/reqres-legacy-unknown-schema.json)
- [Auth Request Schema](json-schema/reqres-auth-request-schema.json)
- [Register Response Schema](json-schema/reqres-register-response-schema.json)
- [Login Response Schema](json-schema/reqres-login-response-schema.json)
- [Collection Schema](json-schema/reqres-collection-schema.json)
- [Collection Record Schema](json-schema/reqres-collection-record-schema.json)
- [App User Schema](json-schema/reqres-app-user-schema.json)
- [App User Login Response Schema](json-schema/reqres-app-user-login-response-schema.json)
- [Agent User Schema](json-schema/reqres-agent-user-schema.json)
- [Agent Pagination Meta Schema](json-schema/reqres-agent-pagination-meta-schema.json)
- [Legacy User Structure](json-structure/reqres-legacy-user-structure.json)
- [Collection Structure](json-structure/reqres-collection-structure.json)
- [Collection Record Structure](json-structure/reqres-collection-record-structure.json)
- [App User Structure](json-structure/reqres-app-user-structure.json)
- [Agent User Structure](json-structure/reqres-agent-user-structure.json)
- [JSONLD](json-ld/reqres-context.jsonld)
- [Legacy User Example](examples/reqres-legacy-user-example.json)
- [Legacy Unknown Example](examples/reqres-legacy-unknown-example.json)
- [Register Response Example](examples/reqres-register-response-example.json)
- [Login Response Example](examples/reqres-login-response-example.json)
- [Collection Example](examples/reqres-collection-example.json)
- [Collection Record Example](examples/reqres-collection-record-example.json)
- [App User Example](examples/reqres-app-user-example.json)
- [Agent User Example](examples/reqres-agent-user-example.json)
- [Naftiko Capability — Legacy](capabilities/reqres-legacy.yaml)
- [Naftiko Capability — Authentication](capabilities/reqres-authentication.yaml)
- [Naftiko Capability — Collections](capabilities/reqres-collections.yaml)
- [Naftiko Capability — App Users](capabilities/reqres-app-users.yaml)
- [Naftiko Capability — Custom Endpoints](capabilities/reqres-custom-endpoints.yaml)
- [Naftiko Capability — Agent Sandbox](capabilities/reqres-agent-sandbox.yaml)

## Common Properties

- [Website](https://reqres.in/)
- [GettingStarted](https://reqres.in/)
- [Documentation](https://reqres.in/docs)
- [SignUp](https://app.reqres.in/)
- [Pricing](https://reqres.in/pricing)
- [Blog](https://reqres.in/blog)
- [Demo App (Source)](https://github.com/benhowdle89/reqres-demo-app)
- [Waitlist Demo (Source)](https://github.com/benhowdle89/reqres-waitlist-demo)
- [Ben Howdle (Creator)](https://github.com/benhowdle89)
- [Ben Howdle on LinkedIn](https://www.linkedin.com/in/ben-howdle)
- [PublicAPIsListing](https://github.com/public-apis/public-apis)
- [PublicAPIDevListing](https://publicapi.dev/req-res-api)
- [Plans](plans/reqres-plans-pricing.yml)
- [RateLimits](rate-limits/reqres-rate-limits.yml)
- [SpectralRules](rules/reqres-rules.yml)
- [Vocabulary](vocabulary/reqres-vocabulary.yml)

## Features

| Name | Description |
|------|-------------|
| Legacy Demo Fixtures | Stable /api/users, /api/users/{id}, /api/unknown, /api/unknown/{id} fixture data preserved from the original reqres.in launch — the same payloads tutorials have been wired against for years. |
| Simulated Auth Flows | /api/register, /api/login, and /api/logout return success-shaped tokens without creating real accounts — drop-in for teaching auth patterns without standing up a real identity provider. |
| Persistent Collections | /api/collections/{slug}/records supports GET/POST/PUT/DELETE with real persistence on paid plans, with custom schemas on the Dev tier and above. |
| Project-Scoped App Users | /app/* surface lets each app user authenticate independently with a session bearer, so client-side prototypes can model real per-user isolation. |
| Custom Endpoints | /api/custom/{path} executes user-defined endpoints, letting builders shape arbitrary REST surfaces without writing backend code. |
| Agent Sandbox | /agent/v1/* exposes endpoints designed for AI coding agents — cursor pagination, deeply nested resources, deliberate failure scenarios, and deterministic seeded fixtures. |
| 15 Deliberate Failure Scenarios | The Agent Developer plan unlocks 15 failure scenarios on /agent/v1/scenarios so AI agents can be tested against timeouts, rate limits, validation errors, and pagination edge cases. |
| Delayed Responses | Legacy endpoints accept a ?delay=N query param to simulate slow upstream conditions — useful for spinner/loading-state testing. |
| HTTPS Only | Served exclusively over HTTPS at reqres.in. |
| CORS Enabled | All origins are allowed, making ReqRes safe to call directly from browser-based prototypes. |

## Use Cases

| Name | Description |
|------|-------------|
| Frontend Tutorial Endpoints | The default fake API cited in React, Vue, Angular, and Svelte tutorials when an author needs a real HTTP endpoint without standing up a backend. |
| Bootcamp Curriculum | Coding bootcamps wire exercises against ReqRes legacy endpoints so students can practice CRUD flows on a stable, free, no-signup surface. |
| API Client Test Suites | Use the legacy and Collections surfaces to exercise HTTP client libraries (fetch, axios, requests, OkHttp) against a real REST API. |
| Frontend-First Prototyping | Build a UI against persistent ReqRes collections before standing up a real backend; swap in a real API later by renaming the base URL. |
| AI Agent Testing | Test AI coding agents against the /agent/v1/* sandbox — cursor pagination, deliberate failures, deterministic seeded fixtures. |
| Sales Demos | Power live sales demos for tools that need to talk to an API without exposing customer data. |
| Workshop Sandboxes | Hands-on workshops where every participant needs a working API endpoint in under a minute. |

## Integrations

| Name | Description |
|------|-------------|
| Postman | Public Postman collections wrap ReqRes endpoints for quick HTTP exploration and learning. |
| Hoppscotch | Frequently used as the default example endpoint in HTTP clients including Hoppscotch and Insomnia. |
| MSW (Mock Service Worker) | Often paired with MSW so frontend tests can intercept and stub ReqRes traffic deterministically. |
| Claude Code / AI Coding Agents | The /agent/v1/* sandbox is purpose-built for AI coding agents like Claude Code, with deliberate failure scenarios and cursor pagination. |
| Cypress / Playwright | Browser E2E test suites use ReqRes as a stable upstream when writing tests that depend on real network traffic. |

## Solutions

| Name | Description |
|------|-------------|
| Self-Hosted Deployment | From $499/year per team, deploy ReqRes inside your own infrastructure with no external dependencies — useful for regulated environments that can't call a public service. |
| Scoped Per-Engineer API Keys | On the Team plan, issue scoped API keys per engineer with usage tracking, so a single project can attribute spend back to individuals. |
| Webhook Automations | On the Pro plan, configure webhooks that fire on collection data changes, letting ReqRes drive downstream pipelines as a prototyping backend. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [ReqRes API](openapi/reqres-openapi.yml)

### JSON Schema (40)

40 standalone JSON Schema files generated from `openapi/reqres-openapi.yml` covering Legacy, Authentication, Collections, App Users, Templates, and Agent Sandbox schemas. Browse [json-schema/](json-schema/).

### JSON Structure (40)

40 JSON Structure files (https://json-structure.org) generated from the JSON Schemas, providing strict typing and modular references. Browse [json-structure/](json-structure/).

### JSON-LD

- [ReqRes Context](json-ld/reqres-context.jsonld) — 114 terms mapping ReqRes property names to schema.org, Dublin Core, and the `reqres:` namespace

### Examples (40)

40 realistic JSON example payloads, one per schema, derived from the OpenAPI spec. Browse [examples/](examples/).

## Capabilities

Naftiko capabilities organized as one self-contained file per business surface. Every file ships with both a REST exposer (port 8080) and an MCP exposer (port 9090) routed inline through its own consumes block.

| Capability | File | Operations |
|------------|------|-----------:|
| ReqRes Legacy | [reqres-legacy.yaml](capabilities/reqres-legacy.yaml) | 8 |
| ReqRes Authentication | [reqres-authentication.yaml](capabilities/reqres-authentication.yaml) | 3 |
| ReqRes Collections | [reqres-collections.yaml](capabilities/reqres-collections.yaml) | 10 |
| ReqRes App Users | [reqres-app-users.yaml](capabilities/reqres-app-users.yaml) | 19 |
| ReqRes Custom Endpoints | [reqres-custom-endpoints.yaml](capabilities/reqres-custom-endpoints.yaml) | 5 |
| ReqRes Agent Sandbox | [reqres-agent-sandbox.yaml](capabilities/reqres-agent-sandbox.yaml) | 7 |

## Vocabulary

- [ReqRes Vocabulary](vocabulary/reqres-vocabulary.yml) — Unified taxonomy mapping 8 resources, 12 actions, 6 workflows, and 5 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [ReqRes Spectral Rules](rules/reqres-rules.yml) — 38 rules across 13 categories enforcing ReqRes API conventions (ReqRes title/summary prefix, /api+/app+/agent path prefixes, x-api-key header, page/per_page pagination, MIT license, OpenAPI 3.0.x)

## Plans

- [ReqRes Plans & Pricing](plans/reqres-plans-pricing.yml) — 7 plans (Free, Lite, Dev, Pro, Team, Agent Developer, Self-Hosted) captured using the API Commons Plans 0.1 schema

## Rate Limits

- [ReqRes Rate Limits](rate-limits/reqres-rate-limits.yml) — Per-plan daily / monthly quotas captured using the API Commons Rate Limits 0.1 schema

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
