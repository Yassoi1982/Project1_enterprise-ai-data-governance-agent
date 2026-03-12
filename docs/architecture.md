# Enterprise AI Data Governance Agent Architecture

## Overview

This project demonstrates an AI-powered data governance system that automatically validates datasets, detects data quality issues, and generates governance reports using AWS services.

The system uses an agentic AI architecture where a large language model interprets governance requests and orchestrates validation workflows.

---

## Architecture Flow

User Request  
→ Amazon Bedrock Agent  
→ Tool Selection  
→ AWS Step Functions Workflow  
→ AWS Lambda Functions  
→ Athena / Glue Data Quality / S3  
→ Governance Report Generation  
→ CloudWatch Monitoring

---

## Architecture Components

### 1. User Request Layer

A user submits a natural-language request such as:

> Validate the policy dataset quality and generate a compliance report.

The request is interpreted by the AI agent.

---

### 2. AI Agent Layer

Amazon Bedrock processes the request using a foundation model.

The agent:
- understands the governance task
- selects the required validation tools
- orchestrates the workflow.

---

### 3. Workflow Orchestration Layer

AWS Step Functions coordinates the workflow steps:

- dataset profiling
- SQL validation
- data quality rule execution
- governance report generation.

---

### 4. Validation Layer

AWS Lambda functions execute validation tasks such as:

- SQL validation scripts
- dataset profiling
- anomaly detection
- compliance rule checks.

---

### 5. Data Layer

Amazon S3 stores:

- raw datasets
- governance documentation
- validation results
- generated reports.

Amazon Athena runs SQL queries on data stored in S3.

AWS Glue Data Catalog manages dataset metadata.

AWS Glue Data Quality executes data quality rules.

---

### 6. Knowledge Retrieval Layer

Governance policies and documentation stored in Amazon S3 are used to build a Retrieval-Augmented Generation (RAG) system.

Amazon Bedrock retrieves relevant governance documents to explain validation results.

---

### 7. Monitoring Layer

Amazon CloudWatch tracks:

- system logs
- workflow metrics
- alerts for failures or anomalies.

---

## Key Benefits

- Automated data governance checks
- Reduced manual validation work
- Improved compliance monitoring
- AI-powered governance insights