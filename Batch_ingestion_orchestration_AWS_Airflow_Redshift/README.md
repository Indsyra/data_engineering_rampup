
# Generalities
Storage Layer : Amazon S3 => CSV
Orchestration Layer : Airflow + Python (Input dataset validation / Data cleaning / Data transformation / Data ingestion)
Data Warefouse : Final reporting tables


# Airflow
Fully managed by AWS
Automatically scales resources to meet demands of workflows
DAG (Direct Acyclic Graph)
Airflow Hooks : intefaces to external platforms and databases
Airflow Operators : building blocks of a workflow. Can be used as task to execute a specific function.
Airflow Xcoms : Share data between the tasks


# Redshift: data warehouse service in the cloud
Data warehouse: Centralized repository that stores large volumes of data from multiple sources

Severless : no need to manage clusters, automatically scales capacity based on workload

Query Data on Redshift : SQL Editor
Port 5439



