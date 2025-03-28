---
title: Deliverables
weight: 15
---
## Specifications

### Verifiable Trust specification

Specification for adding a trust verification layer to the Internet. It proposes a system using [Verifiable Credentials](https://www.w3.org/TR/vc-data-model-2.0/) and Verifiable Public Registries (VPRs) to establish secure, zero-trust communication channels. The specification details requirements for verifiable services and user agents, including essential credential schemas for various entities (services, organizations, persons, user agents). It outlines procedures for credential issuance, presentation requests, and trust resolution, aiming to create a more trustworthy and interoperable internet.

Browsable spec: [Verifiable Trust Specification](https://verana-labs.github.io/verifiable-trust-spec/)

### Verifiable Public Registry specification

Specification for a Verifiable Public Registry (VPR), a decentralized, ledger-based system designed to improve Internet security and trust. A VPR is a public network that can be used by any Ecosystem that would like to manages trust registries, credential schemas, and permissions for issuing and verifying credentials. It uses a tokenized business model to incentivize participation, build reputation, and maintain the system. The specification details the data model, module requirements, and various methods for managing trust registries, credential schemas, permissions, validation processes, and a [DID](https://www.w3.org/TR/did-1.0/) directory.

Browsable spec: [Verifiable Public Registry Specification](https://verana-labs.github.io/verifiable-trust-vpr-spec/)

## Software

### Verana Network

#### Backend

An open source [Cosmos-sdk](https://cosmos.network/) based implementation of the [Verifiable Public Registry Specification (VPR spec)](https://github.com/verana-labs/verifiable-trust-vpr-spec). The Verana Network includes all specified modules of the VPR spec. The network will be run by volunteers around the world. If you are interested in participating, join our [discord server](https://verana.io) and let us know.

Repo: [Verana Network](https://github.com/verana-labs/verana-blockchain)

#### Frontend

An open source dashboard for Ecosystems for interacting with the Verana Network and manage trust registries, credential schemas, permissions, and DID Directory.

Repo: [Verana Frontend](https://github.com/verana-labs/verana-frontend)

### Verre (aka Verana Resolver)

Verre is an open-source TypeScript library designed for resolving trust according to the [Verifiable Trust Specification](https://verana-labs.github.io/verifiable-trust-spec/).

This library enables any project to seamlessly integrate the Verifiable Trust layer, providing essential trust verification capabilities.

#### Key Features

With Verre, you can:

- Verify Verifiable Services – Check if a DID provides a Verifiable Service and identify its provider.

- Authenticate Credential Issuers – Ensure that an Issuer of a given credential schema is authorized by the Ecosystem Controller.

- Validate Verifier Permissions – Confirm whether a Verifier is allowed to request the presentation of a Verifiable Credential from a specific Issuer within an ecosystem.

#### How It Works

The resolver begins by resolving the DID to retrieve its DID Document, then recursively validates the required entries to ensure compliance with the Verifiable Trust framework.

Repo: [Verre](https://github.com/verana-labs/verre)

## Third Party Software

The following third-party software is being build with the Verifiable Trust spec in mind.

### Hologram Messaging

A Signal-like, self-custody messaging app which features a Verifiable Credential wallet and advanced features. The first Verifiable User Agent (VUA).

[Hologram Website](https://hologram.zone)

### Generic Verifiable Services for Credential issuance and verification

2060.io github repo is a good source of Verifiable Service examples:

[https://github.com/2060-io/](https://github.com/2060-io/)