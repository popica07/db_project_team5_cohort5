You are an enterprise software architect.

Decision:
Partition trades by trade_date.

Alternatives:

- Single table
- Partition by trade_id

Constraints:

- PostgreSQL 16
- 50k trades/day
- 5 year retention

Generate an ADR using Michael Nygard format.