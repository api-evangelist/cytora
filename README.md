# Cytora

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Cytora is a London-headquartered insurtech, founded in 2012 as a University of Cambridge spinout, that sells a digital risk processing platform to commercial insurers, wholesale brokers, MGAs and reinsurers. Its software ingests inbound submissions arriving as email, PDF, spreadsheet and broker API payloads, digitises them against pre-built line-of-business schemas (property, commercial combined, construction, cyber, fleet, general liability, professional liability, D&O, E&O, management liability), augments them from a data ecosystem of roughly sixty third-party risk-data partners, evaluates them against appetite and priority rules, and routes them into downstream underwriting and claims systems. Use cases span new business, renewals, mid-term adjustments, claims FNOL and post-FNOL intake, and facultative and treaty reinsurance submissions. Named customers include Zurich, Chubb, Markel, Beazley, Travelers, Tokio Marine, Ecclesiastical, Arch, Everest and TransRe. Applied Systems acquired Cytora in September 2025. Its API posture is partner-gated and enterprise-only: Cytora runs a real production API gateway at api.cytora.com and a real ReadMe-hosted API reference at docs.cytora.com, but the documentation site is entirely password-protected (HTTP 302 to a password wall, robots.txt Disallow) and the gateway resets anonymous TLS connections. There is no self-serve developer signup, no public OpenAPI, no public Postman collection and no published webhook or event catalog. The only externally verifiable technical surface is the Auth0 OIDC discovery document at auth.cytora.com, which confirms OAuth 2.0 client-credentials and authorization-code flows for provisioned partner integrations. The United Kingdom home market has no open-insurance mandate, so nothing compels Cytora to expose any of this publicly.

**Areas:** Insurance · United Kingdom · Insurtech · Commercial Insurance · Underwriting · Claims · Risk Data · Property and Casualty · Reinsurance · Brokerage · Submission Intake · Document AI

## Cytora on APIs.io

Everything profiled for Cytora is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cytora/](https://apis.io/providers/cytora/)** — or go straight to one of the APIs or properties below.

### APIs (2)

- [Cytora Platform API](https://apis.io/apis/cytora/cytora-platform-api/) — Cytora's production REST API for digital risk processing — the "preferred method" of submission intake described in its own Risk Flow Academy. The gateway…
- [Cytora Identity (Auth0 OIDC)](https://apis.io/apis/cytora/cytora-identity-auth0-oidc/) — The OAuth 2.0 / OpenID Connect authorization server that fronts every Cytora integration, running on an Auth0 EU tenant (cytora-prod.eu.auth0.com). This is…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Moved to /providers/cytora/](https://apis.io/servers/cytora/cytora/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Cytora Authentication](https://apis.io/security/cytora/cytora-authentication/)
- [Cytora Domain Security](https://apis.io/security/cytora/cytora-domain-security/)
- [Cytora Trust Center](https://apis.io/security/cytora/cytora-trust-center/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Cytora Scopes](https://apis.io/scopes/cytora/cytora-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://cytora.com/)
- [Documentation](https://docs.cytora.com/)
- [Support](https://cytora.com/about-us/contact-us)
- [Blog](https://cytora.com/risk-flow-center/blog)
- [Compliance](https://trust.cytora.com/)
- [Trust centre](https://trust.cytora.com/)
- [Privacy policy](https://cytora.com/privacy-policy)
- [GitHub](https://github.com/cytora)
- [Status](https://status.cytora.com/)

## API Evangelist rating

**Kin Score 25.0** — emerging · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 68.3 |
| Contract quality | 0.0 |
| Contract governance | 18.2 |
| Operational transparency | 18.4 |
| Developer ergonomics | 19.0 |
| Access clarity | 32.9 |

**Agent readiness 23.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 37.7** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cytora/](https://apis.io/providers/cytora/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Cytora: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cytora/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
