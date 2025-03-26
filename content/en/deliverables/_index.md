---
title: Deliverables
weight: 15
---
## Specifications

### Verifiable Trust Specification

Specification for adding a trust verification layer to the Internet. It proposes a system using [Verifiable Credentials](https://www.w3.org/TR/vc-data-model-2.0/) and Verifiable Public Registries (VPRs) to establish secure, zero-trust communication channels. The specification details requirements for verifiable services and user agents, including essential credential schemas for various entities (services, organizations, persons, user agents). It outlines procedures for credential issuance, presentation requests, and trust resolution, aiming to create a more trustworthy and interoperable internet. The specification also addresses aspects like [DID](https://www.w3.org/TR/did-1.0/) Documents and whitelists of trusted VPRs.

Browsable spec: [https://verana-labs.github.io/verifiable-trust-spec/](https://verana-labs.github.io/verifiable-trust-spec/)

### Verifiable Public Registry Specification

Specification for a Verifiable Public Registry (VPR), a decentralized, ledger-based system designed to improve Internet security and trust. A VPR is a public network that can be used by any Ecosystem that would like to manages trust registries, credential schemas, and permissions for issuing and verifying credentials. It uses a tokenized business model to incentivize participation, build reputation, and maintain the system. The specification details the data model, module requirements, and various methods for managing trust registries, credential schemas, permissions, validation processes, and a [DID](https://www.w3.org/TR/did-1.0/) directory. A governance framework ensures adherence to established rules.

Browsable spec: [https://verana-labs.github.io/verifiable-trust-vpr-spec/](https://verana-labs.github.io/verifiable-trust-vpr-spec/)

## Software

### Verana Network

#### Backend

An open source [Cosmos-sdk](https://cosmos.network/) based implementation of the [Verifiable Public Registry Specification](https://github.com/verana-labs/verifiable-trust-vpr-spec).

Repo: [Verana Network](https://github.com/verana-labs/verana-blockchain)

#### Frontend

Repo: [Verana Network](https://github.com/verana-labs/verana-frontend)

### Verre (aka Verana Resolver)

An open source typescript library for resolving trust as specified in the The [Verifiable Trust Specification](https://github.com/verana-labs/verifiable-trust-spec).

This typescript library can be used by any project that would like to embed the Verifiable Trust layer.

Repo: [Verre](https://github.com/verana-labs/verre)

## Third Party Software

The following third-party software is being build with the Verifiable Trust spec in mind.

### Hologram Messaging

A Signal-like messaging App which features a Verifiable Credential wallet and advanced features.

[Get Hologram](https://hologram.zone)

### Unic ID

### Generic Credential Verifier

A generic credential verifier

[https://github.com/2060-io/generic-verifier](https://github.com/2060-io/generic-verifier)