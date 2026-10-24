# POW-S

Proof-of-work services research for the Bitcoin Silver ecosystem.

**Status: research scaffold only.** No simulator, market, rental service, or
production component exists in this repository yet. POW-S is where proof-of-work
service designs are specified, modeled, and tested before any of them become a
product repository.

## Purpose

Explore how BTCS proof-of-work capacity can be measured, priced, rented, and
settled without changing L1 consensus. The immediate output is reproducible
research: models, simulations, benchmarks, and decision records. A production
service is a separate decision.

## Research questions

- How should hashrate rental be priced and settled when shares arrive at
  variable difficulty?
- Which payout model is fair and auditable for rented capacity?
- How do luck, variance, and pool fees affect short-window miner returns?
- What data must a pool expose to make rental accounting verifiable?
- Which parts can be simulated locally, and which require a live testnet?
- What are the legal, custody, and market-manipulation risks of a rental
  marketplace?

## Scope

Planned work:

1. **Definitions** — a shared vocabulary for hashrate, difficulty, shares,
   rounds, luck, and settlement windows.
2. **Simulation** — deterministic models of share arrival, round variance, and
   payout outcomes, with seeded fixtures.
3. **Benchmarks** — reproducible measurements of validation and accounting
   throughput.
4. **Design records** — rental, pricing, and payout proposals with explicit
   assumptions and failure modes.
5. **Reference implementation** — only after a design is reviewed; kept small
   and separate from production custody.

## Out of scope

- Consensus changes or a new proof-of-work algorithm.
- Custody, lending, derivatives, or any financial product.
- A live marketplace, order book, or real-value rental service.
- Changes to `BTCS-Mining-Pool` without that repository's review.

## Planned components

| Component | Responsibility |
| --- | --- |
| `docs/` | Research notes and decision records |
| `sim/` | Deterministic share, round, and payout simulations |
| `bench/` | Throughput and boundary benchmarks |
| `fixtures/` | Seeded, non-sensitive test data |

The directory names are proposed. They are not created yet.

## Integration points

- [BTCS-Mining-Pool](https://github.com/Silver-Labs-Technology-Development/BTCS-Mining-Pool)
  — the operator service that would consume a validated design.
- [btcs-core](https://github.com/Silver-Labs-Technology-Development/Silver-Labs-Bitcoin-Silver-Development)
  — the authority for difficulty, templates, and blocks.
- [silver-labs-platform](https://github.com/Silver-Labs-Technology-Development/silver-labs-platform)
  — shared schemas if research output becomes an API.

## Local development

There is no runnable code yet. Future simulations should run offline with a
fixed seed and no network access. Any benchmark that needs a node must use a
disposable regtest instance.

## Safety and release status

This is research, not a product. Nothing here is production-ready or audited.
Do not present a simulation result as evidence of live profitability, fair
market value, or network security. Never commit wallet data, keys, `.env`
files, or miner credentials.

See [`SECURITY.md`](SECURITY.md).

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

## License

No open-source license is granted. See [`LICENSE`](LICENSE). The repository is
public for review and development, not for reuse or redistribution.

## Related repositories

- [BTCS Mining Pool](https://github.com/Silver-Labs-Technology-Development/BTCS-Mining-Pool)
- [BTCS Core](https://github.com/Silver-Labs-Technology-Development/Silver-Labs-Bitcoin-Silver-Development)
- [Silver Labs workspace](https://github.com/orgs/Silver-Labs-Technology-Development/repositories)
