# Data Engineering with Rust

## Abstract

Data engineering has long been the domain of JVM-based and Python ecosystems—think Apache Spark, Hadoop, and pandas.
Rust’s performance, safety, and growing ecosystem now make it an ideal choice for building high-throughput, low-latency data pipelines.
In this talk, you’ll learn how to harness crates like **arrow-rs**, **datafusion**, and **delta-rs** to ingest, transform, store, and query large datasets entirely in Rust.
We’ll explore real-world examples, benchmark comparisons against traditional tools, and best practices for architecting robust, production-ready pipelines.

## Talk Outline

1. **Introduction & Motivation**
   - Some background on the data engineering domain
      - Queries for analytics vs. Queries for applications
      - Columnar data storage (Apache Parquet)
      - DataFrame APIs
      - Query engines vs. a full RDBMS
      - Data pipeline orchestration
   - Why use rust for this task?
      - Growing ecosystem
      - Great performance
      - Error handling
      - Access to all of the rust tooling
2. **Key Crates Overview**
   - **arrow-rs**: In-memory columnar data, zero copy
   - **object_store**: Unified API for S3, GCS, local FS
   - **datafusion**: Rust based query engine
   - **delta-rs**: Rust implementation of the delta lake transaction protocol
3. **Building a Sample Pipeline**
   - Ingesting CSV/Parquet files from S3
   - Transforming data with DataFusion’s DataFrame DSL
   - Writing out the results to a delta table for downstream usage
4. **Performance Benchmarks**
   - Throughput and latency comparison vs. Spark/Pandas
   - Memory footprint analysis
   - Anecdotal example
5. **Best Practices & Patterns**
   - Data partitioning and concurrently processing data
   - Orchestration using an event driven architecture
   - Deploying rust pipelines to your infrastructure
   - Error handling and retry strategies
6. **Final thoughts**
   - Summarizing what was learned
   - Suggest further reading
   - Other crates in this space
      - polars
      - iceberg-rust
      - plotlars
      - serde_arrow
      - arrow_odbc

## Talk objectives

1. Show off the viability of rust in this space
2. Showcase all of the different crates that exist
3. Give a short overview on how to get started
