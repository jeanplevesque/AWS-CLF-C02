# AWS CLF-C02 Study Table

Concise study summaries based on current official AWS product and documentation pages checked on 2026-05-19.

## Analytics

| Service | Very short description |
| --- | --- |
| Amazon Athena | Serverless SQL queries on S3 data. |
| Amazon EMR | Managed big data platform for Spark, Hadoop, and analytics. |
| AWS Glue | Serverless data integration and ETL. |
| Amazon Kinesis | Real-time data streaming and processing. |
| Amazon OpenSearch Service | Managed search, log analytics, and observability. |
| Amazon QuickSight | Serverless business intelligence dashboards and analytics. |
| Amazon Redshift | Cloud data warehouse for analytics. |

## Application Integration

| Service | Very short description |
| --- | --- |
| Amazon EventBridge | Serverless event bus for application integration. |
| Amazon Simple Notification Service (Amazon SNS) | Pub/sub messaging and notifications. |
| Amazon Simple Queue Service (Amazon SQS) | Fully managed message queues. |
| AWS Step Functions | Visual workflow orchestration for distributed applications. |

## Business Applications

| Service | Very short description |
| --- | --- |
| Amazon Connect | Cloud contact center service. |
| Amazon Simple Email Service (Amazon SES) | Cloud email sending and receiving. |

## Cloud Financial Management

| Service | Very short description |
| --- | --- |
| AWS Budgets | Set and track cost or usage budgets. |
| AWS Cost and Usage Reports | Detailed billing and usage exports. |
| AWS Cost Explorer | Analyze and forecast AWS spending. |
| AWS Marketplace | Buy and deploy third-party software on AWS. |

## Compute

| Service | Very short description |
| --- | --- |
| AWS Batch | Run and scale batch computing jobs. |
| Amazon EC2 | Resizable virtual servers in the cloud. |
| AWS Elastic Beanstalk | Deploy and scale web apps simply. |
| Amazon Lightsail | Simplified VPS, storage, and networking. |
| AWS Outposts | AWS infrastructure and services on premises. |

## Containers

| Service | Very short description |
| --- | --- |
| Amazon Elastic Container Registry (Amazon ECR) | Managed container image registry for ECS, EKS, and other runtimes. |
| Amazon Elastic Container Service (Amazon ECS) | Managed container orchestration service that can run on EC2 or Fargate. |
| Amazon Elastic Kubernetes Service (Amazon EKS) | Managed Kubernetes on AWS that can run with EC2 or Fargate. |

## Customer Enablement

| Service | Very short description |
| --- | --- |
| AWS Support | Support plans and technical help from AWS. |

## Database

| Service | Very short description |
| --- | --- |
| Amazon Aurora | High-performance MySQL/PostgreSQL-compatible relational database. |
| Amazon DocumentDB | Managed document database with MongoDB compatibility. |
| Amazon DynamoDB | Serverless NoSQL key-value database. |
| Amazon ElastiCache | Managed in-memory caching service. |
| Amazon Neptune | Managed graph database service. |
| Amazon RDS | Managed relational database service. |

## Developer Tools

| Service | Very short description |
| --- | --- |
| AWS CLI | Command line tool for AWS. |
| AWS CodeBuild | Managed build and test service. |
| AWS CodePipeline | Continuous integration and delivery pipelines. |
| AWS X-Ray | Trace and analyze application requests. |

## End User Computing

For differentiation: Amazon AppStream 2.0 documentation now describes the service as Amazon WorkSpaces Applications, a fully managed application streaming service that gives users instant access to desktop applications without giving them a full desktop. Amazon WorkSpaces is for full virtual desktops, including persistent personal desktops or non-persistent pooled desktops, that users access from devices or web browsers. Amazon WorkSpaces Secure Browser, previously called WorkSpaces Web, is narrower than both: AWS documentation describes it as a fully managed hosted browser service for secure access to internal websites and SaaS apps.

In short: AppStream 2.0 is for individual apps, WorkSpaces is for complete desktops, and Secure Browser is for browser-based access only.

| Service | Very short description |
| --- | --- |
| Amazon AppStream 2.0 | Stream desktop apps to web browsers. |
| Amazon WorkSpaces | Managed cloud virtual desktops. |
| Amazon WorkSpaces Secure Browser | Managed isolated browser sessions. |

## Frontend Web and Mobile

| Service | Very short description |
| --- | --- |
| AWS Amplify | Build and host full-stack web and mobile apps. |
| AWS AppSync | Managed GraphQL APIs with real-time data sync. |

## Internet of Things (IoT)

| Service | Very short description |
| --- | --- |
| AWS IoT Core | Connect and manage IoT devices securely. |

## Machine Learning

| Service | Very short description |
| --- | --- |
| Amazon Comprehend | Natural language processing for text insights. |
| Amazon Kendra | Intelligent enterprise search service. |
| Amazon Lex | Build conversational voice and text bots. |
| Amazon Polly | Turn text into lifelike speech. |
| Amazon Q | Generative AI assistant for work and AWS. |
| Amazon Rekognition | Analyze images and video with AI. |
| Amazon SageMaker AI | Build, train, and deploy ML models. |
| Amazon Textract | Extract text and data from documents. |
| Amazon Transcribe | Automatic speech-to-text transcription. |
| Amazon Translate | Neural machine translation service. |

## Management and Governance

| Service | Very short description |
| --- | --- |
| AWS Auto Scaling | Automatically adjust resource capacity. |
| AWS CloudFormation | Infrastructure as code with templates. |
| AWS CloudTrail | Record AWS API and account activity across services. |
| Amazon CloudWatch | Metrics, logs, alarms, and observability across AWS workloads. |
| AWS Compute Optimizer | Rightsizing recommendations for AWS resources. |
| AWS Config | Track AWS resource configurations, changes, and compliance. |
| AWS Control Tower | Set up and govern multi-account AWS environments. |
| AWS Health Dashboard | Personalized AWS health events and notices. |
| AWS License Manager | Track and control software licenses. |
| AWS Management Console | Web interface for managing AWS. |
| AWS Organizations | Govern and manage multiple AWS accounts. |
| AWS Service Catalog | Approved self-service cloud products. |
| Service Quotas | View and manage service limits. |
| AWS Systems Manager | Operations, patching, and automation at scale. |
| AWS Trusted Advisor | Best practice checks for AWS environments. |
| AWS Well-Architected Tool | Review workloads against AWS best practices. |

## Migration and Transfer

| Service | Very short description |
| --- | --- |
| AWS Application Discovery Service | Discover on-premises servers and dependencies. |
| AWS Application Migration Service | Lift-and-shift server migration to AWS. |
| AWS Database Migration Service (AWS DMS) | Migrate databases with minimal downtime. |
| Migration Evaluator | Estimate migration costs and business case. |
| AWS Migration Hub | Track migrations across AWS tools. |
| AWS Schema Conversion Tool (AWS SCT) | Convert database schemas for migration. |
| AWS Snow Family | Edge devices for offline compute and data transfer. |

## Networking and Content Delivery

| Service | Very short description |
| --- | --- |
| Amazon API Gateway | Create, publish, and manage APIs. |
| Amazon CloudFront | Global content delivery network. |
| AWS Direct Connect | Dedicated private network link to AWS. |
| AWS Global Accelerator | Improve global app performance and availability. |
| AWS PrivateLink | Private access to services over VPC endpoints. |
| Amazon Route 53 | DNS, domains, and traffic routing. |
| AWS Transit Gateway | Central hub for VPC and network connectivity. |
| Amazon VPC | Isolated virtual networking in AWS. |
| AWS VPN | Managed VPN connectivity to AWS. |
| AWS Site-to-Site VPN | IPsec VPN between AWS and on-premises networks. |
| AWS Client VPN | Managed remote-access VPN for users. |

## Security, Identity, and Compliance

| Service | Very short description | How to tell it apart |
| --- | --- | --- |
| AWS Artifact | On-demand AWS compliance reports and agreements. | Read AWS compliance reports and accept agreements. |
| AWS Audit Manager | Collect audit evidence continuously. | Automates evidence collection for audits and assessments. |
| AWS Certificate Manager (ACM) | Provision and manage TLS certificates. | For SSL/TLS certificates, not keys or secrets. |
| AWS CloudHSM | Dedicated hardware security modules. | Single-tenant HSM control when you manage the hardware-backed keys. |
| Amazon Cognito | User sign-up, sign-in, and access control. | Customer app identity for end users and apps. |
| Amazon Detective | Investigate security findings visually. | Investigates findings using log data from AWS resources. |
| AWS Directory Service | Managed Microsoft AD and directory options. | Managed Active Directory for AD-dependent workloads. |
| AWS Firewall Manager | Centrally manage firewall rules and protections. | Pushes WAF and firewall policies across accounts and resources. |
| Amazon GuardDuty | Intelligent threat detection for AWS. | Detects threats and produces findings. |
| AWS Identity and Access Management (IAM) | Manage access with users, roles, and policies. | Core AWS permissions service for users, roles, and policies. |
| AWS IAM Identity Center | Workforce access and single sign-on. | Workforce SSO and centralized multi-account access. |
| Amazon Inspector | Automated vulnerability and exposure scanning. | Scans EC2, container images, Lambda, and code repositories. |
| AWS Key Management Service (AWS KMS) | Create and control encryption keys. | Managed encryption keys and cryptographic operations. |
| Amazon Macie | Discover and protect sensitive data in S3. | Focused on sensitive data discovery in S3. |
| AWS Resource Access Manager (AWS RAM) | Share AWS resources across accounts. | Shares resources across AWS accounts. |
| AWS Secrets Manager | Store and rotate secrets securely. | Stores and rotates passwords, API keys, and secrets. |
| AWS Security Hub | Centralize security findings and posture. | Aggregates signals from AWS and partner security tools. |
| AWS Shield | Managed DDoS protection. | For DDoS protection, especially advanced mitigation. |
| AWS WAF | Web application firewall for HTTP apps. | Blocks web exploits, bots, and bad HTTP requests. |

## Serverless

| Service | Very short description |
| --- | --- |
| AWS Fargate | Serverless compute for containers used by ECS or EKS. |
| AWS Lambda | Run code without managing servers. |

## Storage

| Service | Very short description |
| --- | --- |
| AWS Backup | Centralized backup management across AWS services. |
| Amazon Elastic Block Store (Amazon EBS) | Block storage for EC2 instances. |
| Amazon Elastic File System (Amazon EFS) | Elastic shared file storage for Linux workloads. |
| AWS Elastic Disaster Recovery | Low-cost disaster recovery to AWS. |
| Amazon FSx | Managed high-performance file systems. |
| Amazon S3 | Scalable object storage service. |
| Amazon S3 Glacier | Low-cost archival storage classes in S3. |
| AWS Storage Gateway | Hybrid storage between on-premises and AWS. |
