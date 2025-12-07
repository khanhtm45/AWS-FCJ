---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}

### Week 5 Objectives:

- Connect and get acquainted with members of First Cloud Journey.
- Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                                                                        | Start Date | Completion Date | Reference Material                  |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------- |
| 2   | - **Workshop:** VM Import/Export <br>&emsp; + Setup VMware Workstation environment <br>&emsp; + Import VM images to Amazon EC2 <br>&emsp; + Export EC2 instances back to on-premises <br>&emsp; + Manage VM migration lifecycle                                             | 06/10/2025 | 06/10/2025      | <https://000014.awsstudygroup.com/> |
| 3   | - **Workshop:** Database Schema Conversion & Migration <br>&emsp; + Use AWS Schema Conversion Tool (SCT) <br>&emsp; + Configure AWS Database Migration Service (DMS) <br>&emsp; + Perform heterogeneous database migration <br>&emsp; + Monitor and troubleshoot migrations | 07/10/2025 | 07/10/2025      | <https://000043.awsstudygroup.com/> |
| 4   | - **Workshop:** AWS Elastic Disaster Recovery <br>&emsp; + Configure DRS settings and IAM <br>&emsp; + Install DRS agent on source servers <br>&emsp; + Configure EC2 Launch Templates <br>&emsp; + Perform failover testing                                                | 08/10/2025 | 08/10/2025      | <https://000100.awsstudygroup.com/> |
| 5   | - **Workshop:** Optimizing EC2 Costs with Lambda <br>&emsp; + Create instance tags for automation <br>&emsp; + Configure IAM roles for Lambda <br>&emsp; + Create Lambda functions for auto start/stop <br>&emsp; + Schedule with EventBridge                               | 09/10/2025 | 09/10/2025      | <https://000022.awsstudygroup.com/> |
| 6   | - **Workshop:** Getting Started with Grafana <br>&emsp; + Install Grafana on Linux EC2 <br>&emsp; + Configure data sources <br>&emsp; + Create monitoring dashboards <br>&emsp; + Visualize CloudWatch metrics                                                              | 10/10/2025 | 10/10/2025      | <https://000029.awsstudygroup.com/> |

### Week 5 Achievements:

- **Day 2 - VM Import/Export:**

  - Mastered VM Import/Export for hybrid cloud migrations
  - Set up VMware Workstation virtualization environment
  - Learned to export VM images from on-premises
  - Imported virtual machine images to Amazon EC2
  - Configured VM conversion settings and parameters
  - Uploaded VM images to S3 for import process
  - Exported EC2 instances back to on-premises format
  - Understood VM compatibility requirements
  - Managed VM migration lifecycle and dependencies
  - Applied best practices for VM migrations
  - Enabled disaster recovery and backup scenarios

- **Day 3 - Database Migration:**

  - Gained expertise in AWS Database Migration Service (DMS)
  - Mastered AWS Schema Conversion Tool (SCT)
  - Performed heterogeneous database migrations
  - Converted database schemas between different engines
  - Configured DMS source and target endpoints
  - Set up serverless DMS replication
  - Implemented continuous data replication
  - Monitored migration tasks and metrics
  - Troubleshot common migration issues
  - Minimized downtime during production migrations
  - Migrated from on-premises to RDS/Aurora
  - Converted stored procedures and functions

- **Day 4 - AWS Elastic Disaster Recovery:**

  - Understood AWS Elastic Disaster Recovery (DRS) service
  - Configured DRS settings and replication
  - Created DRS IAM users and roles
  - Installed DRS agent on source servers (Windows/Linux)
  - Configured continuous block-level replication
  - Set up EC2 Launch Templates for recovery
  - Performed drill and recovery failover operations
  - Tested recovery point objectives (RPO) and recovery time objectives (RTO)
  - Monitored replication lag and health
  - Implemented point-in-time recovery
  - Minimized downtime and data loss
  - Applied DR best practices for business continuity

- **Day 5 - Lambda Cost Optimization:**

  - Implemented EC2 cost optimization with Lambda
  - Created instance tagging strategy for automation
  - Configured IAM roles with proper permissions for Lambda
  - Developed Lambda functions for EC2 start/stop automation
  - Scheduled Lambda execution with EventBridge (CloudWatch Events)
  - Filtered instances by tags for selective automation
  - Implemented time-based instance scheduling
  - Calculated cost savings from automated schedules
  - Learned about Savings Plans for 24/7 instances
  - Applied cost optimization strategies
  - Monitored Lambda execution and errors
  - Reduced unnecessary EC2 runtime costs

- **Day 6 - Grafana Monitoring:**

  - Installed and configured Grafana on Linux EC2
  - Set up Grafana service and security
  - Integrated Grafana with CloudWatch data source
  - Created custom monitoring dashboards
  - Visualized AWS metrics and logs
  - Configured dashboard panels and queries
  - Set up alerts and notifications
  - Monitored EC2, RDS, and other AWS resources
  - Created time-series visualizations
  - Implemented real-time monitoring
  - Applied dashboard best practices
  - Enhanced observability with Grafana

- **Overall Achievements:**
  - Completed 5 advanced workshops on migration, DR, and optimization
  - Mastered VM and database migration to AWS
  - Implemented disaster recovery with AWS DRS
  - Automated cost optimization with Lambda
  - Built comprehensive monitoring with Grafana
  - Ready to design resilient, cost-effective cloud architectures
