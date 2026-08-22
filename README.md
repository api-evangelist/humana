# Humana (humana)

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

Humana is a U.S. health insurance company that provides Medicare, Medicaid, and employer-sponsored health insurance plans, along with wellness programs and healthcare services. Humana publishes a suite of FHIR-compliant APIs that give third-party applications access to member health data, coverage information, drug formularies, and provider directories under CMS interoperability rules.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/humana/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/humana/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- FHIR
- Health Insurance
- Healthcare
- Interoperability
- Medicare

## Timestamps

- **Created:** 2025-01-07
- **Modified:** 2026-05-19

## APIs

### Humana FHIR Clinical Data API

FHIR R4-compliant API surface providing clinical resources for member health data, including AllergyIntolerance, CarePlan, CareTeam, Condition, Goal, Immunization, Observation, and Procedure resources.

- **Human URL:** [https://developers.humana.com/apis/allergyintolerance-api/doc](https://developers.humana.com/apis/allergyintolerance-api/doc)
- **Base URL:** `https://fhir.humana.com/api`

#### Tags

- Clinical Data
- FHIR
- Healthcare

#### Properties

- [Documentation](https://developers.humana.com/apis/allergyintolerance-api/doc)
- [Capability Statement](https://fhir.humana.com/api/metadata)
- [Sandbox](https://sandbox-fhir.humana.com/api/)
- [Getting Started](https://developers.humana.com/)
- [OpenAPI](openapi/humana-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/humana.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/humana.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Humana FHIR Medication API

FHIR R4-compliant API surface for medication-related resources including Medication, MedicationKnowledge, MedicationRequest, drug formulary List resources, and supporting payer data.

- **Human URL:** [https://developers.humana.com/](https://developers.humana.com/)
- **Base URL:** `https://fhir.humana.com/api`

#### Tags

- FHIR
- Formulary
- Medications

#### Properties

- [Documentation](https://developers.humana.com/)
- [Capability Statement](https://fhir.humana.com/api/metadata)
- [Sandbox](https://sandbox-fhir.humana.com/api/)
- [Postman Collection](collections/humana.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/humana.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Humana FHIR Coverage and Benefits API

FHIR R4-compliant API surface for insurance coverage data, including Coverage, ExplanationOfBenefits, and InsurancePlan resources used to satisfy CMS Patient Access and Provider Directory rules.

- **Human URL:** [https://developers.humana.com/](https://developers.humana.com/)
- **Base URL:** `https://fhir.humana.com/api`

#### Tags

- Coverage
- FHIR
- Insurance

#### Properties

- [Documentation](https://developers.humana.com/)
- [Capability Statement](https://fhir.humana.com/api/metadata)
- [Sandbox](https://sandbox-fhir.humana.com/api/)
- [Postman Collection](collections/humana.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/humana.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Humana FHIR Provider Directory API

FHIR R4-compliant API surface for provider directory information, including Patient, Practitioner, PractitionerRole, Organization, Location, and DocumentReference resources.

- **Human URL:** [https://developers.humana.com/](https://developers.humana.com/)
- **Base URL:** `https://fhir.humana.com/api`

#### Tags

- FHIR
- Provider Directory

#### Properties

- [Documentation](https://developers.humana.com/)
- [Capability Statement](https://fhir.humana.com/api/metadata)
- [Sandbox](https://sandbox-fhir.humana.com/api/)
- [Postman Collection](collections/humana.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/humana.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/humana)
- [LinkedIn](https://www.linkedin.com/company/humana)
- [Portal](https://developers.humana.com/)
- [Website](https://www.humana.com/)
- [Privacy Policy](https://www.humana.com/legal/privacy-policy)
- [Terms of Service](https://www.humana.com/legal/terms-conditions)
- [Rules](https://raw.githubusercontent.com/api-evangelist/humana/refs/heads/main/humana-rules.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
