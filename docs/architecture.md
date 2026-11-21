# Architecture

1. Synthetic CSV files represent source-system extracts.
2. Files are loaded into Snowflake raw tables through an internal stage and `COPY INTO`.
3. Staging views standardize source fields and types.
4. Curated tables are populated with SQL transformations and incremental `MERGE`.
5. Customer history is maintained using an SCD Type 2 pattern.
6. A stream captures changes and a task demonstrates scheduled processing.
7. Validation SQL checks row counts, null business keys, duplicates, and referential consistency.

```text
CSV files -> Internal Stage -> RAW tables -> STAGING views
                                      |
                                      v
                             CURATED / DIMENSIONS
                                      |
                             Streams + Tasks
                                      |
                               Data Quality
```
