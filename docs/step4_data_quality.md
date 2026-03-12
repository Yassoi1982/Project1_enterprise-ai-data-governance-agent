## Step 4 — Data Quality Monitoring

AWS Glue Data Quality rulesets were created to monitor dataset quality.

Rulesets implemented:
- raw_dq_ruleset_v1 → completeness validation
- raw_dq_ruleset_v2 → schema integrity checks
- raw_dq_ruleset_v3 → statistical monitoring
- raw_dq_ruleset_v4 → data volume monitoring
- raw_dq_ruleset_v5 → schema drift detection

Results:
Data quality scores were generated after evaluating the rulesets on the dataset.