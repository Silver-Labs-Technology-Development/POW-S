# POW-S

> **Status: Research / planned — repository and scope only.**
> No service, API, contract, or implementation exists here. The product scope
> is unresolved.

## Purpose

POW-S is a placeholder product boundary for proof-of-work services research.
The name does not yet imply a confirmed service, customer, or operating model.
This repository exists so that research has a separate home and cannot be
mistaken for a released product.

POW-S is not a renamed BTCS Mining Pool. The relationship between the two, if
any, is undecided.

## Questions that must be answered before a design is chosen

1. What concrete proof-of-work service is being offered?
2. Who is the customer, and what do they receive?
3. How is work verified, priced, and settled?
4. What are the custody, fraud, abuse, and legal boundaries?
5. Does the service use BTCS, another chain, or no chain at all?
6. What existing implementation, if any, can be reviewed and licensed?

Until these questions are answered, no API, token, marketplace, or revenue
model should be documented as planned functionality.

## Explicitly out of scope

- Any claim that POW-S is implemented, available, or accepting customers.
- Real-fund payments, custody, or mining contracts.
- Copying an upstream implementation without a license and security review.
- Merging POW-S code into BTCS Core, BTCS L2, or the mining pool by assumption.

## Possible integration points, subject to the design

- **BTCS Core** — proof-of-work verification and chain data, if relevant.
- **BTCS Mining Pool** — only if a documented boundary is agreed.
- **SilverPay** — only if a payment flow is actually designed and approved.
- **silver-labs-platform** — schemas and client contracts if an API is defined.

## First milestone

A scope decision record that states the service, customer, verification method,
payment model, and explicit non-goals. No code before that decision.

## Repository facts

- Local workspace path: `~/Silver-Labs/POW-S`
- Default branch: `main`
- Implementation: none
- Tests run: none (no code)
- License: proprietary; all rights reserved (see `LICENSE`); no reuse rights are granted
- Visibility: public research repository

This repository is labeled research so that its existence is not mistaken for a
product.

## Repository layout

```text
.
├── README.md
├── LICENSE
├── SECURITY.md
├── .gitignore
└── docs/
    └── ARCHITECTURE.md
```

## Architecture note

[`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) records a candidate component
breakdown and threat model. It is subordinate to the scope and decisions above
and does not authorize implementation.

## Security

See [`SECURITY.md`](SECURITY.md) for the reporting policy and security
boundaries. No implementation, test suite, or independent audit exists yet.

## License

No open-source license is granted. See [`LICENSE`](LICENSE). The repository is
public for review and development, not for reuse or redistribution.
