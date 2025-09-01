# Hybrid Banking Backoffice System on AWS \+ Kubernetes  
   
## Overview  
Design for a hybrid banking backoffice system\*\* integrating on-premise core banking with AWS cloud services. The architecture ensures \*\*secure, low-latency connectivity, high availability, and regulatory compliance\*\* suitable for financial workloads.  
   
## Architecture Highlights  
- Hybrid Connectivity   
- On-premise core banking system securely connected to AWS using \*\*redundant Direct Connect links in two regions\*\*.   
- Low-latency and private data transfer between datacenter and AWS cloud.   
   
- AWS Infrastructure\*\*   
  - Multi-AZ \*\*VPCs across two regions (USA)\*\*.   
  - Public subnets\*\*: Application Load Balancers (ALBs), NAT Gateways for outbound access.   
  - Private subnets\*\*: Amazon EKS worker nodes, Kubernetes pods, backend services.   
   
- Containerized Microservices on EKS\*\*   
  - Transaction Ingestion\*\* – handles incoming transactions from multiple channels using AWS MQ .   
  - Fraud Detection\*\* – real-time anomaly and fraud scoring engine.   
  - Reconciliation\*\* – automated reconciliation of transactions with core banking.   
  - Reporting API\*\* – provides financial and compliance reports.   
  - User/Role Management\*\* – manages backoffice users and permissions.   
  - Notifications\*\* – alerting and messaging system for events and audit trails.   
  - All microservices deployed via \*\*Helm charts\*\* for consistent, templated configuration.   
   
- Infrastructure as Code (IaC)\*\*   
  - Full AWS \+ Kubernetes stack automated using \*\*Terraform\*\*.   
  - Version-controlled, reproducible, and scalable deployments.   
  - Enabled \*\*high availability and disaster recovery\*\* through multi-AZ and multi-region architecture.   
   
## Key Benefits  
- Scalable & Resilient\*\* – fault-tolerant across multiple AZs and regions.   
- Secure\*\* – private connectivity and IAM-based access control for services.   
- Automated\*\* – reduced manual intervention via IaC and Helm templates.   
- Financial-grade SLA\*\* – architecture built to meet strict banking requirements.   
   
General Topology  
   
 <img width="851" height="631" alt="image" src="https://github.com/user-attachments/assets/e3529eee-2bbe-4cd8-adf9-67f061997e5d" />

Networking Topology  
   
<img width="986" height="492" alt="image" src="https://github.com/user-attachments/assets/3e826dbb-2cd3-4458-aec7-9759bc336987" />

