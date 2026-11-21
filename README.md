# Project 02 — Enterprise Retail Data Engineering Pipeline with Snowflake

An intermediate learning project using synthetic retail data to practise Snowflake SQL, CSV ingestion, transformations, incremental MERGE patterns, SCD Type 2, Streams, Tasks, and data-quality validation.

## Structure
- `sql/` — setup, tables, file formats, ingestion, transformations, incremental loading, SCD2, streams/tasks, quality checks
- `data/` — synthetic customers, products, orders, order items
- `docs/architecture.md` — logical architecture
- `tests/validation_queries.sql` — validation queries

## Run order
Execute SQL scripts in numerical order in a Snowflake development account. Update the warehouse/database names if needed. Upload CSVs to the named internal stage before running `COPY INTO` (the ingestion script includes the expected file paths).

## Cost and safety
Use a small warehouse and suspend it when finished. The scripts are educational starter code: validate object names, privileges, task scheduling, and SCD2 edge cases in your own account before describing the project as complete or production-ready. All data is synthetic.
