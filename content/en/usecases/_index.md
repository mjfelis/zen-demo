---
title: Use cases
weight: 10

---

The following use cases summarize the concept of Verifiable Trust.

## 🏢 How an Organization Can Run a Verifiable Service (VS)

Running a Verifiable Service (VS) means your organization can operate a trusted, privacy-respecting digital service on the decentralized web. Here’s what you need to do:

### ✅ 1. Obtain a Decentralized Identifier (DID)

- Create a **DID** for your organization.
- This **DID** will be resolvable to a **DID Document**, which contains service metadata and linked credentials.

You can use any DID method.

### ✅ 2. Obtain an **Organization Credential (VT-EC-ORG)**

You’ll need a **Verifiable Organization Credential**, issued under an **Essential Credential Schema**:

- Find a **trusted issuer** in a **Verifiable Public Registry (VPR)**.
- Provide proof of:
  - Legal name and registration
  - Jurisdiction (country code)
  - Organization type (e.g., PRIVATE, FOUNDATION)
  - Registry URL and ID
  - Address and logo

Once verified, you receive the credential.

### ✅ 3. Issue a **Service Credential (VT-EC-SERVICE)**

- This credential describes the specific service you're offering.
- It includes:
  - Service name, description, logo
  - Minimum age required
  - Terms & conditions URL
  - Privacy policy URL
- It must be linked to your organization via your DID.

You can either:

- **Self-issue** it (if you're an authorized issuer), or
- **Request** it from an ECS issuer in the VPR.

### ✅ 4. Update Your DID Document

- Add **Linked Verifiable Presentations**:
  - Your **Service Credential**
  - Your **Organization Credential**
- Include a `VerifiablePublicRegistry` entry pointing to the VPR your credentials are registered in.

### ✅ 5. Ensure Trust Resolution Can Succeed

To be recognized as a **Verifiable Service**:

- Credentials must be **issued by authorized entities**
- They must conform to ECS JSON Schemas
- They must be **resolvable** through the VPR API
- Your credentials must be **presented in your DID Document** correctly

### ✅ 6. Start Accepting Secure Connections

Once your DID is set up:

- Other Verifiable Services or User Agents can resolve your DID
- They will check your credentials and validate them
- If trust resolution passes, they’ll allow a secure DIDComm connection

### 🚀 Summary Checklist

| Step | Action |
|------|--------|
| 🆔 | Create a DID and DID Document |
| 🏛️ | Get an Organization Credential |
| 🛠️ | Get or issue a Service Credential |
| 🔗 | Add credentials to your DID Document |
| 🔍 | Ensure trust resolution works with VPR |
| 🌐 | Go live as a Verifiable Service |

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