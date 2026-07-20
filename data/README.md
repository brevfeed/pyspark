# Sample datasets

Small datasets used across lessons. Kept deliberately tiny so everything
runs instantly on a laptop; lessons that need scale generate data with
`spark.range(...)` or use the Databricks `samples` catalog (lesson 1.1).

- `sample_logs.txt` — fake application log, one event per line,
  space-separated: `date time LEVEL component key=value...`. Used by
  Module 2 (RDD lessons) for textFile/map/filter/pair-RDD examples.
- `orders.csv` — 41 e-commerce order rows with **deliberate quirks** the
  Module 3 lessons rely on: two missing `quantity` values, three missing
  `country` values (lesson 3.5, null handling), and one fully duplicated
  row, order_id 1021 (lesson 3.3, distinct/dropDuplicates). Don't "fix"
  the file.
- `customers.csv` — 21-row customer dimension keyed by `customer_id`,
  built to join against `orders.csv` with **deliberate quirks** Module 7
  relies on: `c019` is *missing* (order 1037 references it — orphan FK
  for left-join nulls and anti joins), `c021`/`c022` exist but have *no
  orders* (right/full outer, anti from the other side), and it has its
  own `country` column (home country) colliding with `orders.country`
  (shipping country) — fuel for lesson 7.3's ambiguity errors. Countries
  FR/IT appear only here. Don't "fix" any of it.
- `events.jsonl` — 12 JSON-lines clickstream events with nested structs
  (`user`, `payment`) and arrays (`items`), ragged fields (some events
  lack `items`/`payment`), and **one deliberately corrupt line (event 10
  — unterminated string)** for Module 5's malformed-record handling.
  Module 6 reuses it for nested-data lessons. Don't fix line 10.
