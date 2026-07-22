
# ADR-0001 — Partition the `trades` table by `trade_date`

- Status: Accepted
- Date: 2026-07-22
- Deciders: ReconX Team

## Context

ReconX stores around 50,000 trades per day with a retention period of five years.
Most reconciliation queries filter by trade date.

A single large table would become very large and make date-range queries and archival slower.

## Decision

Partition the trades table by RANGE using the trade_date column.

Each month has its own partition.

A default partition catches unexpected dates.

## Consequences

### Positive

- Faster queries through partition pruning
- Easier archival
- Smaller indexes

### Negative

- Composite primary key
- Additional maintenance for partitions