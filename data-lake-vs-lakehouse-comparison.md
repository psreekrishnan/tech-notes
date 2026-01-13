
Data Lake vs Data Lakehouse

| **Layer**       | **Data Lake**                                                                 | **Data Lakehouse**                                                                 |
|-----------------|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Storage**     | - Raw data in native formats (CSV, JSON, Parquet)                            | - Same as Data Lake (open formats like Parquet, ORC)                              |
|                 | - Stored in distributed systems (e.g., AWS S3, Azure Data Lake, HDFS)        | - Stored in distributed systems + transactional layer (Delta Lake, Hudi, Iceberg) |
| **Processing**  | - External engines: Apache Spark, Hive, Presto                               | - Integrated engines: Spark + Delta Lake/Hudi/Iceberg                             |
|                 | - Batch-oriented, schema-on-read                                             | - Batch + streaming support, optimized queries (indexing, caching)                |
| **Management**  | - Basic metadata catalogs (AWS Glue, Hive Metastore)                        | - Advanced governance: schema enforcement, ACID transactions                      |
|                 | - Limited data quality checks                                               | - Built-in data versioning, time travel, lineage                                  |
|                 | - Security handled externally                                               | - Unified metadata layer, strong security & compliance                            |


### Key Differences:

- Storage: Both use distributed storage, but Lakehouse adds transactional tables.
- Processing: Lakehouse integrates processing with optimizations and streaming.
- Management: Lakehouse provides schema enforcement, ACID, versioning, unlike basic catalogs in Data Lake.
