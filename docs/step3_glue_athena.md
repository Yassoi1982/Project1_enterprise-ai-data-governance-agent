## Step 3 — Register dataset with AWS Glue and query with Athena

The credit card fraud dataset was uploaded to Amazon S3 and registered in AWS Glue Data Catalog.

Services used:
- Amazon S3 (data lake storage)
- AWS Glue Data Catalog (metadata)
- Amazon Athena (SQL query engine)

Process:
1. Upload dataset to S3
2. Create Glue crawler
3. Register table in Glue Data Catalog
4. Query dataset using Athena

Example query:

SELECT *
FROM raw
LIMIT 10;