# ADR-0003 — Use GIN jsonb_path_ops index for JSONB metadata

- Status: Accepted
- Date: 2026-07-22
- Deciders: ReconX Team

## Context

Metadata is stored in JSONB.

Queries search inside JSON documents.

## Decision

Create a GIN index using jsonb_path_ops.

## Consequences

### Positive

- Faster JSON searches
- Efficient containment queries

### Negative

- Larger index
- Slightly slower inserts