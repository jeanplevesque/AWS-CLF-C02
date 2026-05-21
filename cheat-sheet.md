# AWS CLF-C02 Concept Cheat Sheet

Exam-focused notes for AWS Cloud Practitioner topics that are not already covered in [in-scope-services.md](./in-scope-services.md).

Checked: 2026-05-21

## 1. Core Cloud Ideas

### Benefits of cloud computing

- Trade fixed capital expense for variable expense: pay for what you use.
- Benefit from massive economies of scale: AWS can often deliver lower unit costs.
- Stop guessing capacity: scale up or down instead of overprovisioning.
- Increase speed and agility: provision resources in minutes.
- Stop spending money running and maintaining data centers.
- Go global in minutes: deploy in multiple Regions quickly.

### Cloud service models

- IaaS: most control over compute, storage, and networking. Example mindset: virtual servers.
- PaaS: focus on application deployment while AWS manages more of the platform.
- SaaS: use a finished application managed by the vendor.

### Deployment models

- Cloud-native: built for elastic, managed, API-driven services.
- Hybrid: some workloads stay on premises, others run in AWS.
- On premises: you manage infrastructure in your own facilities.

## 2. AWS Global Infrastructure

- Region: separate geographic area.
- Availability Zone (AZ): one or more discrete data centers in a Region with independent power, cooling, and networking.
- Edge location: CDN and edge-compute site used mainly by services such as CloudFront.
- Choose multiple AZs for higher availability within a Region.
- Choose multiple Regions for geographic redundancy, latency, or compliance needs.

## 3. Well-Architected Framework

AWS Well-Architected helps you evaluate workloads against best practices.

### The 6 pillars

- Operational Excellence: run, monitor, and improve operations.
- Security: protect systems, data, and identities.
- Reliability: recover quickly and meet demand.
- Performance Efficiency: use the right resources and keep performance efficient as needs change.
- Cost Optimization: avoid unnecessary cost and choose the right consumption model.
- Sustainability: minimize the environmental impact of workloads.

### Exam shortcut

- Secure, reliable, cost-aware, efficient, sustainable, and operationally mature.

## 4. AWS Cloud Adoption Framework (AWS CAF)

- AWS CAF helps organizations accelerate cloud-powered digital transformation using AWS best practices.
- Use AWS CAF to identify and prioritize transformation opportunities, assess cloud readiness, and iteratively build a transformation roadmap.

### The 6 perspectives

- Business: align cloud adoption with business goals and measurable outcomes.
- People: address culture, leadership, organizational change, and workforce skills.
- Governance: guide decision-making, risk management, compliance, and value realization.
- Platform: build and modernize an enterprise-grade cloud foundation.
- Security: protect data and workloads while maintaining confidentiality, integrity, and availability.
- Operations: run and support cloud services at a level that meets business needs.

### Transformation phases

- Envision: identify and prioritize cloud transformation opportunities.
- Align: find capability gaps, dependencies, and readiness improvements.
- Launch: deliver pilots in production and prove business value.
- Scale: expand adoption and sustain the benefits.

### Exam shortcut

- AWS CAF = organization and transformation readiness.
- Well-Architected = workload design and operational best practices.

## 5. Shared Responsibility Model

- AWS is responsible for security of the cloud.
- The customer is responsible for security in the cloud.

### AWS typically manages

- Hardware, facilities, networking, Regions, AZs, and the virtualization layer.

### Customer typically manages

- Data.
- Identity and access management choices.
- Guest operating system for EC2.
- Application configuration.
- Security group and network configuration.
- Encryption configuration and traffic protection decisions.

### Exam shortcut

- Managed service means AWS does more.
- EC2 means customer does more than with a serverless service such as Lambda.

## 6. IAM and Access Basics

- Root user: full account access; do not use for everyday work.
- IAM user: identity for a specific person or application.
- IAM group: collection of IAM users.
- IAM role: temporary-access identity assumed by people, applications, or AWS services.
- Policy: JSON document that defines permissions.

### High-yield rules

- Use least privilege.
- Prefer roles and temporary credentials over long-term access keys when possible.
- MFA adds a second authentication factor and should be enabled, especially for privileged access.
- Identity-based policies attach to users, groups, and roles.
- Resource-based policies attach to resources such as S3 buckets.
- Explicit deny overrides allow.

### IAM Identity Center vs IAM

- IAM: account-level identities and permissions for AWS access.
- IAM Identity Center: workforce SSO and centralized access across multiple AWS accounts and applications.

## 7. Network Security Concepts

### Security groups vs network ACLs

| Concept | Security group | Network ACL |
| --- | --- | --- |
| Scope | Instance or ENI level | Subnet level |
| Type | Stateful | Stateless |
| Rules | Allow rules only | Allow and deny rules |
| Evaluation | All rules considered | Rules evaluated in number order |

### Study shortcut

- Security group = virtual firewall for instances.
- Network ACL = subnet guardrail.
- Because NACLs are stateless, return traffic must be allowed explicitly.
- Because security groups are stateful, return traffic is automatically allowed.

## 8. S3 Basics You Should Know

### Core storage types

- Object storage: Amazon S3.
- Block storage: Amazon EBS.
- File storage: Amazon EFS and Amazon FSx.

### S3 storage classes

- S3 Standard: frequently accessed general-purpose storage.
- S3 Intelligent-Tiering: data with unknown or changing access patterns.
- S3 Express One Zone: highest-performance S3 storage class in a single AZ.
- S3 Standard-IA: infrequently accessed data that still needs millisecond retrieval.
- S3 One Zone-IA: infrequently accessed, re-creatable data stored in one AZ.
- S3 Glacier Instant Retrieval: archive data that still needs instant retrieval.
- S3 Glacier Flexible Retrieval: archive data retrieved in minutes or hours.
- S3 Glacier Deep Archive: lowest-cost archive for data rarely accessed.

### S3 security and ownership

- Bucket policies are the primary way to control access to S3 buckets.
- By default, new buckets use Object Ownership: Bucket owner enforced.
- With Bucket owner enforced, ACLs are disabled and the bucket owner owns all objects.
- Modern best practice: keep ACLs disabled unless you have a specific object-level access requirement.
- Block Public Access is commonly used to prevent accidental exposure.

### S3 exam patterns

- Need durable object storage for any amount of data: S3.
- Need archival storage: S3 Glacier storage classes.
- Need changing-access optimization without manual tier selection: S3 Intelligent-Tiering.

## 9. EC2 Pricing and Capacity Concepts

- On-Demand: pay as you go, no long-term commitment.
- Savings Plans: commit to consistent usage in dollars per hour for 1 or 3 years.
- Reserved Instances: commit to a specific instance configuration for 1 or 3 years.
- Spot Instances: use spare capacity at major discount, but instances can be interrupted.
- Dedicated Instances: instances run on single-tenant hardware.
- Dedicated Hosts: entire physical server dedicated to you; useful for license/compliance needs.
- Capacity Reservations: reserve capacity in a specific AZ.

### Exam shortcut

- Unpredictable workload: On-Demand.
- Steady workload with commitment: Savings Plans or Reserved Instances.
- Fault-tolerant interruptible workload: Spot.
- Specific host or license requirement: Dedicated Hosts.

## 10. Migration and Modernization

### The 7 Rs of migration

- Rehost: lift and shift with minimal changes.
- Relocate: move workloads at the hypervisor or platform level with minimal changes.
- Replatform: make limited optimizations without changing the core architecture.
- Repurchase: move to a different product, often SaaS.
- Refactor: re-architect to use cloud-native capabilities.
- Retain: keep it as is for now and revisit later.
- Retire: decommission what is no longer needed.

### Migration shortcuts

- Fastest simple move: rehost.
- Want some cloud benefits without a full redesign: replatform.
- Need full cloud-native redesign: refactor.
- App no longer needed: retire.
- Cannot move yet for business, technical, or compliance reasons: retain.

## 11. Pricing, Billing, and Support Concepts

### Cost ideas

- Pricing is affected by compute time, storage consumed, requests, data transfer, and support plan.
- Inbound data transfer is commonly free; outbound internet transfer is commonly charged.
- The AWS Pricing Calculator helps estimate cost before deployment.

### Billing and account concepts

- Consolidated billing is a benefit of AWS Organizations.
- Tags help allocate and analyze costs.
- Budgets alert on planned spend or usage thresholds.
- Cost Explorer helps visualize and forecast spending.
- CUR gives raw detailed cost and usage data for custom analysis.

### AWS Organizations, OUs, and SCPs

- AWS Organizations helps centrally govern multiple AWS accounts.
- An organizational unit (OU) is a way to group accounts so you can manage them as a single unit.
- OUs can be nested, and accounts inherit applicable organization policies from parent levels.
- Use OUs to separate environments or functions such as production, sandbox, security, or workloads by business unit.
- A service control policy (SCP) is an organization policy that sets the maximum available permissions for member accounts.
- SCPs do not grant permissions. IAM or resource-based policies must still allow the action.
- Effective access in a member account must be allowed by both the applicable SCPs and the account's IAM permissions.
- SCPs affect member accounts, including their root users, but do not affect users or roles in the management account.
- Exam shortcut: OU = account grouping and policy inheritance. SCP = permission guardrail across member accounts.

### AWS Support plans

- Basic Support: included for all accounts.
- Paid plans add faster response times, guidance, and broader support coverage.
- Enterprise-level plans include the highest support level and more proactive guidance.

## 12. Resilience, Availability, and Disaster Recovery

- High availability: keep workloads available despite failures, often across multiple AZs.
- Fault tolerance: keep operating even when components fail.
- Scalability: ability to increase or decrease capacity.
- Elasticity: automatic or rapid scaling with demand.
- Disaster recovery focuses on restoring systems after major failure.
- Backup and restore is the simplest DR pattern, but usually has the highest recovery time.

### Common exam distinctions

- Multi-AZ improves resilience within one Region.
- Multi-Region improves geographic resilience.
- Backups help recovery, but they are not the same as high availability.

## 13. Quick Compare Table

| Need | Best-fit concept |
| --- | --- |
| Temporary permissions for an app or AWS service | IAM role |
| Firewall at instance level | Security group |
| Allow or deny traffic at subnet level | Network ACL |
| Frequently accessed object storage | S3 Standard |
| Unknown or changing S3 access pattern | S3 Intelligent-Tiering |
| Lowest-cost long-term archive | S3 Glacier Deep Archive |
| Predictable compute with commitment | Savings Plans or Reserved Instances |
| Interruptible discounted compute | Spot Instances |
| Centralized multi-account governance | AWS Organizations |
| Group accounts for governance by environment or function | Organizational units (OUs) |
| Set maximum permissions across member accounts | Service control policies (SCPs) |
| Review workload design against best practices | AWS Well-Architected Framework |

## Sources Checked

- https://aws.amazon.com/architecture/well-architected/
- https://aws.amazon.com/cloud-adoption-framework/
- https://docs.aws.amazon.com/whitepapers/latest/overview-aws-cloud-adoption-framework/welcome.html
- https://aws.amazon.com/compliance/shared-responsibility-model/
- https://aws.amazon.com/s3/
- https://aws.amazon.com/s3/storage-classes/
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/acl-overview.html
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html
- https://docs.aws.amazon.com/vpc/latest/userguide/vpc-security-groups.html
- https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html
- https://aws.amazon.com/ec2/pricing/
- https://docs.aws.amazon.com/IAM/latest/UserGuide/id.html
- https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- https://aws.amazon.com/organizations/
- https://aws.amazon.com/organizations/features/
- https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_ous.html
- https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- https://builder.aws.com/content/2cKbgI3WsAYTiDM0J48uEMVqOVW/understanding-the-7-rs-cloud-migration-strategies
