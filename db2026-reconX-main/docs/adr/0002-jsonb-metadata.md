# ADR-0002 — Store instrument metadata using JSONB

- Status: Accepted
- Date: 2026-07-22
- Deciders: ReconX Team

## Context

Different financial instruments require different metadata fields.

Using relational columns would require frequent schema changes.

## Decision

Store metadata in a PostgreSQL JSONB column.

## Consequences

### Positive

- Flexible schema
- Easy evolution
- Supports indexing

### Negative

- Harder validation
- Less strict typing