
# Module 2: AWS Foundations for Modernization

## IAM Roles & Security for M2
- **IAM Roles**: Provide secure access for AWS Mainframe Modernization environments to interact with AWS resources.  
- **Best Practices**:  
  - Use least-privilege access.  
  - Separate roles for **development**, **testing**, and **production**.  
  - Enable **MFA (Multi-Factor Authentication)** for admins.  
- **Security Integration**:  
  - Map **mainframe RACF/ACF2 rules** → **IAM policies**.  
  - Use **AWS KMS** for encryption at rest.  
  - Use **TLS/SSL** for encryption in transit.  

## Networking for Mainframe Workloads
- **VPC (Virtual Private Cloud)**: Isolated environment to host mainframe workloads.  
- **Subnets**:  
  - Public subnets → For load balancers, API Gateway.  
  - Private subnets → For Rocket runtime, databases, and applications.  
- **Security Groups**: Firewall rules for controlling inbound/outbound traffic.  
- **Key Considerations**:  
  - Use **VPC Peering / Transit Gateway** for hybrid mainframe connections.  
  - Configure **NAT Gateway** for outbound internet access from private subnets.  
  - Integrate with **AWS Direct Connect / VPN** for on-prem mainframe connectivity.  

## Databases in AWS for Mainframe Equivalence
Mainframe databases → AWS managed equivalents:

| Mainframe DB | AWS Equivalent | Use Case |
|--------------|----------------|----------|
| **VSAM**     | DynamoDB / Aurora | Key-value or relational replacement |
| **DB2**      | RDS PostgreSQL / Aurora | OLTP and relational workloads |
| **IMS**      | Amazon DocumentDB | Hierarchical → NoSQL document model |

**Example**:  
- Move **VSAM KSDS** datasets → **DynamoDB tables**.  
- Move **DB2 tables** → **Aurora PostgreSQL** for relational transactions.  
- Move **IMS hierarchical data** → **DocumentDB (MongoDB API compatible)**.  

## Storage Equivalence
- **Mainframe GDGs (Generation Data Groups), datasets** → **Amazon S3**.  
- Benefits:  
  - **Lifecycle policies** for automatic archival (e.g., S3 → Glacier).  
  - **Versioning** provides GDG-like behavior (retain multiple dataset generations).  
  - **Replication** across regions for DR.  

**Example**:  
- Daily batch output datasets → stored in **S3 buckets** with lifecycle rules:  
  - Keep last 7 days in S3 Standard.  
  - Archive older datasets to Glacier Deep Archive.  

