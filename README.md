# Cytora (cytora)

Cytora is a London-headquartered insurtech, founded in 2012 as a University of Cambridge spinout, that sells a digital risk processing platform to commercial insurers, wholesale brokers, MGAs and reinsurers. Its software ingests inbound submissions arriving as email, PDF, spreadsheet and broker API payloads, digitises them against pre-built line-of-business schemas, augments them from a data ecosystem of roughly sixty third-party risk-data partners, evaluates them against appetite and priority rules, and routes them into downstream underwriting and claims systems. Applied Systems acquired Cytora in September 2025.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cytora/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cytora/refs/heads/main/apis.yml)

## Tags

- Insurance
- United Kingdom
- Insurtech
- Commercial Insurance
- Underwriting
- Claims
- Risk Data
- Property and Casualty
- Reinsurance
- Broker
- Submission Intake
- Document AI

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

**None listed — and that is the accurate record.**

Cytora is a genuinely API-centric product whose entire developer surface is closed to the public. No API is listed in `apis.yml` because none can be reached, read or signed up for without a contract.

What was confirmed:

| Surface | Host | Result |
| --- | --- | --- |
| API reference | `https://docs.cytora.com/` | HTTP 302 → `/password?redirect=/` — "Cytora Platform Documentation / Password Protected". ReadMe-hosted, `robots.txt: Disallow: /`. A real reference site behind a password wall, not a self-serve developer portal. |
| API gateway | `https://api.cytora.com/` | Resolves via `gateway.cytora-prod.com` to a Google Cloud load balancer. TCP 443 open, TLS handshake reset for anonymous clients. Real gateway, not publicly reachable. |
| Authorization server | `https://auth.cytora.com/` | HTTP 200. Auth0 EU tenant (`cytora-prod.eu.auth0.com`) serving a full OIDC discovery document — the only anonymously readable machine-readable artifact Cytora publishes. |
| Status page | `https://status.cytora.com/` | HTTP 200 |
| Trust center | `https://trust.cytora.com/` | HTTP 200 |

`developer.cytora.com`, `developers.cytora.com`, `platform.cytora.com`, `app.cytora.com` and `console.cytora.com` do not resolve. `cytora.com/developers`, `/developer`, `/api`, `/partners` and `/integrations` all return 404.

**OpenAPI specifications harvested: 0.** Every spec path probed on `docs.cytora.com` (`/openapi.json`, `/openapi.yaml`, `/swagger.json`, `/api-docs`, `/spec`, `/cytora-platform/openapi.json`, `/sitemap.xml`) returns the password wall. There is no `openapi/` directory in this repo because nothing real was found.

## ACORD Posture

**No ACORD reference found — Cytora ships proprietary per-line-of-business schemas instead.**

Zero occurrences of ACORD, AL3, ACORD XML, NGDS, IVANS, Applied Epic, Vertafore or AMS360 across every public Cytora page inspected. In place of ACORD, Cytora publishes its own pre-built schemas as marketing pages under `/schemas/` — commercial-combined, construction, cyber-eu, cyber-us, directors-officers, errors-omissions, fleet, general-liability, management-liability, professional-liability and property. Those pages list human-readable field names and descriptions but publish no machine-readable schema, JSON Schema or download.

For context only: Cytora's acquirer Applied Systems operates in the ACORD/IVANS agency-download world via Applied Epic, and Duck Creek Technologies appears as a named system-provider partner in Cytora's data ecosystem. Neither is an ACORD claim made by Cytora.

## Quote / Bind / Issue / FNOL

None of the four canonical insurance verbs is exposed on a public API. Cytora sits **upstream** of them: its verb is intake and digitisation of the submission, then routing into the customer's own underwriting, policy administration and claims systems. FNOL and post-FNOL claim-submission intake is a prominently marketed capability with out-of-the-box claim schemas, but it is delivered inside the platform to contracted customers. The audience is partner and enterprise customer — not consumer, not openly agent-facing.

## Auth Model

OAuth 2.0 / OpenID Connect via an Auth0 EU tenant at `https://auth.cytora.com/`. Discovery, OAuth authorization-server metadata and JWKS all return HTTP 200 anonymously. Grants advertised include `client_credentials` (consistent with per-customer machine-to-machine partner integrations) and `authorization_code`, with PKCE `S256`, `private_key_jwt` client authentication and DPoP `ES256`. Only stock OIDC identity scopes are advertised — no product or resource scopes are published. Credentials cannot be obtained without a contract.

## Webhooks, Events, SDKs, Postman

No public webhook documentation, event catalog or AsyncAPI document. No public Postman collection or workspace. No SDK, client library or CLI. The `github.com/cytora` organization holds 39 public repos but they are legacy engineering forks and internal tooling from 2014-2023 with no API artifacts.

## Market Context

The United Kingdom has the FCA and PRA but no open-insurance obligation; the FCA's Open Finance work remains consultation rather than rule. Nothing compels a UK insurtech to publish an API. Cytora's closed posture is the market-normal outcome — notable mainly because Cytora is one of the most genuinely API-centric products in UK commercial insurance while publishing none of it.

## Links

- [Website](https://cytora.com/)
- [Documentation (password-gated)](https://docs.cytora.com/)
- [Blog](https://cytora.com/risk-flow-center/blog)
- [Status Page](https://status.cytora.com/)
- [Trust Center](https://trust.cytora.com/)
- [Authentication (OIDC discovery)](https://auth.cytora.com/.well-known/openid-configuration)
- [GitHub Organization](https://github.com/cytora)
- [LinkedIn](https://www.linkedin.com/company/cytora)
- [Privacy Policy](https://cytora.com/privacy-policy)
- [Contact](https://cytora.com/about-us/contact-us)
