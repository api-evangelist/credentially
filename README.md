# Credentially

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

Credentially is a UK-founded, healthcare-only onboarding and compliance automation platform used by NHS trusts, private providers, urgent care and clinical staffing agencies in the UK and US. It brings pre-employment checks, DBS and right-to-work validation, primary source verification, credentialing and continuous compliance monitoring onto one platform, cutting the platform-managed steps of onboarding clinical staff from an industry average of around 60 days to as little as 5. The Credentially Public API (OpenAPI 3.1) exposes profiles, placements, documents with OCR auto-fill, DBS checks, references, right-to-work status and compliance packages, with a companion Webhook API for state-change events.

**Areas:** Healthcare · Credentialing · Compliance · Onboarding · Workforce · Identity Verification · Background Checks · NHS · Company

## Credentially on APIs.io

Everything profiled for Credentially is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/credentially/](https://apis.io/providers/credentially/)** — or go straight to one of the APIs or properties below.

### APIs (21)

- [Credentially Compliance-packages API](https://apis.io/apis/credentially/credentially-compliance-packages-api/) — Profile's compliance packages management proxy endpoints
- [Credentially DBS API](https://apis.io/apis/credentially/credentially-dbs-api/) — DBS check lookup and refresh endpoints
- [Credentially Dictionary API](https://apis.io/apis/credentially/credentially-dictionary-api/) — Dictionary lookup endpoints for custom profile field values
- [Credentially Document Auto-fill API](https://apis.io/apis/credentially/credentially-document-auto-fill-api/) — Automated document data extraction and validation endpoints
- [Credentially Documents API](https://apis.io/apis/credentially/credentially-documents-api/) — Document management proxy endpoints
- [Credentially Employee Placements API](https://apis.io/apis/credentially/credentially-employee-placements-api/) — Placement data scoped to a specific employee.
- [Credentially Jurisdictions API](https://apis.io/apis/credentially/credentially-jurisdictions-api/) — Org-scoped jurisdictions a placement can reference (read-only).
- [Credentially Location Types API](https://apis.io/apis/credentially/credentially-location-types-api/) — Org-scoped classifications for placement locations (read-only).
- [Credentially Locations API](https://apis.io/apis/credentially/credentially-locations-api/) — Facilities / sites where placements occur. Each belongs to one jurisdiction.
- [Credentially Meta API](https://apis.io/apis/credentially/credentially-meta-api/) — API for fetching metadata
- [Credentially Organisation Groups API](https://apis.io/apis/credentially/credentially-organisation-groups-api/) — Organisation group member management endpoints
- [Credentially Placement Notes API](https://apis.io/apis/credentially/credentially-placement-notes-api/) — Notes attached to a placement — free-text annotations.
- [Credentially Placement Roles API](https://apis.io/apis/credentially/credentially-placement-roles-api/) — Org-scoped roles a placement can reference (e.g. Band 6 RN).
- [Credentially Placements API](https://apis.io/apis/credentially/credentially-placements-api/) — Placement lifecycle proxy endpoints — assignment of an employee to a location + role within the organisation.
- [Credentially Profile Groups API](https://apis.io/apis/credentially/credentially-profile-groups-api/) — Organisation groups proxy endpoints
- [Credentially Profiles API](https://apis.io/apis/credentially/credentially-profiles-api/) — Profile management proxy endpoints
- [Credentially References API](https://apis.io/apis/credentially/credentially-references-api/) — Profile reference status lookup endpoints
- [Credentially Right to Work API](https://apis.io/apis/credentially/credentially-right-to-work-api/) — Right to work status lookup endpoints
- [Credentially Stage Placements API](https://apis.io/apis/credentially/credentially-stage-placements-api/) — Placements scoped to a Kanban stage — board column reads + bulk-move.
- [Credentially Stages API](https://apis.io/apis/credentially/credentially-stages-api/) — Kanban placement stages — per-org column definitions for the placements board.
- [Credentially Subscriptions API](https://apis.io/apis/credentially/credentially-subscriptions-api/) — API for managing webhook callback subscriptions

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Credentially Webhooks](https://apis.io/asyncapis/credentially/credentially-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [credentially](https://apis.io/servers/credentially/credentially/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Credentially Agentic Access](https://apis.io/agentic-access/credentially/credentially-agentic-access/)

#### Collections (21)

Postman and Open Collection request collections.

- [Credentially Public Compliance-packages API](https://apis.io/collections/credentially/open-credentially-compliance-packages-api/)
- [Credentially Public Compliance-packages DBS API](https://apis.io/collections/credentially/open-credentially-dbs-api/)
- [Credentially Public Compliance-packages Dictionary API](https://apis.io/collections/credentially/open-credentially-dictionary-api/)
- [Credentially Public Compliance-packages Document Auto-fill API](https://apis.io/collections/credentially/open-credentially-document-auto-fill-api/)
- [Credentially Public Compliance-packages Documents API](https://apis.io/collections/credentially/open-credentially-documents-api/)
- [Credentially Public Compliance-packages Employee Placements API](https://apis.io/collections/credentially/open-credentially-employee-placements-api/)
- [Credentially Public Compliance-packages Jurisdictions API](https://apis.io/collections/credentially/open-credentially-jurisdictions-api/)
- [Credentially Public Compliance-packages Location Types API](https://apis.io/collections/credentially/open-credentially-location-types-api/)
- [Credentially Public Compliance-packages Locations API](https://apis.io/collections/credentially/open-credentially-locations-api/)
- [Credentially Public Compliance-packages Meta API](https://apis.io/collections/credentially/open-credentially-meta-api/)
- [Credentially Public Compliance-packages Organisation Groups API](https://apis.io/collections/credentially/open-credentially-organisation-groups-api/)
- [Credentially Public Compliance-packages Placement Notes API](https://apis.io/collections/credentially/open-credentially-placement-notes-api/)
- [Credentially Public Compliance-packages Placement Roles API](https://apis.io/collections/credentially/open-credentially-placement-roles-api/)
- [Credentially Public Compliance-packages Placements API](https://apis.io/collections/credentially/open-credentially-placements-api/)
- [Credentially Public Compliance-packages Profile Groups API](https://apis.io/collections/credentially/open-credentially-profile-groups-api/)
- [Credentially Public Compliance-packages Profiles API](https://apis.io/collections/credentially/open-credentially-profiles-api/)
- [Credentially Public Compliance-packages References API](https://apis.io/collections/credentially/open-credentially-references-api/)
- [Credentially Public Compliance-packages Right to Work API](https://apis.io/collections/credentially/open-credentially-right-to-work-api/)
- [Credentially Public Compliance-packages Stage Placements API](https://apis.io/collections/credentially/open-credentially-stage-placements-api/)
- [Credentially Public Compliance-packages Stages API](https://apis.io/collections/credentially/open-credentially-stages-api/)
- [Credentially Public Compliance-packages Subscriptions API](https://apis.io/collections/credentially/open-credentially-subscriptions-api/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Credentially Gateway Overlay](https://apis.io/overlays/credentially/credentially-gateway-overlay/)
- [Credentially Webhook Overlay](https://apis.io/overlays/credentially/credentially-webhook-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Credentially Authentication](https://apis.io/security/credentially/credentially-authentication/)
- [Credentially Domain Security](https://apis.io/security/credentially/credentially-domain-security/)
- [Credentially Trust Center](https://apis.io/security/credentially/credentially-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Credentially Plans Pricing](https://apis.io/plans/credentially/credentially-plans-pricing/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://credentially.io/)
- [Documentation](https://credentially.readme.io/)
- [Getting started](https://credentially.readme.io/reference/getting-started-with-your-api)
- [API reference](https://credentially.readme.io/reference/getting-started-with-your-api)
- [Pricing](https://www.credentially.io/pricing)
- [Sign up](https://www.credentially.io/book-a-demo)
- [Support](https://credentially.my.site.com/s/KnowledgeHub)
- [Blog](https://www.credentially.io/blog)
- [Compliance](https://www.credentially.io/security)
- [Terms of service](https://www.credentially.io/terms-policies/terms-of-use)
- [Privacy policy](https://www.credentially.io/terms-policies/privacy-policy)
- [GitHub](https://github.com/Credentially)
- [Status](https://status.credentially.io/)

## API Evangelist rating

**Kin Score 52.9** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 62.1 |
| Contract governance | 18.2 |
| Operational transparency | 26.3 |
| Developer ergonomics | 48.2 |
| Access clarity | 60.5 |

**Agent readiness 35.1** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | verified |
| Rate Limit Signal | verified |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 27.3** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/credentially/](https://apis.io/providers/credentially/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Credentially: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/credentially/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
