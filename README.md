# Storable (storable)

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

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/storable/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/storable/refs/heads/main/apis.yml)

## Brand family and access model

Storable owns two competing property-management products it sells in parallel, each with its own API:

- **storEDGE** ([api.storedgefms.com](https://api.storedgefms.com/docs/v1.html)) - a modern REST API. The full endpoint reference (~150 routes across tenants, units, ledgers, leads, move-ins/outs, gate access, insurance, tasks, documents/eSign, delinquency/auctions, and reporting) is publicly readable with no login or NDA. Calling the API requires a storEDGE facility to generate its own API access key and secret, used for one-legged OAuth 1.0 request signing - there is no three-legged OAuth handshake and no public sandbox documented.
- **SiteLink** ([sitelink.com](https://www.sitelink.com/solutions/integrations-partners)) - an older SOAP-style API. Its reference document is a password-protected PDF at `apidoc.sitelink.com`, released only after signing an NDA, plus a separate API license application at `apilicenseapplication.sitelink.com`. SiteLink documents four access levels: API Aggregator (facility/unit data), API Regular (full transaction access), API Full Reporting, and API Insurance Reporting. No endpoint list is publicly readable, so this entry does not fabricate one.
- **SpareFoot** is Storable's storage-unit listing marketplace; third-party integration partners (call centers, gate hardware, insurance, listing sites, accounting) connect to whichever of the two management-system APIs a given facility runs, with SpareFoot and StorageTreasures as common downstream consumers.

This entry focuses the `apis:` list on **storEDGE**, since it is the surface with real, publicly confirmed endpoints, and documents SiteLink honestly as a gated legacy sibling in `review.yml` rather than inventing endpoint detail for it.

## Tags

- Self Storage
- Property Management
- Facility Management
- Tenants
- Reservations
- Payments
- SiteLink
- storEDGE
- SpareFoot

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### Storable Tenants API

Create, look up, search, and update tenant records scoped to a facility - sign-in/sign-up, username/password recovery, preferences, notes, delinquency status, eligibility, and each tenant's associated leads and ledgers.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Units & Rate Management API

Manage unit inventory (list, availability, walk-thru, bulk create/update, rate history, future scheduled rates), unit groups and unit types, tiered unit-group rates, rate-applied actions, and discount plans.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Ledgers & Payments API

Read tenant ledgers and delinquency/eligibility state, make and batch payments, manage autopay and gate-access codes on a ledger, register payment methods and payment intents, authorize funds, and retrieve invoices and invoiceable items.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Leads & Reservations API

Create and manage leads across the pipeline - current, reservations, inquiries, missed move-ins, and waitlist - at the facility, company, and per-tenant level.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Move Ins & Move Outs API

Review costs and process move-ins, and review costs, schedule, cancel, and process move-outs, plus retrieve move-out reasons and applicable rates.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Gate Access API

Check gate-code availability, open gates, log gate activity events, and list a facility's access points, integrating storEDGE with third-party gate/security hardware.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Insurance API

Retrieve facility-level insurance summary and activity, configure tenant auto-enrollment settings, and record private (non-Storable) insurance coverage on a ledger.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Tasks API

Create, complete, and bulk-manage operational tasks at both the facility level and the individual unit level.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Documents & eSign API

Retrieve lease and rental documents, send esignable documents to a tenant, and complete SiteLink eSign on a rental event.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Delinquency & Auctions API

List and act on delinquency events (including bulk state transitions) and list scheduled or active lien-unit auctions at the facility and company level.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

### Storable Reporting API

Request and poll asynchronous report bundles at the facility or company level and retrieve completed results as JSON, plus check/register Business Intelligence Express enablement.

- **Human URL:** [https://api.storedgefms.com/docs/v1.html](https://api.storedgefms.com/docs/v1.html)
- **Base URL:** `https://api.storedgefms.com/v1`

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/storableinc)
- [Website](https://www.storable.com/)
- [Documentation](https://api.storedgefms.com/docs/v1.html)
- [Plans](plans/storable-plans-pricing.yml)
- [Rate Limits](rate-limits/storable-rate-limits.yml)
- [Fin Ops](finops/storable-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
