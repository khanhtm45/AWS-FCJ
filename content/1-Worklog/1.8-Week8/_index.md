---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}

### Week 8 Objectives:

- Connect and get acquainted with members of First Cloud Journey.
- Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                | Start Date | Completion Date | Reference Material                  |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------- |
| 2   | - **Workshop:** AWS Web Application Firewall (WAF) <br>&emsp; + Learn WAF basics <br>&emsp; + Create WAF rules <br>&emsp; + Configure web ACLs <br>&emsp; + Protect web applications                                | 27/10/2025 | 27/10/2025      | <https://000026.awsstudygroup.com/> |
| 3   | - **Workshop:** Encrypt at Rest with AWS KMS <br>&emsp; + Create KMS keys <br>&emsp; + Encrypt S3 objects <br>&emsp; + Configure CloudTrail logging <br>&emsp; + Query logs with Athena                             | 28/10/2025 | 28/10/2025      | <https://000033.awsstudygroup.com/> |
| 4   | - **Workshop:** AWS Secrets Manager with RDS and Fargate <br>&emsp; + Store RDS credentials <br>&emsp; + Configure secret rotation <br>&emsp; + Access secrets from Fargate <br>&emsp; + Test with shell scripts    | 29/10/2025 | 29/10/2025      | <https://000096.awsstudygroup.com/> |
| 5   | - **Workshop:** Implementing AWS Cognito Across Sites <br>&emsp; + Create Cognito User Pools <br>&emsp; + Configure Identity Pools <br>&emsp; + Implement authentication <br>&emsp; + Deploy cross-site integration | 30/10/2025 | 30/10/2025      | <https://000141.awsstudygroup.com/> |
| 6   | - **Workshop:** Autonomous Patching with EC2 Image Builder <br>&emsp; + Configure EC2 Image Builder <br>&emsp; + Create AMI pipeline <br>&emsp; + Automate with Systems Manager <br>&emsp; + Blue/green deployment  | 31/10/2025 | 31/10/2025      | <https://000099.awsstudygroup.com/> |

### Week 8 Achievements:

- **Day 2 - AWS Web Application Firewall:**

  - Mastered AWS WAF fundamentals for web application protection
  - Created and configured WAF web ACLs
  - Implemented WAF rules for traffic filtering
  - Protected applications from common web exploits
  - Configured rate-based rules to prevent DDoS attacks
  - Used AWS managed rule groups
  - Created custom rule groups for specific requirements
  - Monitored WAF metrics and logs
  - Applied WAF best practices for security
  - Integrated WAF with CloudFront and ALB

- **Day 3 - KMS Encryption at Rest:**

  - Understood AWS Key Management Service (KMS) concepts
  - Created and managed customer master keys (CMKs)
  - Encrypted S3 objects with KMS keys
  - Configured server-side encryption (SSE-KMS)
  - Set up CloudTrail for KMS API logging
  - Used Amazon Athena to query CloudTrail logs
  - Implemented key rotation policies
  - Shared encrypted data securely between accounts
  - Applied encryption best practices for data at rest
  - Managed key policies and grants
  - Ensured compliance with encryption requirements

- **Day 4 - AWS Secrets Manager Integration:**

  - Mastered AWS Secrets Manager for credential management
  - Stored RDS database credentials securely
  - Configured automatic secret rotation
  - Integrated Secrets Manager with Amazon RDS
  - Accessed secrets from EC2 instances
  - Retrieved secrets from AWS Fargate containers
  - Implemented least privilege access with IAM
  - Created Docker containers with secret integration
  - Automated secret management with shell scripts
  - Applied preventative security controls (CSF framework)
  - Built secure VPC architecture with private subnets

- **Day 5 - AWS Cognito Authentication:**

  - Understood Amazon Cognito identity platform
  - Created and configured Cognito User Pools
  - Set up Cognito Identity Pools for AWS access
  - Implemented user authentication for web/mobile apps
  - Integrated third-party identity providers (IdPs)
  - Configured SAML 2.0 and OIDC authentication
  - Issued authenticated JSON Web Tokens (JWTs)
  - Implemented cross-site authentication
  - Used role-based and attribute-based access control
  - Applied OAuth 2.0 authorization flows
  - Built secure user directory with self-service features

- **Day 6 - Autonomous Patching Pipeline:**

  - Built automated patching solution with EC2 Image Builder
  - Created AMI builder pipelines
  - Configured Systems Manager Automation documents
  - Implemented blue/green deployment methodology
  - Used CloudFormation AutoScalingReplacingUpdate policy
  - Automated OS patching for security compliance
  - Reduced operational overhead with automation
  - Ensured minimal interruption to application availability
  - Established traceability for compliance audits
  - Deployed updated AMIs to application clusters
  - Applied Well-Architected security best practices

- **Overall Week 8 Results:**
  - Completed 5 workshops on AWS Security and Automation
  - Mastered web application protection with WAF
  - Implemented encryption at rest with KMS
  - Secured credentials with Secrets Manager
  - Built authentication systems with Cognito
  - Automated patching with EC2 Image Builder
  - Ready to implement enterprise security solutions
