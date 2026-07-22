Decision:
Use GIN jsonb_path_ops instead of BTREE.

Alternatives:

- BTREE
- No index

Constraints:

- JSONB metadata
- PostgreSQL 16

Generate an ADR.