---
title: Use cases
weight: 10

---

## How an Organization (or a Person) Can Run a Verifiable Service

To run a Verifiable Service (VS), an organization must establish both technical compliance and trust compliance. Here’s how:

✅ 1. Create a Decentralized Identifier (DID)

- The organization must generate a DID that will represent the service.
- This DID will be resolvable to a DID Document, which contains service metadata and linked credentials.

⚠️ You can use any DID method.

✅ 2. Obtain Verifiable Credentials

The organization must obtain and link the following Essential Credentials to the service’s DID Document.

🔸 a. Service Credential (VT-EC-SERVICE)

Self-issued to the DID of the service by the organization DID. This credential describes:

- Name, type, description
- Minimum age requirements
- Terms and privacy policy
- Logo

🔸 b. Organization Credential (VT-EC-ORG)

Issued to the organization’s DID by a authorized issuer, verifying:

- Legal identity (registry ID, name, type)
- Address, country, logo, etc.

⚠️ If the service is operated by an individual instead of a legal organization, then A Person Credential (VT-EC-PERSON) is required instead of an Organization Credential.

✅ 3. Publish DID Document with Linked Presentations

The service’s DID Document must include:

- A signed linked verifiable presentation of the Service Credential
- A linked verifiable presentation of the Organization (or Person) Credential
- (Optionally) Additional VT credentials (e.g. trademark, regulatory approvals, etc.)

✅ 4. Ensure the Credentials Are Trust-Resolvable

To be trust-resolvable, the presented credentials must:

- Conform to ECS Json Schemas published in a trusted VPR
- Be issued by an entity authorized by the Trust Registry controlling those schemas
- Be cryptographically valid and current (not expired nor revoked)

✅ 5. Comply with VS Requirements

According to the spec:

- The service must only connect to compliant VUAs or VSs
- Your VS must support trust resolution logic (dereferencing DID Documents, resolving schema definitions and issuer/verifier permissions in trust registries created in VPRs...)
