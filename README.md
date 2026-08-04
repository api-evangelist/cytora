# Cytora (cytora)

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
