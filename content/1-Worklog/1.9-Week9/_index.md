---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}

### Week 9 Objectives:

- Connect and get acquainted with members of First Cloud Journey.
- Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                 | Start Date | Completion Date | Reference Material                  |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------- |
| 2   | - **Workshop:** Deploy AWS Backup to the System <br>&emsp; + Create backup plans <br>&emsp; + Automate backups for EBS, RDS, DynamoDB <br>&emsp; + Test restore operations <br>&emsp; + Configure SNS notifications  | 03/11/2025 | 03/11/2025      | <https://000013.awsstudygroup.com/> |
| 3   | - **Workshop:** Setting up VPC Peering <br>&emsp; + Create VPC Peering connections <br>&emsp; + Configure Network ACLs <br>&emsp; + Update route tables <br>&emsp; + Enable cross-peer DNS                           | 04/11/2025 | 04/11/2025      | <https://000019.awsstudygroup.com/> |
| 4   | - **Workshop:** Set up AWS Transit Gateway <br>&emsp; + Create Transit Gateway <br>&emsp; + Configure TGW attachments <br>&emsp; + Set up TGW route tables <br>&emsp; + Connect multiple VPCs                        | 05/11/2025 | 05/11/2025      | <https://000020.awsstudygroup.com/> |
| 5   | - **Workshop:** Event-Driven Architecture with SNS and SQS <br>&emsp; + Create SNS topics <br>&emsp; + Configure SQS queues <br>&emsp; + Implement message filtering <br>&emsp; + Build pub/sub patterns             | 06/11/2025 | 06/11/2025      | <https://000077.awsstudygroup.com/> |
| 6   | - **Workshop:** Secure Data Sharing with EBS NVMe Reservation <br>&emsp; + Configure EBS Multi-Attach <br>&emsp; + Implement NVMe reservations <br>&emsp; + Set up PostgreSQL backup <br>&emsp; + Test data recovery | 07/11/2025 | 07/11/2025      | <https://100000.awsstudygroup.com/> |

### Week 9 Achievements:

- **Day 2 - AWS Backup Implementation:**

  - Mastered AWS Backup for centralized data protection
  - Created automated backup plans for AWS resources
  - Configured backups for EBS Volumes, RDS Databases, DynamoDB Tables
  - Set up backup for EFS File Systems
  - Tested backup and restore operations
  - Configured AWS SNS for backup notifications
  - Implemented backup policies from a single location
  - Automated data protection workflows
  - Ensured data recovery capabilities
  - Applied backup best practices for business continuity
  - Validated backups through restore testing

- **Day 3 - VPC Peering:**

  - Understood VPC Peering concepts and architecture
  - Created VPC Peering connections between VPCs
  - Configured Network ACLs for stateless filtering
  - Updated route tables for peering communication
  - Enabled cross-peering DNS for name resolution
  - Implemented security groups and NACLs together
  - Used private IPv4/IPv6 addresses for routing
  - Enhanced security by avoiding public internet traversal
  - Reduced latency with direct VPC connections
  - Applied defense-in-depth security strategies
  - Understood non-transitive peering limitations

- **Day 4 - AWS Transit Gateway:**

  - Mastered AWS Transit Gateway for scalable networking
  - Created Transit Gateway as cloud router hub
  - Configured Transit Gateway Attachments for VPCs
  - Set up Transit Gateway Route Tables
  - Connected multiple VPCs through single gateway
  - Simplified network architecture vs VPC Peering
  - Implemented centralized network management
  - Reduced operational complexity
  - Understood TGW vs VPC Peering trade-offs
  - Applied transit gateway for enterprise networking
  - Configured encryption in transit

- **Day 5 - Event-Driven Architecture:**

  - Built event-driven architectures with SNS and SQS
  - Created Amazon SNS topics for pub/sub messaging
  - Configured Amazon SQS queues for message processing
  - Implemented message filtering with filter policies
  - Designed simple pub/sub patterns
  - Applied advanced message filtering techniques
  - Used JSON attributes for message differentiation
  - Offloaded message routing logic from publishers
  - Enabled independent development team operations
  - Improved application scalability with events
  - Built decoupled microservices architecture

- **Day 6 - EBS NVMe Reservation:**

  - Implemented secure data sharing with EBS NVMe reservations
  - Configured EBS Multi-Attach for io2 volumes
  - Used NVMe reservations for storage fencing
  - Maintained data consistency across instances
  - Set up PostgreSQL on multiple EC2 instances
  - Implemented database backup configurations
  - Tested data recovery across VPCs
  - Applied industry-standard storage fencing protocols
  - Coordinated access control for shared volumes
  - Worked with SUSE Linux, RHEL, and Amazon Linux 2
  - Enhanced security with separate VPCs
  - Optimized performance with efficient data management

- **Overall Week 9 Results:**
  - Completed 5 workshops on Networking, Backup, and Event-Driven Architecture
  - Mastered data protection with AWS Backup
  - Built scalable network architectures with VPC Peering and Transit Gateway
  - Implemented event-driven systems with SNS/SQS
  - Secured data sharing with EBS NVMe reservations
  - Ready to design enterprise-grade cloud architectures
