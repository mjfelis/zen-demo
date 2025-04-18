---
title: The Verana Foundation
date: 2022-08-03T20:48:20+02:00

---
Welcome!

## Introduction to the Verana Foundation

Thirty years after Tim Berners-Lee introduced the World Wide Web as an open platform for sharing knowledge and connecting people, the digital world stands at a crossroads. What began as a noble tool to democratize information has evolved into a complex ecosystem shaped by commercial interests, surveillance, misinformation, and fragmented user experiences. Berners-Lee, reflecting on his creation, has voiced both pride in the web’s reach and deep concern over the direction it has taken.

{{< figure src="images/tim.png" width="200" caption="Tim Berners-Lee" class="alignright" alt="Tim Berners-Lee" >}}

We wholeheartedly echo his call for a fundamental re-foundation of the web—one built on openness, transparency, accountability, and service to the public good. A web that upholds human rights, fosters permissionless innovation, and remains accessible to all.

The Verana Foundation is a nonprofit organization dedicated to rebuilding digital trust in an era where the web's original promise of openness, privacy, and decentralization has been undermined. In response to the growing challenges of identity theft, misinformation, and opaque governance in online systems, Verana is stewarding the development of open standards and decentralized infrastructure to support secure, interoperable, and privacy-respecting communication.

Through its flagship specifications — the [Verifiable Trust Specification](https://verana-labs.github.io/verifiable-trust-spec/) and the [Verifiable Public Registry Specification](https://verana-labs.github.io/verifiable-trust-vpr-spec/) — the foundation defines a new trust layer for the internet, built on [Verifiable Credentials (VCs)](https://en.wikipedia.org/wiki/Verifiable_credentials), decentralized identifiers (DIDs), and permissioned trust registries.

As the steward of Essential Credential Schemas (ECS), the Verana Foundation not only defines the minimum set of credentials required for establishing trust in digital services and user agents, but also governs their issuance through a transparent and community-driven governance framework. This includes appointing issuer grantors and authorized issuers to ensure that ECS credentials can be relied upon as the foundational trust anchors of a decentralized digital ecosystem.

## Our Mission

The Verana Foundation is committed to advancing digital trust as a public good. Through open standards, decentralized governance, and inclusive credentialing frameworks, we enable secure, privacy-preserving digital identity and communication systems—empowering individuals, strengthening institutions, and supporting democratic digital infrastructure globally.

## Our Vision

### Verifiable Interactions

The Internet is a heterogeneous world where various types of participants coexist and interact:

- Organizations
- Services
- Individuals
- Things
- User Agents (e.g., apps, browsers)
- AI Agents
...

Interactions between participants occur by establishing connections and exchanging information.

With the growing number of communication channels and connection methods, the challenge of verifying participants' identities has become more pressing. Unfortunately, existing protocols and services do not offer a reliable way to identify and authenticate connection participants with certainty.

As a result, there is always a risk of sharing information with the wrong entity. A common example from everyday life illustrates this: when you receive a call from an unknown number claiming to be your bank, how can you verify their identity?

Several workaround methods have been developed, but they are often cumbersome, outdated, and degrade the user experience. Moreover, these methods primarily focus on authenticating consumers rather than services or their providers.

At the Verana Foundation, we believe that the widespread adoption of [Verifiable Credentials (VCs)](https://en.wikipedia.org/wiki/Verifiable_credentials) can enable any Internet participant to instantly and effortlessly verify the identity of others before exchanging information. Importantly, identity does not necessarily mean official identity. For instance, an influencer may be identified by an avatar rather than a legal name—but as a user, I can trust that this avatar represents the influencer I intend to connect with.

### Verifiable Data

From another perspective, verifying the authenticity of data is a complex task for participants. Collecting "true" data and ensuring its accuracy often requires outsourcing verification to third-party companies or services (such as identity verification providers). This approach is costly and results in the widespread sharing of user data.

At the Verana Foundation, we believe that by generalizing the use of [Verifiable Credentials (VCs)](https://en.wikipedia.org/wiki/Verifiable_credentials), verifying the authenticity of any presented data could become seamless. VCs ensure that the information they contain has not been tampered with—but that alone is not enough. To establish true trust, we must answer the following key questions:

- Is the Issuer (I) authorized to issue this credential with these claims to the Holder (H)?

- Is the Verifier (V) permitted to request H to present a credential issued by I?

- Does V trust credentials issued by I?

In practical terms, imagine a plumber presents a credential verifying their qualifications:

- I need to confirm that the credential has not been altered.

- I want to verify who issued the credential and whether I recognize them as a legitimate authority for plumbing certifications.

- When the plumber arrives, I should be able to match their face to the credential.

By addressing these questions, we move beyond simple data integrity and toward a fully trustable and verifiable ecosystem for digital credentials.

### Verifiable Reputation

At the Verana Foundation, we believe that trust should not be dictated by a central authority. Instead, ecosystems and participants should determine trustworthiness on their own. But how can this be achieved?

To enable decentralized trust, we propose that day-to-day interactions between participants and ecosystems should serve as the foundation for building a verifiable reputation. The more a participant engages with others, the stronger their reputation becomes. The higher the reputation, the more likely others are to trust that participant.

An example with Decentralized Moderation:

Social networks today are flooded with fake information, inappropriate content, and illegal material. Often, content is:

- Inappropriate for certain users (e.g., children accessing adult content).

- Legal in some jurisdictions but prohibited in others.

- Difficult to moderate at scale, as content volume is too high.

Currently, social network owners handle content moderation, but this centralized approach has major flaws:

- Limited scalability — no entity can effectively moderate all content.

- Censorship concerns—moderation decisions should not be controlled by a single company that may introduce bias, favoritism, or political influence.

- Lack of accountability — bad actors can post prohibited content without concern, as they can easily create new accounts.

- Proliferation of bots and AI-generated content, making it difficult to verify real users.

At the Verana Foundation, we believe that social networks should be decentralized into independent social channels, where channel owners are accountable through a reputation and trust deposit system.

- Each social channel owner would be identified through a Verifiable Credential (VC).

- Each social channel owner maintains a trust deposit, which grows through positive engagement and shrinks if they violate governance rules.

- Publishing harmful or illegal content results in a trust deposit penalty, discouraging bad behavior while maintaining decentralization.

- A higher trust deposit and stronger reputation attract more users, reinforcing credibility.

- If a channel owner's deposit is significantly slashed, they must refill it to continue operating, ensuring long-term accountability.

By linking content moderation to a transparent, decentralized reputation system, this model eliminates the need for centralized censorship while ensuring social channels remain responsible for their own governance.








Social networks are poisoned by fake information and sensitive or illegal content. Sometimes the content is not appropriated for the users that see it (for example, a kid should not be able to view adult content). Sometimes, a content is not legal in a juridiction, but can be legal in another one. A the moment, social network owners are performing moderation of the content generated by users and bots, but this leads to a number of issues:

- it is impossible to moderate all content because there is too much content;
- deciding if a content should be removed or censured should not be in the hands of a small group of people like the social network owner, as this can lead to favoritism or political choices and be against freedom of speech.
- sometimes, people publish prohibited content because they do not care about being banned or their social account closed, as they can create new accounts easily and start over.
- it is nearly impossible to know if content is published by real users, or by bots or AI agents.

At the Verana Foundation, we believe that if social networks were to be decentralized in independent social channels, and that those social channels owners would be mandatorily identified by an identity verifiable credential, it would solve the moderation issue of social network, as any social channel owner would auto-moderate its channel and respect the laws of its juridiction for several reasons:

- by publishing content without respecting the laws, their identity credential (real identity, avatar...) could be revoked, and they would loose access to their followers.

Building a reputation takes time. How many months needs an influencer to build a network of millions of followers linked to his Avatar?

Making Service Identification mandatory has a huge additional benefit: it enables self-moderation of participants.



## What we enable

We enable the principle: "Don't trust, verify".





- any Service, User Agent (Mobile App, Browser),... MUST be Verifiable.
- users 

Here we will show a nice diagram.
