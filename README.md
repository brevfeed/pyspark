# PySpark notebooks

72 runnable Colab notebooks for **real Spark 4.0** — the JVM/cluster half of
PySpark that a browser can't run: RDDs, shuffle, Catalyst, UDFs, caching,
performance tuning and Structured Streaming.

Every notebook is self-contained. Click an **Open in Colab** badge below and run the
first cell — it installs a JDK 17 + PySpark and pulls the sample data from this
repo. Nothing to set up locally, no cluster, no account.

> Learning the DataFrame API itself? Start with the free in-browser course at
> **[brevfeed.com/learn/pyspark](https://brevfeed.com/learn/pyspark)** — 44 lessons
> with graded exercises that run in the page, no install at all. These notebooks are
> the companion track for everything that needs a real engine.

## Sample data

`data/` holds four small, deliberately quirky files shared across the notebooks —
missing values, a duplicate row, an orphaned foreign key, one corrupt JSON line.
The quirks are the point; several lessons depend on them. See
[`data/README.md`](data/README.md).

## Notebooks

### 2. RDD fundamentals

The layer under the DataFrame API — and when it still matters.

| # | Notebook | |
|---|---|---|
| 0 | [Creating RDDs: `parallelize` and `textFile`](notebooks/02-rdd-fundamentals/00-creating-rdds.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/02-rdd-fundamentals/00-creating-rdds.ipynb) |
| 1 | [Transformations vs actions, lazy evaluation, DAG](notebooks/02-rdd-fundamentals/01-transformations-actions-lazy.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/02-rdd-fundamentals/01-transformations-actions-lazy.ipynb) |
| 2 | [map, flatMap, filter, reduce, and the *ByKey family](notebooks/02-rdd-fundamentals/02-core-transformations.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/02-rdd-fundamentals/02-core-transformations.ipynb) |
| 3 | [Partitions, repartition() vs coalesce()](notebooks/02-rdd-fundamentals/03-partitions-repartition-coalesce.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/02-rdd-fundamentals/03-partitions-repartition-coalesce.ipynb) |
| 4 | [cache(), persist(), storage levels](notebooks/02-rdd-fundamentals/04-cache-persist-storage-levels.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/02-rdd-fundamentals/04-cache-persist-storage-levels.ipynb) |
| 5 | [Broadcast variables and accumulators](notebooks/02-rdd-fundamentals/05-broadcast-accumulators.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/02-rdd-fundamentals/05-broadcast-accumulators.ipynb) |

### 3. DataFrame fundamentals

The core verbs, explicit schemas, and the chained-pipeline style.

| # | Notebook | |
|---|---|---|
| 0 | [Creating DataFrames and schemas](notebooks/03-dataframe-fundamentals/00-creating-dataframes-and-schemas.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/03-dataframe-fundamentals/00-creating-dataframes-and-schemas.ipynb) |
| 1 | [select, filter/where, withColumn, drop, alias, cast](notebooks/03-dataframe-fundamentals/01-select-filter-withcolumn.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/03-dataframe-fundamentals/01-select-filter-withcolumn.ipynb) |
| 2 | [Column expressions: col(), lit(), expr(), when/otherwise](notebooks/03-dataframe-fundamentals/02-column-expressions.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/03-dataframe-fundamentals/02-column-expressions.ipynb) |
| 3 | [orderBy/sort, distinct, limit, sample](notebooks/03-dataframe-fundamentals/03-sort-distinct-limit-sample.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/03-dataframe-fundamentals/03-sort-distinct-limit-sample.ipynb) |
| 4 | [groupBy + agg](notebooks/03-dataframe-fundamentals/04-groupby-agg.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/03-dataframe-fundamentals/04-groupby-agg.ipynb) |
| 5 | [Null handling](notebooks/03-dataframe-fundamentals/05-null-handling.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/03-dataframe-fundamentals/05-null-handling.ipynb) |
| 6 | [show / collect / take / toPandas, safely](notebooks/03-dataframe-fundamentals/06-getting-data-out-safely.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/03-dataframe-fundamentals/06-getting-data-out-safely.ipynb) |

### 4. Spark SQL

Temp views, parameterized `spark.sql()`, and mixing SQL with the API.

| # | Notebook | |
|---|---|---|
| 0 | [Temp views, global temp views, spark.sql()](notebooks/04-spark-sql/00-temp-views-and-spark-sql.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/04-spark-sql/00-temp-views-and-spark-sql.ipynb) |
| 1 | [SQL vs DataFrame API in a real script](notebooks/04-spark-sql/01-sql-vs-dataframe-api.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/04-spark-sql/01-sql-vs-dataframe-api.ipynb) |
| 2 | [The Catalog API](notebooks/04-spark-sql/02-catalog-api.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/04-spark-sql/02-catalog-api.ipynb) |
| 3 | [Hive metastore basics](notebooks/04-spark-sql/03-hive-metastore-basics.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/04-spark-sql/03-hive-metastore-basics.ipynb) |

### 5. Data sources & I/O

CSV/JSON/Parquet, malformed records, JDBC, and the Kafka source shape.

| # | Notebook | |
|---|---|---|
| 0 | [File formats and the options that matter](notebooks/05-data-sources-io/00-file-formats-and-options.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/05-data-sources-io/00-file-formats-and-options.ipynb) |
| 1 | [Schema evolution and merging](notebooks/05-data-sources-io/01-schema-evolution-and-merging.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/05-data-sources-io/01-schema-evolution-and-merging.ipynb) |
| 2 | [partitionBy, predicate pushdown, column pruning](notebooks/05-data-sources-io/02-partitionby-pushdown-pruning.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/05-data-sources-io/02-partitionby-pushdown-pruning.ipynb) |
| 3 | [JDBC read/write](notebooks/05-data-sources-io/03-jdbc-read-write.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/05-data-sources-io/03-jdbc-read-write.ipynb) |
| 4 | [The small-files problem](notebooks/05-data-sources-io/04-small-files-problem.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/05-data-sources-io/04-small-files-problem.ipynb) |
| 5 | [Reading from Kafka](notebooks/05-data-sources-io/05-reading-from-kafka.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/05-data-sources-io/05-reading-from-kafka.ipynb) |

### 6. Complex & nested data

Arrays, structs, maps, and reusable flattening utilities.

| # | Notebook | |
|---|---|---|
| 0 | [Arrays: explode and higher-order functions](notebooks/06-complex-nested-data/00-arrays.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/06-complex-nested-data/00-arrays.ipynb) |
| 1 | [Structs](notebooks/06-complex-nested-data/01-structs.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/06-complex-nested-data/01-structs.ipynb) |
| 2 | [Maps](notebooks/06-complex-nested-data/02-maps.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/06-complex-nested-data/02-maps.ipynb) |
| 3 | [JSON in a column: from_json, to_json, schema_of_json](notebooks/06-complex-nested-data/03-json-in-a-column.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/06-complex-nested-data/03-json-in-a-column.ipynb) |
| 4 | [Programmatic flattening](notebooks/06-complex-nested-data/04-programmatic-flattening.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/06-complex-nested-data/04-programmatic-flattening.ipynb) |

### 7. Joins deep dive

Join types, strategies, skew, and the ambiguity errors everyone hits.

| # | Notebook | |
|---|---|---|
| 0 | [Join types: inner, outer, semi, anti, cross](notebooks/07-joins-deep-dive/00-join-types.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/07-joins-deep-dive/00-join-types.ipynb) |
| 1 | [Join strategies: BHJ, SMJ, SHJ, BNLJ](notebooks/07-joins-deep-dive/01-join-strategies.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/07-joins-deep-dive/01-join-strategies.ipynb) |
| 2 | [broadcast() and autoBroadcastJoinThreshold](notebooks/07-joins-deep-dive/02-broadcast-hint-and-threshold.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/07-joins-deep-dive/02-broadcast-hint-and-threshold.ipynb) |
| 3 | [Ambiguous columns after joins](notebooks/07-joins-deep-dive/03-ambiguous-columns.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/07-joins-deep-dive/03-ambiguous-columns.ipynb) |
| 4 | [Join skew: see it, salt it, let AQE fix it](notebooks/07-joins-deep-dive/04-join-skew-salting-aqe.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/07-joins-deep-dive/04-join-skew-salting-aqe.ipynb) |

### 8. Window functions

Ranking, lag/lead, frames, running totals, and sessionization.

| # | Notebook | |
|---|---|---|
| 0 | [The window spec: partitionBy, orderBy, frames](notebooks/08-window-functions/00-window-spec.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/08-window-functions/00-window-spec.ipynb) |
| 1 | [Ranking: row_number, rank, dense_rank, ntile](notebooks/08-window-functions/01-ranking.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/08-window-functions/01-ranking.ipynb) |
| 2 | [lag, lead, first, last](notebooks/08-window-functions/02-lag-lead-first-last.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/08-window-functions/02-lag-lead-first-last.ipynb) |
| 3 | [Running totals, moving averages, sessionization](notebooks/08-window-functions/03-running-totals-sessionization.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/08-window-functions/03-running-totals-sessionization.ipynb) |
| 4 | [Deduplication: pick the survivor deliberately](notebooks/08-window-functions/04-dedup-patterns.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/08-window-functions/04-dedup-patterns.ipynb) |

### 9. User-defined functions

Python vs pandas UDFs, the serialization cost, and how to avoid both.

| # | Notebook | |
|---|---|---|
| 0 | [Python UDFs: mechanics and cost](notebooks/09-user-defined-functions/00-python-udfs.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/09-user-defined-functions/00-python-udfs.ipynb) |
| 1 | [Pandas UDFs: vectorized escape hatches](notebooks/09-user-defined-functions/01-pandas-udfs.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/09-user-defined-functions/01-pandas-udfs.ipynb) |
| 2 | [Pandas Function API: applyInPandas, mapInPandas, cogroup](notebooks/09-user-defined-functions/02-pandas-function-api.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/09-user-defined-functions/02-pandas-function-api.ipynb) |
| 3 | [Arrow: the two switches, timed](notebooks/09-user-defined-functions/03-arrow-optimization.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/09-user-defined-functions/03-arrow-optimization.ipynb) |
| 4 | [The best UDF is no UDF](notebooks/09-user-defined-functions/04-avoiding-udfs.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/09-user-defined-functions/04-avoiding-udfs.ipynb) |

### 10. Partitioning & shuffle

Partitions vs cores vs tasks, the Exchange, and shuffle config.

| # | Notebook | |
|---|---|---|
| 0 | [Partitions vs cores vs tasks: the mental model](notebooks/10-partitioning-shuffle/00-partitions-cores-tasks.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/10-partitioning-shuffle/00-partitions-cores-tasks.ipynb) |
| 1 | [repartition, coalesce, and repartition-by-column](notebooks/10-partitioning-shuffle/01-repartition-coalesce-by-column.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/10-partitioning-shuffle/01-repartition-coalesce-by-column.ipynb) |
| 2 | [Shuffle mechanics: catch the shuffle in the act](notebooks/10-partitioning-shuffle/02-shuffle-mechanics.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/10-partitioning-shuffle/02-shuffle-mechanics.ipynb) |
| 3 | [spark.sql.shuffle.partitions: catch 200 red-handed](notebooks/10-partitioning-shuffle/03-shuffle-partitions-config.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/10-partitioning-shuffle/03-shuffle-partitions-config.ipynb) |
| 4 | [Data skew everywhere](notebooks/10-partitioning-shuffle/04-data-skew.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/10-partitioning-shuffle/04-data-skew.ipynb) |

### 11. The Catalyst optimizer

The four plan trees, pushdown, pruning, and reading `explain()`.

| # | Notebook | |
|---|---|---|
| 0 | [The plan pipeline: four trees on one object](notebooks/11-catalyst-optimizer/00-plan-pipeline.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/11-catalyst-optimizer/00-plan-pipeline.ipynb) |
| 1 | [explain() modes: five doors into the plan](notebooks/11-catalyst-optimizer/01-explain-modes.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/11-catalyst-optimizer/01-explain-modes.ipynb) |
| 2 | [Pushdown, pruning, folding: read it off the scan node](notebooks/11-catalyst-optimizer/02-pushdown-pruning-folding.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/11-catalyst-optimizer/02-pushdown-pruning-folding.ipynb) |
| 3 | [Whole-stage codegen: what the `*` means](notebooks/11-catalyst-optimizer/03-whole-stage-codegen.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/11-catalyst-optimizer/03-whole-stage-codegen.ipynb) |
| 4 | [Adaptive Query Execution: the optimizer that runs twice](notebooks/11-catalyst-optimizer/04-adaptive-query-execution.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/11-catalyst-optimizer/04-adaptive-query-execution.ipynb) |

### 12. Caching & memory

Storage levels, the unified memory model, spill, and checkpointing.

| # | Notebook | |
|---|---|---|
| 0 | [Storage levels: catch a DataFrame cache in the act](notebooks/12-caching-memory/00-storage-levels.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/12-caching-memory/00-storage-levels.ipynb) |
| 1 | [Unified memory model: watch storage lose to execution](notebooks/12-caching-memory/01-unified-memory-model.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/12-caching-memory/01-unified-memory-model.ipynb) |
| 2 | [Diagnosing spill: find it, don't just report it](notebooks/12-caching-memory/02-diagnosing-spill.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/12-caching-memory/02-diagnosing-spill.ipynb) |
| 3 | [Checkpointing vs caching: sever the lineage](notebooks/12-caching-memory/03-checkpointing-vs-caching.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/12-caching-memory/03-checkpointing-vs-caching.ipynb) |
| 4 | [Executor memory, overhead, and GC: read the signal first](notebooks/12-caching-memory/04-executor-memory-gc.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/12-caching-memory/04-executor-memory-gc.ipynb) |

### 13. Performance tuning

The top-down diagnosis routine and a pre-ship checklist.

| # | Notebook | |
|---|---|---|
| 0 | [Reading the UI DAG and skew: the top-down routine](notebooks/13-performance-tuning/00-reading-ui-dag-and-skew.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/13-performance-tuning/00-reading-ui-dag-and-skew.ipynb) |
| 1 | [Symptom classifier: spill, skew, or bad partition count](notebooks/13-performance-tuning/01-diagnosing-oom-spill-skew-partitions.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/13-performance-tuning/01-diagnosing-oom-spill-skew-partitions.ipynb) |
| 2 | [Bucketing: pay the shuffle once, not every run](notebooks/13-performance-tuning/02-bucketing-for-joins.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/13-performance-tuning/02-bucketing-for-joins.ipynb) |
| 3 | [Table statistics: give the optimizer real numbers](notebooks/13-performance-tuning/03-table-statistics-cbo.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/13-performance-tuning/03-table-statistics-cbo.ipynb) |
| 4 | [Cluster sizing: the math, since local mode can't show the cluster](notebooks/13-performance-tuning/04-cluster-sizing.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/13-performance-tuning/04-cluster-sizing.ipynb) |
| 5 | [Pre-ship checklist, applied: fix a deliberately bad script](notebooks/13-performance-tuning/05-pre-ship-checklist.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/13-performance-tuning/05-pre-ship-checklist.ipynb) |

### 14. Structured Streaming

The unbounded table, watermarks, output modes, and stateful ops.

| # | Notebook | |
|---|---|---|
| 0 | [The unbounded-table model, made concrete](notebooks/14-structured-streaming/00-unbounded-table-model.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/14-structured-streaming/00-unbounded-table-model.ipynb) |
| 1 | [Sources: file, Kafka, rate](notebooks/14-structured-streaming/01-sources-file-kafka-rate.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/14-structured-streaming/01-sources-file-kafka-rate.ipynb) |
| 2 | [Output modes and sinks, side by side](notebooks/14-structured-streaming/02-output-modes-and-sinks.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/14-structured-streaming/02-output-modes-and-sinks.ipynb) |
| 3 | [Watermarking: bounded state, and a concrete drop rule](notebooks/14-structured-streaming/03-watermarking-late-data.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/14-structured-streaming/03-watermarking-late-data.ipynb) |
| 4 | [Stateful ops: windows, then hand-rolled state](notebooks/14-structured-streaming/04-stateful-ops.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/14-structured-streaming/04-stateful-ops.ipynb) |
| 5 | [Stream-static and stream-stream joins](notebooks/14-structured-streaming/05-stream-joins.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/14-structured-streaming/05-stream-joins.ipynb) |
| 6 | [Checkpointing: what's actually in there, and restart behavior](notebooks/14-structured-streaming/06-checkpointing-semantics.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/14-structured-streaming/06-checkpointing-semantics.ipynb) |
| 7 | [Trigger types: cadence is a deliberate choice](notebooks/14-structured-streaming/07-trigger-types.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brevfeed/pyspark/blob/main/notebooks/14-structured-streaming/07-trigger-types.ipynb) |

## Running locally

```bash
pip install pyspark==4.0.0 jupyter    # needs a JDK 17+ on PATH
jupyter notebook notebooks/
```

The setup cell detects a usable JDK and an existing PySpark install and skips
both, so local runs stay fast.

## License

MIT — see [LICENSE](LICENSE).
