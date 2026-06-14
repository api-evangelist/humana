# Humana GraphQL Schema

## Overview

This conceptual GraphQL schema models the Humana healthcare insurance platform, covering Medicare plans, commercial insurance, provider directories, pharmacy and formulary data, claims, prior authorizations, wellness programs, and auxiliary product lines such as dental, vision, and life insurance. It is derived from publicly documented FHIR R4 APIs published at https://developers.humana.com/ and from the general structure of CMS-mandated interoperability endpoints.

The schema is conceptual. Humana does not currently expose a public GraphQL endpoint; this document describes how the REST and FHIR resources could be expressed in GraphQL terms to support third-party application development.

## Schema Source

- Developer portal: https://developers.humana.com/
- FHIR base URL: https://fhir.humana.com/api
- Sandbox: https://sandbox-fhir.humana.com/api/
- CMS interoperability rules: Patient Access API, Provider Directory API, Drug Formulary API

## Authentication

Humana's APIs use OAuth 2.0 with SMART on FHIR authorization. Third-party apps register through the developer portal and obtain access tokens scoped to patient, user, or system contexts. The `APIKey` and `Token` types in this schema reflect those constructs.

## Domain Areas

### Member and Enrollment
Types covering the insured member identity, plan enrollment, member ID card, and demographic profile. Key types: `Member`, `MemberCard`, `MemberProfile`, `Enrollment`.

### Plans and Coverage
Medicare Advantage, Medicare PDP, Medicare Supplement, commercial employer-sponsored, and HumanaOne individual plans. Key types: `InsurancePlan`, `MedicarePlan`, `MedicareAdvantage`, `MedicarePDP`, `MedicareSupplement`, `PDP`, `CommercialPlan`, `HumanaOne`, `PlanDetails`, `Coverage`, `Deductible`, `Copay`, `Coinsurance`, `MaxOOP`.

### Employer and Group Benefits
Group plan administration and employer benefit configuration. Key types: `Employer`, `EmployerBenefits`, `GroupPlan`.

### Provider Directory
FHIR-based practitioner, organization, location, and role data. Key types: `Provider`, `ProviderDirectory`, `Hospital`, `PCP`, `Specialist`, `NetworkProvider`, `InNetworkProvider`, `PCPSelection`, `SpecialistReferral`.

### Care Management
Care plans, case management, disease management programs, and chronic care support. Key types: `CarePlan`, `CaseManager`, `DiseaseManagement`, `ChronicCare`.

### Utilization and Encounters
Hospital admissions, emergency visits, and telehealth encounters. Key types: `HospitalAdmission`, `ERVisit`, `Telehealth`.

### Claims and Payments
Adjudicated claim records, claim lines, payment details, and Explanation of Benefits (EOB). Key types: `Claim`, `ClaimDetail`, `ClaimLine`, `ClaimStatus`, `ClaimPayment`, `ExplanationOfBenefits`.

### Prior Authorization and Clinical Review
Pre-authorization requests and clinical review decisions. Key types: `PreAuth`, `ClinicalReview`.

### Pharmacy and Formulary
Drug formulary tiers, pharmacy network, prescription history, and mail-order service. Key types: `Pharmacy`, `DrugFormulary`, `CoverageStage`, `Tier`, `PharmacyNetwork`, `RxHistory`, `PrescriptionOrder`, `MailOrder`.

### Wellness
Health risk assessments and wellness program enrollment. Key types: `Wellness`, `HealthAssessment`, `GoHealthyTogether`.

### Ancillary Products
Dental, vision, and life insurance lines. Key types: `HumanaDental`, `HumanaVision`, `HumanaLifeInsurance`.

### Platform and Security
API credential management and webhook subscription management. Key types: `APIKey`, `Token`, `Webhook`.

## Types Count

This schema defines 65 named GraphQL types (object types, enums, and input types).

## Usage Notes

- All monetary values use a `Money` scalar representing USD amounts as strings to avoid floating-point precision issues.
- Date fields use ISO 8601 strings (`String`) throughout.
- FHIR resource identifiers map to the `id` field on each type.
- The `Query` root provides entry points by member ID, plan ID, provider NPI, and claim ID.
- The `Mutation` root covers PCPSelection, PreAuth submission, PrescriptionOrder, Webhook management, and Wellness enrollment.
