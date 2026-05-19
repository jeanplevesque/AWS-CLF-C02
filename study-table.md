# AWS CLF-C02 Study Table

Concise study summaries based on current official AWS product and documentation pages checked on 2026-05-19.

## Analytics

| Service | Short description |
| --- | --- |
| Amazon Athena | Serverless SQL queries on S3 and other data sources. |
| Amazon EMR | Managed big data platform for Spark, Hadoop, and analytics. |
| AWS Glue | Serverless data integration, ETL, and data catalog. |
| Amazon Kinesis | Collect, process, and analyze real-time video and data streams. |
| Amazon OpenSearch Service | Managed search, log analytics, and observability. |
| Amazon QuickSight | Serverless business intelligence dashboards and analytics. |
| Amazon Redshift | Cloud data warehouse for analytics. |

These services can work together, but they do not all serve the same role. A common pattern is to use Amazon Kinesis for real-time streaming data, AWS Glue to discover, prepare, move, and catalog data, Amazon Athena to run serverless SQL directly on data in Amazon S3, Amazon Redshift for warehouse-style analytics on curated data, and Amazon QuickSight to present insights in dashboards. Use Amazon OpenSearch Service when the main need is search, log analytics, or observability rather than warehouse BI, and use Amazon EMR when you need open-source big-data frameworks such as Spark, Trino, Flink, or Hive with more processing flexibility.

In short: Kinesis for streaming, Glue for data integration, Athena for querying data where it lives, Redshift for data warehousing, QuickSight for BI, OpenSearch for search and log analytics, and EMR for large-scale customizable big-data processing.

## Application Integration

| Service | Short description |
| --- | --- |
| Amazon EventBridge | Serverless event bus for application integration. |
| Amazon Simple Notification Service (Amazon SNS) | Pub/sub messaging and notifications. |
| Amazon Simple Queue Service (Amazon SQS) | Fully managed message queues. |
| AWS Step Functions | Visual workflow orchestration for distributed applications. |

## Business Applications

| Service | Short description |
| --- | --- |
| Amazon Connect | Cloud contact center service. |
| Amazon Simple Email Service (Amazon SES) | Cloud email sending and receiving. |

## Cloud Financial Management

| Service | Short description |
| --- | --- |
| AWS Budgets | Set and track cost or usage budgets. |
| AWS Cost and Usage Reports (CUR) | CUR is the detailed underlying dataset. It exports cost and usage data to your Amazon S3 bucket in CSV or Parquet so you can do custom analysis with tools such as Amazon Athena, Amazon Redshift, Amazon QuickSight, or spreadsheets. |
| AWS Cost Explorer | Built-in interface and API for visualizing, filtering, grouping, and forecasting AWS spending over time. |
| AWS Marketplace | Buy and deploy third-party software on AWS. |

In short: use CUR when you need raw, comprehensive data for custom reporting, chargeback, or deep analysis; use Cost Explorer when you want quick charts, trend analysis, and forecasts without building your own reporting pipeline.

## Compute

| Service | Short description |
| --- | --- |
| AWS Batch | Run and scale batch computing jobs. |
| Amazon EC2 | Resizable virtual servers in the cloud. |
| AWS Elastic Beanstalk | Managed platform for quickly deploying and scaling traditional web apps and APIs without managing the underlying infrastructure yourself. |
| AWS Lambda | Serverless compute for event-driven code, APIs, automation, and data processing without managing servers or clusters. |
| Amazon Lightsail | Low-cost simplified VPS platform for small websites, blogs, dev/test environments, and basic business apps with predictable monthly pricing. |
| AWS Outposts | Extends AWS infrastructure on premises for hybrid workloads that need low latency to local systems, local processing, or data residency. |

## Containers

| Service | Short description |
| --- | --- |
| Amazon Elastic Container Registry (Amazon ECR) | Managed registry for storing, scanning, signing, and sharing container images and artifacts used by ECS, EKS, and CI/CD pipelines. |
| Amazon Elastic Container Service (Amazon ECS) | AWS-native container orchestration for running containerized apps, microservices, and batch workloads on EC2 or with serverless Fargate. |
| Amazon Elastic Kubernetes Service (Amazon EKS) | Managed Kubernetes for teams that want Kubernetes-compatible tooling and portability for cloud-native, hybrid, or large-scale container workloads on EC2 or Fargate. |
| AWS Fargate | Serverless, pay-as-you-go compute engine for containers running on ECS or EKS when you want containers without managing servers. |

## Customer Enablement

| Service | Short description |
| --- | --- |
| AWS Support | Support plans and technical help from AWS. |

## Database

| Service | Short description |
| --- | --- |
| Amazon Aurora | High-performance MySQL- and PostgreSQL-compatible relational database. |
| Amazon DocumentDB | Managed document database with MongoDB compatibility. |
| Amazon DynamoDB | Serverless NoSQL key-value and document database. |
| Amazon ElastiCache | Managed in-memory caching with Valkey, Redis OSS, or Memcached. |
| Amazon Neptune | Managed graph database service. |
| Amazon RDS | Managed relational database service across multiple database engines. |

## Developer Tools

| Service | Short description |
| --- | --- |
| AWS CLI | Command line tool for AWS. |
| AWS CodeBuild | Managed build and test service. |
| AWS CodePipeline | Continuous integration and delivery pipelines. |
| AWS X-Ray | Trace and analyze application requests. |

## End User Computing

| Service | Short description |
| --- | --- |
| Amazon AppStream 2.0 | Stream desktop apps to web browsers. |
| Amazon WorkSpaces | Managed cloud virtual desktops. |
| Amazon WorkSpaces Secure Browser | Managed isolated browser sessions. |

For differentiation: Amazon AppStream 2.0 documentation now describes the service as Amazon WorkSpaces Applications, a fully managed application streaming service that gives users instant access to desktop applications without giving them a full desktop. Amazon WorkSpaces is for full virtual desktops, including persistent personal desktops or non-persistent pooled desktops, that users access from devices or web browsers. Amazon WorkSpaces Secure Browser, previously called WorkSpaces Web, is narrower than both: AWS documentation describes it as a fully managed hosted browser service for secure access to internal websites and SaaS apps.

In short: AppStream 2.0 is for individual apps, WorkSpaces is for complete desktops, and Secure Browser is for browser-based access only.

## Frontend Web and Mobile

| Service | Short description |
| --- | --- |
| AWS Amplify | Frontend and full-stack web/mobile platform with managed hosting, Git-based workflows, CI/CD, and integrated app features such as auth, data, storage, and functions. |
| AWS AppSync | Managed GraphQL APIs with real-time data sync. |

## Internet of Things (IoT)

| Service | Short description |
| --- | --- |
| AWS IoT Core | Connect and manage IoT devices securely. |

## Machine Learning

| Service | Short description |
| --- | --- |
| Amazon Comprehend | Natural language processing for text insights. |
| Amazon Kendra | Intelligent enterprise search service. |
| Amazon Lex | Build conversational AI chatbots and voice interfaces. |
| Amazon Polly | Turn text into lifelike speech. |
| Amazon Q | Generative AI assistant for work and AWS. |
| Amazon Rekognition | Analyze images and video for objects, faces, text, and moderation. |
| Amazon SageMaker AI | Build, train, and deploy ML models. |
| Amazon Textract | Extract text and data from documents. |
| Amazon Transcribe | Automatic speech-to-text transcription. |
| Amazon Translate | Neural machine translation service. |

## Management and Governance

### Monitoring, Audit, and Configuration

| Service | Short description |
| --- | --- |
| AWS CloudTrail | Record AWS API and account activity across services. |
| Amazon CloudWatch | Metrics, logs, alarms, and observability across AWS workloads. |
| AWS Config | Track AWS resource configurations, changes, and compliance. |
| AWS Health Dashboard | Personalized AWS health events and notices. |

### Operations and Automation

| Service | Short description |
| --- | --- |
| AWS Auto Scaling | Automatically adjust resource capacity. |
| AWS CloudFormation | Infrastructure as code with templates. |
| AWS Systems Manager | Manage nodes at scale with patching, automation, secure access, and fleet visibility. |
| Service Quotas | Centrally view quotas, track utilization, and request quota increases. |

### Governance and Administration

| Service | Short description |
| --- | --- |
| AWS Control Tower | Landing-zone service to establish and govern a multi-account AWS environment using AWS best practices and preconfigured controls. |
| AWS Organizations | Foundation for multi-account management: group accounts, apply policies, and manage consolidated billing across AWS accounts. |
| AWS Service Catalog | Create and govern a curated catalog of approved cloud products and IaC templates that users can launch through self-service. |
| AWS License Manager | Manage, track, and control software licenses across AWS and on-premises environments. |
| AWS Management Console | Web interface that provides centralized access to AWS services and account tools; it is the UI, not the governance service itself. |

Study shortcut: Organizations manages accounts, Control Tower sets up and governs the multi-account environment, and the Management Console is the UI you use to work with AWS.

### Optimization and Best Practices

| Service | Short description |
| --- | --- |
| AWS Compute Optimizer | Rightsizing recommendations for AWS resources. |
| AWS Trusted Advisor | Automated best practice checks and recommendations for your AWS environment. |
| AWS Well-Architected Tool | Guided workload reviews against AWS Well-Architected best-practice pillars. |

## Migration and Transfer

| Service | Short description | How to tell it apart |
| --- | --- | --- |
| AWS Application Discovery Service | Collect inventory, utilization, and dependency data from on-premises servers and databases to help assess and plan migrations. | Discovery tool: helps you understand what you have before migrating. It does not actually move servers or database data. |
| AWS Application Migration Service | Highly automated lift-and-shift service that replicates and moves physical, virtual, or cloud servers into AWS with minimal changes. | Server rehost tool: use it when you want to move whole servers and applications to AWS quickly, usually into Amazon EC2. |
| AWS Database Migration Service (AWS DMS) | Migrate and continuously replicate database data with minimal downtime, including homogeneous and heterogeneous database migrations. | Database move tool: use it to move the data itself. Pair it with AWS SCT when database schema or code must be converted. |
| Migration Evaluator | Builds a data-driven migration business case by analyzing on-premises inventory, utilization, licensing, and projected AWS costs. | Cost-assessment tool: use it before migration to estimate savings, target sizing, and the financial case. It does not perform the migration. |
| AWS Migration Hub | Central place to discover servers, group them into applications, and track migration progress across multiple AWS migration tools. | Tracking tool: gives program-level visibility across migrations. It coordinates and reports status rather than moving workloads itself. |
| AWS Schema Conversion Tool (AWS SCT) | Converts database schemas, SQL code, and some ETL processes so workloads can move to AWS database targets such as Aurora, Amazon RDS, or Amazon Redshift. | Conversion tool: use it when changing database engines or modernizing database code. It prepares the schema, while DMS typically handles the data movement. |
| AWS Snow Family | Physical devices for offline data transfer and edge processing when moving large datasets over the network would be too slow, costly, or impractical. | Offline transfer and edge device family: use it for remote sites, limited bandwidth, disconnected environments, or petabyte-scale moves rather than normal online migration. |

Study shortcut: Application Discovery Service tells you what you have, Migration Evaluator tells you whether the move makes financial sense, Migration Hub tracks the migration program, Application Migration Service moves whole servers, AWS DMS moves database data, AWS SCT converts schemas and related code, and AWS Snow Family handles offline transfer and edge cases.

Current AWS docs note that AWS Application Discovery Service and AWS Migration Hub are no longer open to new customers, but the distinctions above are still useful for understanding older AWS migration tooling and exam-style service roles.

## Networking and Content Delivery

### Edge Delivery, DNS, and API Entry Points

| Service | Short description |
| --- | --- |
| Amazon API Gateway | Create, publish, and secure REST, HTTP, and WebSocket APIs. |
| Amazon CloudFront | Global content delivery network (CDN). |
| AWS Global Accelerator | Network-layer traffic acceleration to healthy application endpoints using static IPs and the AWS global network for better performance and fast failover. |
| Amazon Route 53 | DNS, domains, and traffic routing. |

### Core Networking and Private Access

| Service | Short description |
| --- | --- |
| Amazon VPC | Logically isolated virtual network where you place AWS resources and control subnets, routing, and security. |
| AWS Transit Gateway | Central cloud router that connects multiple VPCs and on-premises networks through one hub. |
| AWS PrivateLink | Private connectivity to AWS services, SaaS, and VPC resources without using the public internet. |

Study shortcut: VPC is your private AWS network, Transit Gateway is the hub that links many networks, and PrivateLink is for privately reaching services and resources.

### Hybrid and VPN Connectivity

| Service | Short description |
| --- | --- |
| AWS Direct Connect | Dedicated private network connection from your site to AWS for more consistent bandwidth and lower-latency private connectivity. |
| AWS VPN | Managed umbrella for AWS VPN connectivity, including Site-to-Site VPN and Client VPN. |
| AWS Site-to-Site VPN | Managed IPsec VPN between your on-premises network or device and AWS for network-to-network hybrid connectivity over the internet. |
| AWS Client VPN | Managed remote-access VPN for individual users to securely reach AWS and on-premises resources from anywhere. |

When to use which: use Direct Connect when you want a dedicated private link to AWS; use Site-to-Site VPN when you need to connect an office or data center network to AWS over encrypted tunnels; use Client VPN when individual users need remote access; use AWS VPN as the umbrella term for the managed VPN options.

## Security, Identity, and Compliance

### Compliance and Audit

| Service | Short description |
| --- | --- |
| AWS Artifact | On-demand access to AWS and ISV compliance reports and certain agreements; use it to read reports and accept agreements. |
| AWS Audit Manager | Continuously collects audit evidence and maps it to frameworks to simplify audits and assessments. |

### Identity, Directory, and Access

| Service | Short description |
| --- | --- |
| AWS Identity and Access Management (IAM) | Core AWS permissions service for managing access with users, roles, and policies. |
| AWS IAM Identity Center | Workforce single sign-on and centralized multi-account access to AWS accounts and applications. |
| Amazon Cognito | Customer identity service for end-user sign-up, sign-in, and access control in applications. |
| AWS Directory Service | Managed Microsoft Active Directory and related directory options for AD-dependent workloads. |
| AWS Resource Access Manager (AWS RAM) | Securely share supported AWS resources across AWS accounts. |

### Data Protection and Key Management

| Service | Short description |
| --- | --- |
| AWS Certificate Manager (ACM) | Provision and manage public and private SSL/TLS certificates; use it for certificates, not keys or secrets. |
| AWS Key Management Service (AWS KMS) | Managed service to create and control encryption keys and perform cryptographic operations. |
| AWS CloudHSM | Single-tenant hardware security modules that you manage when you need dedicated hardware-backed key control and stronger compliance alignment. |
| AWS Secrets Manager | Store, manage, and rotate passwords, API keys, and other secrets securely. |
| Amazon Macie | Data security service that discovers sensitive data like PII in S3 and highlights data security risks using ML and pattern matching. |

### Detection and Investigation

| Service | Short description |
| --- | --- |
| Amazon GuardDuty | Intelligent threat detection service that monitors AWS accounts, workloads, and data and produces security findings. |
| Amazon Inspector | Vulnerability management service that automatically discovers and scans workloads and code repositories for software issues and unintended network exposure. |
| Amazon Detective | Investigation service that analyzes and visualizes security data and relationships to explain findings and activity. |
| AWS Security Hub | Central security service that correlates, prioritizes, and helps respond to findings and posture signals from AWS and partner tools. |

Study shortcut: GuardDuty detects threats, Detective investigates them, Inspector finds vulnerabilities, and Macie finds sensitive data.

### Network and Application Protection

| Service | Short description |
| --- | --- |
| AWS WAF | Web application firewall for HTTP applications that blocks common exploits, bots, and unwanted web requests. |
| AWS Shield | Managed protection for applications and networks against DDoS attacks, especially when you need advanced mitigation. |
| AWS Firewall Manager | Centrally deploy and manage WAF, Shield, and firewall policies across accounts and resources. |

## Storage

| Service | Short description |
| --- | --- |
| AWS Backup | Centralized backup management across AWS services. |
| Amazon Elastic Block Store (Amazon EBS) | Block storage for EC2 instances. |
| Amazon Elastic File System (Amazon EFS) | Elastic shared file storage for Linux workloads. |
| AWS Elastic Disaster Recovery | Low-cost disaster recovery to AWS. |
| Amazon FSx | Managed high-performance file systems for Windows, Lustre, OpenZFS, and ONTAP. |
| Amazon S3 | Scalable object storage service. |
| Amazon S3 Glacier | Low-cost archival storage classes in S3. |
| AWS Storage Gateway | Hybrid storage between on-premises and AWS. |
