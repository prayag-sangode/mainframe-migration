# Module 1: Introduction

## What is Mainframe Modernization?
Mainframe modernization is the process of moving legacy mainframe applications, data, and workloads to modern cloud-based platforms like **AWS**.  
It enables organizations to **reduce costs**, **improve agility**, and **integrate with modern services** while preserving mission-critical functionality.


## Why Migrate?
- **Cost Savings** → Lower infrastructure and licensing costs on AWS.  
- **Agility** → Faster development, DevOps pipelines, CI/CD support.  
- **Integration** → Connect legacy apps with modern APIs, microservices, and analytics platforms.  


## Migration Strategies
1. **Replatform** → Lift-and-shift apps with minimal changes (Rocket runtime on AWS).  
2. **Refactor** → Transform code (e.g., COBOL → Java) using automated tools.  
3. **Rehost** → Move workloads "as is" to AWS without significant modifications.  


## AWS Mainframe Modernization (M2) Service
AWS Mainframe Modernization provides a **fully managed environment** to migrate, modernize, and run mainframe applications in the cloud.

### Managed Runtimes
- **Blu Age** → Automated refactoring to modern languages (e.g., Java).  
- **Micro Focus / Rocket** → Replatform COBOL and PL/I applications with minimal code changes.  

### Supported Workloads
- **COBOL, PL/I** → Legacy programming languages.  
- **JCL** → Batch job control.  
- **VSAM, DB2, IMS** → Mainframe data sources.  


## Rocket Software Overview
Rocket Software provides tools to run and modernize mainframe applications on AWS.

### Rocket Enterprise Server
- COBOL and PL/I runtime environment.  
- Supports JCL execution.  
- Integrates with AWS for scaling and availability.  

### Rocket Enterprise Developer
- IDE for COBOL/PL/I developers.  
- Debugging, testing, and CI/CD integration.  
- Works with AWS CodePipeline, CodeBuild, and GitHub.  

### Rocket Analyzer
- Analyzes COBOL/PL/I applications.  
- Identifies dependencies, unused code, and migration complexity.  


## Integration with AWS M2
- Rocket runtime is available as a **managed environment** in AWS Mainframe Modernization.  
- Supports seamless migration from **on-prem mainframe to AWS cloud**.  
- Integrates with AWS services like **RDS (Aurora/Postgres), DynamoDB, IAM, KMS, CloudWatch** for modernization.  


