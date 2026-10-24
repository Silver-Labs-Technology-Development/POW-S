# POW-S research architecture

> **Status: candidate design note.** The scope and decisions in
> [`README.md`](../README.md) remain authoritative. This document does not
> authorize implementation.


This document describes how proof-of-work research is organized. It is a
research plan, not a description of running software.

## Research method

1. Define the question and the unit of account.
2. Write the model and its assumptions down before simulating.
3. Use deterministic, seeded simulations; record the seed and inputs.
4. Compare against a hand-calculated boundary case.
5. Publish the result with its limits, not just a headline number.
6. Promote a design to implementation only after review.

## Workstreams

### Measurement

Define hashrate, difficulty, share target, and variance in a way that pool
operators and miners can independently reproduce. Every metric needs units and
a stated observation window.

### Simulation

Model share arrival and round outcomes. Simulations must be offline, seeded,
and fast enough to run in CI. A simulation is not evidence of live returns.

### Pricing and settlement

Compare payout models (PPLNS, proportional, fee-based) under variance and
withholding scenarios. Document who bears variance and how a dispute is
reconciled.

### Rental design

Describe how capacity would be offered, measured, and settled. Identify which
records must be signed, which are operator assertions, and where a rental
market could be gamed.

### Benchmarks

Measure validation and accounting throughput with fixed fixtures. Record
hardware, runtime version, and dataset size with every result.

## Proposed layout

```text
docs/        research notes and decision records
sim/         deterministic simulations
bench/       throughput benchmarks
fixtures/    seeded, non-sensitive inputs
```

## Open questions

- Is rental settled in BTCS, in fiat, or in a separate accounting unit?
- Who is the counterparty, and what happens when a miner withholds shares?
- How is luck reported without implying a guaranteed return?
- Which outputs belong in `BTCS-Mining-Pool`, and which stay research-only?
- What legal review is required before any real-value rental service?

## Non-goals

POW-S does not change consensus, operate a pool, custody funds, or offer a
financial product. It produces evidence and designs for the repositories that
do.
