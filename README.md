# Awesome Analytics Engineering [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

> A curated list of awesome tools, frameworks, and resources for analytics engineers.

Analytics engineering bridges the gap between data engineering and data analysis — applying software engineering best practices to transform, test, document, and serve data for decision-making.

## Contents

- [Transformation Frameworks](#transformation-frameworks)
- [Metrics Layers](#metrics-layers)
- [Data Quality & Testing](#data-quality--testing)
- [Data Modeling](#data-modeling)
- [Orchestration](#orchestration)
- [ELT/ETL & Ingestion](#eltetl--ingestion)
- [Data Warehouses & Lakehouses](#data-warehouses--lakehouses)
- [BI & Visualization](#bi--visualization)
- [Data Catalogs & Governance](#data-catalogs--governance)
- [Version Control & CI/CD for Data](#version-control--cicd-for-data)
- [SQL Utilities](#sql-utilities)
- [Python Libraries](#python-libraries)
- [Career Resources](#career-resources)
- [Books](#books)
- [Newsletters & Blogs](#newsletters--blogs)
- [Communities](#communities)
- [Conferences & Events](#conferences--events)
- [Podcasts](#podcasts)

## Transformation Frameworks

- [dbt](https://github.com/dbt-labs/dbt-core) - The standard for analytics engineering — SQL-first transformation with testing, docs, and lineage built in.
- [SQLMesh](https://github.com/TobikoData/sqlmesh) - Next-gen data transformation framework with built-in CI/CD, column-level lineage, and incremental models.
- [SQLFluff](https://github.com/sqlfluff/sqlfluff) - A modular SQL linter and auto-formatter supporting dbt, Jinja, and 20+ SQL dialects.
- [sqlfmt](https://github.com/tconbeer/sqlfmt) - An opinionated SQL formatter — like Black for Python, but for SQL.
- [dbt-utils](https://github.com/dbt-labs/dbt-utils) - General purpose macros for dbt projects (surrogate keys, date spines, pivot, unpivot).
- [dbt-expectations](https://github.com/calogica/dbt-expectations) - Port of Great Expectations to dbt as native tests.
- [dbt-date](https://github.com/calogica/dbt-date) - Date dimension and utility macros for dbt.
- [dbt-codegen](https://github.com/dbt-labs/dbt-codegen) - Macros to auto-generate dbt model, source, and base model YAML and SQL.
- [dbt-project-evaluator](https://github.com/dbt-labs/dbt-project-evaluator) - Checks your dbt project against best practices and highlights areas for improvement.
- [Lea](https://github.com/carbonfact/lea) - Lightweight alternative to dbt for running SQL transformations.

## Metrics Layers

- [MetricFlow](https://github.com/dbt-labs/metricflow) - The dbt Semantic Layer engine — define metrics once, query from any BI tool.
- [Cube](https://github.com/cube-js/cube) - Headless BI and semantic layer for building data applications with pre-aggregations and caching.
- [Lightdash](https://github.com/lightdash/lightdash) - Open-source BI that connects directly to your dbt project, using your metrics and descriptions.
- [Minerva](https://medium.com/airbnb-engineering/airbnb-metric-computation-with-minerva-part-2-9afe6695b486) - Airbnb's metrics platform (architecture reference and blog series).

## Data Quality & Testing

- [Great Expectations](https://github.com/great-expectations/great_expectations) - Python library for data validation, profiling, and documentation with 150+ built-in expectations.
- [Soda](https://github.com/sodadata/soda-core) - Data quality testing using SodaCL — a YAML-based language for writing checks against your data.
- [Elementary](https://github.com/elementary-data/elementary) - Native dbt data observability — anomaly detection, schema changes, and freshness monitoring.
- [dbt-audit-helper](https://github.com/dbt-labs/dbt-audit-helper) - Macros for comparing model outputs during refactoring to ensure nothing changed.
- [Datafold](https://www.datafold.com/) - Automated data diff and regression testing for data pipelines with CI integration.
- [re_data](https://github.com/re-data/re-data) - Open-source data reliability framework built on top of dbt.
- [Montecarlo](https://www.montecarlodata.com/) - End-to-end data observability platform with automated anomaly detection and lineage.
- [dbt-coverage](https://github.com/slidoapp/dbt-coverage) - Measure test and documentation coverage for your dbt project.

## Data Modeling

- [The Data Warehouse Toolkit (Kimball)](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/books/) - The foundational reference for dimensional modeling.
- [Data Modeling Made Simple](https://stevehoberman.com/) - Practical guide to data modeling techniques by Steve Hoberman.
- [dbdiagram.io](https://dbdiagram.io/) - Free, browser-based ERD tool using a simple DSL — great for quick schema diagrams.
- [SchemaSpy](https://github.com/schemaspy/schemaspy) - Database documentation generator that analyzes metadata and generates visual ERDs.
- [dbterd](https://github.com/datnguye/dbterd) - Generate entity relationship diagrams from your dbt project's YAML definitions.
- [Activity Schema](https://www.activityschema.com/) - A single-table data modeling approach for analytics built around activity streams.

## Orchestration

- [Dagster](https://github.com/dagster-io/dagster) - Data orchestrator with first-class dbt integration, software-defined assets, and great local dev experience.
- [Prefect](https://github.com/PrefectHQ/prefect) - Modern workflow orchestration with Python-native DAGs and a beautiful UI.
- [Apache Airflow](https://github.com/apache/airflow) - The battle-tested workflow scheduler — powers data pipelines at thousands of companies.
- [Mage](https://github.com/mage-ai/mage-ai) - Modern data pipeline tool with notebook-style UI for building, running, and monitoring ETL.
- [Kestra](https://github.com/kestra-io/kestra) - Event-driven orchestrator with a declarative YAML interface and 500+ plugins.
- [dbt Cloud](https://www.getdbt.com/product/dbt-cloud) - Managed dbt with built-in scheduling, CI/CD, IDE, and semantic layer.

## ELT/ETL & Ingestion

- [Airbyte](https://github.com/airbytehq/airbyte) - Open-source data integration with 350+ connectors and CDC support.
- [Fivetran](https://www.fivetran.com/) - Fully managed ELT with 500+ connectors — the industry standard for data ingestion.
- [Meltano](https://github.com/meltano/meltano) - Open-source DataOps platform built on Singer, combining EL with dbt transformation.
- [DltHub](https://github.com/dlt-hub/dlt) - Python library for data loading — build pipelines with decorators, handles schema evolution.
- [Singer](https://www.singer.io/) - Open-source standard for writing scripts that move data (taps and targets).
- [Sling](https://github.com/slingdata-io/sling-cli) - CLI tool for high-performance data transfer between databases, storage, and files.
- [CloudQuery](https://github.com/cloudquery/cloudquery) - High-performance ELT framework for syncing cloud infrastructure data.

## Data Warehouses & Lakehouses

- [Snowflake](https://www.snowflake.com/) - Cloud-native data warehouse with automatic scaling, time travel, and data sharing.
- [Google BigQuery](https://cloud.google.com/bigquery) - Serverless, petabyte-scale data warehouse with built-in ML capabilities.
- [Amazon Redshift](https://aws.amazon.com/redshift/) - Cloud data warehouse with columnar storage and massive parallel processing.
- [DuckDB](https://github.com/duckdb/duckdb) - In-process analytical database — runs SQL on local files, Parquet, CSV without a server.
- [ClickHouse](https://github.com/ClickHouse/ClickHouse) - Column-oriented OLAP database for real-time analytics at petabyte scale.
- [Databricks](https://www.databricks.com/) - Unified analytics platform combining data lake and data warehouse (Lakehouse).
- [Apache Iceberg](https://github.com/apache/iceberg) - Open table format for huge analytic tables with schema evolution and time travel.
- [MotherDuck](https://motherduck.com/) - Serverless cloud analytics powered by DuckDB.

## BI & Visualization

- [Metabase](https://github.com/metabase/metabase) - Open-source BI with a beautiful UI — ask questions in plain English or SQL.
- [Apache Superset](https://github.com/apache/superset) - Open-source modern data exploration and visualization platform.
- [Evidence](https://github.com/evidence-dev/evidence) - Code-driven BI — write reports in Markdown with inline SQL and chart components.
- [Streamlit](https://github.com/streamlit/streamlit) - Python framework for building data apps and dashboards in minutes.
- [Rill](https://github.com/rilldata/rill) - Operational BI for fast dashboards powered by DuckDB.
- [Looker](https://cloud.google.com/looker) - Google's enterprise BI platform with LookML modeling language.
- [Preset](https://preset.io/) - Managed Apache Superset as a service.

## Data Catalogs & Governance

- [DataHub](https://github.com/datahub-project/datahub) - Extensible metadata platform for data discovery, observability, and governance.
- [OpenMetadata](https://github.com/open-metadata/OpenMetadata) - Open-source metadata platform with data quality, profiling, and lineage.
- [Amundsen](https://github.com/amundsen-io/amundsen) - Data discovery and metadata engine by Lyft for finding trusted datasets.
- [Atlan](https://atlan.com/) - Active metadata platform — workspace for data teams to discover, govern, and collaborate.
- [Select Star](https://www.selectstar.com/) - Automated data catalog with column-level lineage and popularity tracking.
- [Castor](https://www.castordoc.com/) - AI-powered data catalog with natural language search for self-service analytics.

## Version Control & CI/CD for Data

- [SQLFluff in CI](https://docs.sqlfluff.com/en/stable/production.html) - Lint SQL in GitHub Actions/CI pipelines to enforce style and catch errors.
- [dbt Slim CI](https://docs.getdbt.com/docs/deploy/continuous-integration) - Only build and test modified models in CI to speed up pull request validation.
- [pre-commit-dbt](https://github.com/dbt-checkpoint/dbt-checkpoint) - Pre-commit hooks for dbt projects — validate schemas, check naming conventions.
- [Datafold CI](https://www.datafold.com/data-diff) - Automated data diff in CI/CD to catch regressions before they hit production.
- [SQLMesh Plan/Apply](https://sqlmesh.readthedocs.io/en/stable/concepts/plans/) - Built-in CI workflow that shows exact impact of changes before applying.

## SQL Utilities

- [SQLGlot](https://github.com/tobymao/sqlglot) - Python SQL parser, transpiler, and optimizer — convert between 20+ SQL dialects.
- [sqlparse](https://github.com/andialbrecht/sqlparse) - Non-validating SQL parser for Python — useful for formatting and tokenizing.
- [pgFormatter](https://github.com/darold/pgFormatter) - PostgreSQL SQL beautifier with Perl and online versions.
- [sql-language-server](https://github.com/joe-re/sql-language-server) - Language server protocol implementation for SQL with autocomplete and linting.
- [SQLancer](https://github.com/sqlancer/sqlancer) - Automated testing tool for finding logic bugs in SQL database engines.
- [Steampipe](https://github.com/turbot/steampipe) - Query cloud APIs, SaaS, and more using standard SQL.

## Python Libraries

- [Polars](https://github.com/pola-rs/polars) - Blazingly fast DataFrame library written in Rust with Python bindings.
- [pandas](https://github.com/pandas-dev/pandas) - The workhorse DataFrame library for data manipulation in Python.
- [DuckDB Python](https://duckdb.org/docs/api/python/overview.html) - Run SQL on DataFrames, Parquet, CSV directly from Python.
- [Ibis](https://github.com/ibis-project/ibis) - Portable Python dataframe library — write once, execute on 20+ backends.
- [Hamilton](https://github.com/DAGWorks-Inc/hamilton) - Micro-framework for creating dataframes by defining each column as a Python function.
- [Pandera](https://github.com/unionai-oss/pandera) - DataFrame validation library — like Great Expectations but for pandas/Polars/PySpark schemas.

## Career Resources

- [Analytics Engineering Guide (dbt)](https://www.getdbt.com/analytics-engineering/) - The definitive guide to the analytics engineering role by dbt Labs.
- [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) - Free 9-week course covering data engineering fundamentals.
- [dbt Certification](https://www.getdbt.com/certifications/analytics-engineering-certification) - Official dbt Analytics Engineering certification.
- [Analytics Engineer Interview Questions](https://www.interviewquery.com/p/analytics-engineer-interview-questions) - Curated list of common AE interview topics.
- [Locally Optimistic Career Guide](https://locallyoptimistic.com/post/analytics-engineer/) - Real-world advice on building an analytics engineering career.

## Books

- [Analytics Engineering with SQL and dbt](https://www.oreilly.com/library/view/analytics-engineering-with/9781098142377/) - O'Reilly book covering dbt, data modeling, and modern analytics workflows.
- [The Data Warehouse Toolkit](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/books/) - Ralph Kimball's classic on dimensional modeling.
- [Fundamentals of Data Engineering](https://www.oreilly.com/library/view/fundamentals-of-data/9781098108298/) - Comprehensive guide to the data engineering landscape by Joe Reis and Matt Housley.
- [Data Modeling Made Simple](https://stevehoberman.com/) - Practical guide to data modeling techniques.
- [SQL for Data Scientists](https://www.wiley.com/en-us/SQL+for+Data+Scientists-p-9781119669364) - Applied SQL with real analytics use cases.

## Newsletters & Blogs

- [Analytics Engineering Roundup](https://roundup.getdbt.com/) - Weekly newsletter from dbt Labs covering the analytics engineering ecosystem.
- [Locally Optimistic](https://locallyoptimistic.com/) - Blog for current and aspiring data analytics leaders.
- [Benn Stancil's Substack](https://benn.substack.com/) - Thought-provoking essays on analytics, data teams, and the industry.
- [Seattle Data Guy](https://seattledataguy.substack.com/) - Data engineering and analytics content with practical tutorials.
- [Data Engineering Weekly](https://www.dataengineeringweekly.com/) - Weekly newsletter covering data engineering news and articles.
- [Start Data Engineering](https://www.startdataengineering.com/) - Practical data engineering tutorials and system design guides.

## Communities

- [dbt Community Slack](https://www.getdbt.com/community/join-the-community) - 70K+ member Slack workspace for dbt users and analytics engineers.
- [Locally Optimistic Slack](https://locallyoptimistic.com/community/) - Private Slack for analytics practitioners and leaders.
- [r/dataengineering](https://www.reddit.com/r/dataengineering/) - Active subreddit for data engineering discussions.
- [r/analytics](https://www.reddit.com/r/analytics/) - Subreddit for analytics professionals.
- [Data Talks Club](https://datatalks.club/) - Global community for data enthusiasts with free courses and events.

## Conferences & Events

- [Coalesce](https://coalesce.getdbt.com/) - The annual analytics engineering conference by dbt Labs.
- [Data Council](https://www.datacouncil.ai/) - Technical conference for data engineers, scientists, and analysts.
- [DataEngBytes](https://dataengconf.com/) - Community-driven data engineering conference.
- [Big Data London](https://bigdataldn.com/) - Europe's leading data and AI conference.

## Podcasts

- [Analytics Engineering Podcast](https://roundup.getdbt.com/s/the-analytics-engineering-podcast) - Deep dives into analytics engineering topics from the dbt team.
- [Data Engineering Podcast](https://www.dataengineeringpodcast.com/) - Weekly interviews with data engineering practitioners and tool builders.
- [The Data Stack Show](https://datastackshow.com/) - Conversations about the modern data stack and its tools.
- [Drill to Detail](https://www.yourpodcasthost.com/drill-to-detail) - Mark Rittman's podcast on analytics, BI, and data engineering.

---

## Contributing

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
