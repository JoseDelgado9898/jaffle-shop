# Jaffle Shop (dbt + Databricks)

A small dbt project for a Databricks Jobs demo (one dbt task).

## Local

1. Put a Databricks target in `~/.dbt/profiles.yml` named `jaffle_shop`.
2. `dbt deps && dbt seed && dbt run`

Query results in Databricks SQL, e.g. `SELECT * FROM <catalog>.<schema>.customers`.

## Databricks Job

Create a job with a single **dbt** task. Point Git source at this repo, SQL warehouse at your warehouse, commands:

```
dbt deps
dbt seed
dbt build
```
