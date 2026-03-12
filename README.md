# Enterprise AI Data Governance Agent

Agentic AI system built on AWS that helps data governance and compliance teams automatically validate datasets, detect quality issues, retrieve governance context, and generate compliance-ready reports.

## Project Overview

This project demonstrates how to build an enterprise-style AI governance solution using AWS services. The system accepts a natural-language governance request, selects the right validation tools, executes SQL and data quality checks, retrieves policy context with RAG, and produces governance and compliance reports.

Example request:

> Validate the policy dataset quality and generate a compliance report.

## Business Problem

Data governance and compliance teams often spend significant time manually checking:
- missing values
- duplicates
- invalid business rule violations
- schema inconsistencies
- governance policy alignment
- compliance reporting

This project automates those tasks with an agentic AI workflow.

## Solution

The solution uses Amazon Bedrock for reasoning and orchestration of governance tasks, AWS Lambda for tool execution, AWS Step Functions for workflow control, Athena and SQL for validation, AWS Glue Data Quality for data quality rules, Amazon S3 for storage, and CloudWatch for monitoring.

## Key Features

- Natural-language governance request handling
- Automated SQL-based dataset validation
- Data quality rule execution
- Anomaly and issue detection
- Governance document retrieval with RAG
- Automated governance and compliance report generation
- Workflow monitoring and observability

## AWS Services Used

- Amazon Bedrock
- AWS Lambda
- AWS Step Functions
- Amazon S3
- Amazon Athena
- AWS Glue Data Catalog
- AWS Glue Data Quality
- AWS Lake Formation
- Amazon CloudWatch
- AWS IAM

## High-Level Architecture

1. User submits a governance request
2. Amazon Bedrock Agent interprets the request
3. Agent selects the required tools
4. Step Functions orchestrates the workflow
5. Lambda functions run profiling, SQL checks, DQ rules, and report generation
6. Athena queries data stored in S3
7. Glue Data Quality evaluates data quality rules
8. Bedrock Knowledge Base retrieves governance policy context from S3
9. Results are stored in S3 and logs are captured in CloudWatch

## Architecture Diagram

!c:\Users\Jlkan\OneDrive\Desktop\AWS Skills\aws-architecture-layout.png

## Agent Workflow Diagram
!c:\Users\Jlkan\OneDrive\Desktop\AWS Skills\Fundamentals of Machine Learning and Artificial Intelligence.png

## Repository Structure

```text
enterprise-ai-data-governance-agent/
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── docs/
├── data/
├── schemas/
├── sql/
├── dq/
├── lambda/
├── stepfunctions/
├── bedrock/
├── knowledge_base/
├── monitoring/
├── reports/
├── prompts/
├── event_samples/
├── samples/
├── tests/
└── images/