# Storable

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

Storable is the leading technology provider for the self-storage industry, serving 33,000+ facilities through a family of brands - SiteLink (legacy Web Edition property management, sold with a partner/NDA-gated SOAP API), storEDGE (modern cloud property management with a documented REST API at api.storedgefms.com), and the SpareFoot storage-unit listing marketplace. This entry models the storEDGE REST API, whose endpoint reference is genuinely publicly documented (no NDA to read the docs), while call access itself requires being a storEDGE customer and generating one-legged OAuth 1.0 credentials (API access key/secret) tied to a facility ID.

**Areas:** Self Storage · Property Management · Facility Management · Tenants · Reservations · Payments · SiteLink · storEDGE · SpareFoot

## Storable on APIs.io

Everything profiled for Storable is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/storable/](https://apis.io/providers/storable/)** — or go straight to one of the APIs or properties below.

### APIs (11)

- [Storable Delinquency & Auctions API](https://apis.io/apis/storable/storable-delinquency-auctions-api/) — Delinquency event tracking and lien-unit auctions.
- [Storable Documents & eSign API](https://apis.io/apis/storable/storable-documents-esign-api/) — Lease/rental documents and electronic signature.
- [Storable Gate Access API](https://apis.io/apis/storable/storable-gate-access-api/) — Gate codes, access points, and gate activity logging.
- [Storable Insurance API](https://apis.io/apis/storable/storable-insurance-api/) — Tenant protection plan summary, activity, and enrollment settings.
- [Storable Leads & Reservations API](https://apis.io/apis/storable/storable-leads-reservations-api/) — Lead pipeline - reservations, inquiries, waitlist.
- [Storable Ledgers & Payments API](https://apis.io/apis/storable/storable-ledgers-payments-api/) — Tenant ledgers, payments, payment methods, invoices.
- [Storable Move Ins & Outs API](https://apis.io/apis/storable/storable-move-ins-outs-api/) — Rental move-in and move-out lifecycle.
- [Storable Reporting API](https://apis.io/apis/storable/storable-reporting-api/) — Asynchronous report requests at the facility and company level.
- [Storable Tasks API](https://apis.io/apis/storable/storable-tasks-api/) — Facility and unit-level operational task management.
- [Storable Tenants API](https://apis.io/apis/storable/storable-tenants-api/) — Tenant accounts, preferences, notes, and eligibility.
- [Storable Units & Rates API](https://apis.io/apis/storable/storable-units-rates-api/) — Unit inventory, unit groups/types, and tiered rate management.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Storable Agentic Access](https://apis.io/agentic-access/storable/storable-agentic-access/)

#### Collections (11)

Postman and Open Collection request collections.

- [Storable Edge (storEDGE) Delinquency & Auctions API](https://apis.io/collections/storable/open-storable-delinquency-auctions-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Documents & eSign API](https://apis.io/collections/storable/open-storable-documents-esign-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Gate Access API](https://apis.io/collections/storable/open-storable-gate-access-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Insurance API](https://apis.io/collections/storable/open-storable-insurance-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Leads & Reservations API](https://apis.io/collections/storable/open-storable-leads-reservations-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Ledgers & Payments API](https://apis.io/collections/storable/open-storable-ledgers-payments-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Move Ins & Outs API](https://apis.io/collections/storable/open-storable-move-ins-outs-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Reporting API](https://apis.io/collections/storable/open-storable-reporting-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Tasks API](https://apis.io/collections/storable/open-storable-tasks-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Tenants API](https://apis.io/collections/storable/open-storable-tenants-api/)
- [Storable Edge (storEDGE) Delinquency & Auctions Units & Rates API](https://apis.io/collections/storable/open-storable-units-rates-api/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Storable Authentication](https://apis.io/security/storable/storable-authentication/)
- [Storable Domain Security](https://apis.io/security/storable/storable-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Storable Plans Pricing](https://apis.io/plans/storable/storable-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Storable Rate Limits](https://apis.io/rate-limits/storable/storable-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Storable Finops](https://apis.io/finops/storable/storable-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.storable.com/)
- [Documentation](https://api.storedgefms.com/docs/v1.html)
- [Blog](https://www.storable.com/blog/)

## API Evangelist rating

**Kin Score 24.4** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 44.1 |
| Contract governance | 0.0 |
| Operational transparency | 7.9 |
| Developer ergonomics | 31.0 |
| Access clarity | 7.9 |

**Agent readiness 17.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 10.7** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/storable/](https://apis.io/providers/storable/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Storable: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/storable/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
