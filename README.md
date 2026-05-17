# EUDI Non-Qualified EAA Issuer Toolkit

Reference toolkit for non-EU institutions to issue **non-qualified Electronic Attestations of Attributes (EAA)** compatible with the **EU Digital Identity Wallet** ecosystem.

The toolkit helps institutions **test, validate and issue** standards-based credentials using open protocols.

**First worked example:** academic diplomas  
**Extensible to:** professional certificates, training records, memberships and other EAA domains  
**License:** Apache-2.0  
**Status:** Early development  
**Standards:** W3C VC 2.0 · SD-JWT VC · OpenID4VCI · OpenID4VP

---

## The problem

Under eIDAS 2.0, the European Digital Identity Wallet ecosystem distinguishes between different types of Electronic Attestations of Attributes, including qualified and non-qualified attestations.

For many institutions established outside the EU, the realistic entry point is the issuance of **non-qualified EAAs**. However, there is currently no simple open-source reference toolkit that helps such institutions produce credentials that are technically aligned with the EUDI Wallet ecosystem.

This project fills that gap.

It provides a practical, open-source issuer toolkit for non-EU institutions that want to issue standards-based, privacy-preserving digital attestations that can be consumed by wallets, verifiers and relying parties.

---

## What this toolkit is

This repository provides a reference implementation for issuing **non-qualified Electronic Attestations of Attributes**.

It is designed to help non-EU issuers:

- issue non-qualified EAAs using open standards;
- use SD-JWT VC for selective disclosure;
- expose issuer configuration compatible with OpenID4VCI;
- validate credential structure and metadata;
- start from a working academic diploma example;
- extend the same pattern to other credential domains.

The first worked example is:

> A Tunisian university issuing an academic diploma attestation that can be presented to a German employer or other EU relying party.

---

## What this toolkit is not

This project is not:

- a QTSP;
- a QEAA issuer;
- a legal trust anchor;
- a national wallet implementation;
- a commercial credential platform;
- a replacement for institutional authority or legal recognition.

The toolkit only provides the **technical issuance pipe**.

Trust remains with the issuing institution and any applicable legal, organisational or ecosystem trust framework.

---

## Project scope

### Core toolkit

The core toolkit will include:

- **Issuer SDK**
  - TypeScript SDK
  - Python SDK

- **OpenID4VCI issuance flow**
  - issuer metadata
  - credential configuration
  - issuance endpoint examples
  - signing abstraction

- **SD-JWT VC support**
  - selective disclosure by default
  - claim-level disclosure design
  - signed sample credentials

- **Non-qualified EAA issuer profile**
  - credential profile for non-EU institutional issuers
  - mapping to EUDI Wallet ecosystem concepts
  - clear trust boundaries

- **Conformance-oriented checks**
  - credential structure validation
  - issuer metadata validation
  - sample test vectors
  - automated tests

---

## First reference example: academic diplomas

The first domain-specific example is academic diplomas.

It will include:

- diploma credential schema;
- sample issuer configuration;
- signed sample credentials;
- holder-facing credential example;
- verifier-facing presentation example;
- integration guide;
- reference flow: Tunisian university → German employer.

The academic diploma example is only the first implementation. The architecture is intended to support additional non-qualified EAA domains.

---

## Planned future examples

Future examples may include:

- professional certifications;
- vocational training certificates;
- membership attestations;
- institutional eligibility attestations;
- government-issued non-PuB attestations;
- private-sector compliance attestations.

New examples should follow the structure described in `CONTRIBUTING.md`.

---

## Repository structure

Planned structure:

```text
.
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── docs/
│   ├── eidas2-context.md
│   ├── issuer-profile.md
│   ├── trust-model.md
│   └── architecture.md
├── packages/
│   ├── issuer-sdk-ts/
│   └── issuer-sdk-py/
├── examples/
│   └── academic-diploma/
│       ├── schema/
│       ├── issuer-config/
│       ├── sample-credentials/
│       └── README.md
├── tests/
│   ├── conformance/
│   └── fixtures/
└── tools/
    └── validator/
```

---

## Standards and specifications

This project is designed around open standards and interoperability.

Target standards include:

- W3C Verifiable Credentials 2.0
- SD-JWT VC
- OpenID for Verifiable Credential Issuance
- OpenID for Verifiable Presentations
- Decentralized Identifiers
- EUDI Wallet Architecture and Reference Framework concepts

The toolkit will avoid proprietary credential formats wherever possible.

---

## Contributing

Contributions are welcome.

Relevant contribution areas include:

- OpenID4VCI implementation;
- SD-JWT VC support;
- EUDI Wallet interoperability;
- credential schema design;
- conformance testing;
- academic credential examples;
- documentation;
- additional non-qualified EAA domain examples.

Before contributing, please read `CONTRIBUTING.md`.

---

## License

This project is licensed under the Apache License 2.0.

See `LICENSE` for details.

---

## Maintainer

This project is maintained by TanitShield.

It is part of a broader effort to build open, privacy-preserving and EUDI-compatible trust infrastructure for cross-border credential verification.

---

## Disclaimer

This repository provides technical tooling and reference implementations.

It does not provide legal advice, qualified trust services, accreditation, certification or official recognition under eIDAS 2.0.

Institutions using this toolkit are responsible for determining their legal obligations, trust framework requirements and compliance responsibilities.
