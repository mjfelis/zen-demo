---
title: Use cases
weight: 10

---

The following use cases summarize the concept of Verifiable Trust.

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

## 🔹 User Experience: Connecting to a Verifiable Service

This is what the flow would feel like to an everyday user:

### 👤 1. User Opens Their VUA (e.g., Hologram, Trusted Wallet App)

- The user has a secure wallet or messaging app that supports Verifiable Trust.
- This app holds their verifiable credentials (e.g., Person Credential) and performs trust resolution in the background.

### 🔗 2. User Clicks a Link or Scans a QR Code

- They receive a connection invitation (e.g., to chat with a service, log in, access content).
- The link points to the DID of a Verifiable Service.

**Behind the scenes:**

- The VUA resolves the DID Document.
- It fetches the linked verifiable presentations from the service (e.g., Service Credential, Org Credential).

### 🔍 3. Trust Resolution Is Performed Automatically

The VUA validates:

- Are the credentials conforming to known ECS schemas?
- Are they issued by authorized issuers in trusted VPRs?
- Do terms, minimum age, and privacy policy match user preferences?

- ✅ If valid: The VUA displays a “Proof of Trust” badge (with icons, names, logos, and country info).
- ❌ If invalid: The user sees a warning and the app blocks the connection.

### 🙋 4. User Reviews the Service Info (Optional)

Before connecting, the app may display:

- ✅ Name of the service
- 🌍 Country of registration
- 🏛️ Organization name & logo
- 📜 Terms of service and privacy policy
- 🔞 Age restrictions

🔒 The user can make an informed decision without relying on branding or gut instinct.

### 🔑 5. User Shares Credentials If Needed

If the service requests a Verifiable Credential (e.g., proof of age, email, or membership):

- The VUA presents prompt the user for a compatible credential.
- The user selects which one to share (or declines).

🛡️ Selective disclosure and proofs without revealing more than needed are supported.

### 💬 6. Connection Established Securely

- A DIDComm connection is established with the service.
- From here, any trusted interaction is possible:
  - Secure chat
  - Video call
  - Credential issuance
  - Digital service access
  - eKYC / login flow, etc.

### 🚀 Summary Flow

1. **Click link / scan QR**
2. **VUA resolves & verifies service**
3. **User sees trust info**
4. **User optionally presents credentials**
5. **Secure session starts**

### ✨ What Makes This Experience Different?

| Feature       | Traditional Web                 | Verifiable Trust                            |
|---------------|----------------------------------|----------------------------------------------|
| **Identity**   | Centralized usernames / logins   | Decentralized identifiers (DIDs)             |
| **Trust**      | Based on logos or reputation     | Based on cryptographic proof (VCs + VPRs)    |
| **Onboarding** | Forms & passwords                | Credential-based, 1-click access             |
| **Privacy**    | Shared personal data             | Minimal disclosure, user-controlled sharing  |
| **Security**   | Phishing-prone                   | Peer authentication with DIDs and credentials |
| **UX**         | Variable, non-transparent        | Guided, verifiable, secure                   |