# Security policy

## Scope

This repository is a **research scaffold** for proof-of-work services. It
contains no production service, no custody, and no real-value settlement.

## Reporting

Do not open a public issue containing exploit details, credentials, or wallet
data. Report privately to the Silver Labs maintainers through the organization
account <https://github.com/Silver-Labs-Technology-Development>.

## Security boundaries for future work

- Simulations must be offline and must not require real keys or live funds.
- Research must not be presented as a security audit or a profitability claim.
- Any design that touches payouts must define limits, approvals, and
  reconciliation before implementation.
- Never commit wallet data, private keys, seed phrases, or `.env` files.

## Known limitations

- No implementation, test suite, or independent review exists.
- Research assumptions may not hold on a live network.
