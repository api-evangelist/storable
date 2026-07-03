# Storable (storable)

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
