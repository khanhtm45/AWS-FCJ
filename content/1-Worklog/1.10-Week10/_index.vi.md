---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 10:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                             | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** Triển khai CI/CD với ECS Container <br>&emsp; + Thiết lập CI/CD cho ECS <br>&emsp; + Triển khai với GitLab và GitHub <br>&emsp; + Tích hợp CodeBuild <br>&emsp; + Giám sát với Container Insights     | 10/11/2025   | 10/11/2025      | <https://000017.awsstudygroup.com/> |
| 3   | - **Workshop:** Triển khai Ứng dụng lên EC2 với CodePipeline <br>&emsp; + Cấu hình CodeCommit repository <br>&emsp; + Thiết lập CodeBuild <br>&emsp; + Triển khai với CodeDeploy <br>&emsp; + Tạo pipeline end-to-end | 11/11/2025   | 11/11/2025      | <https://000023.awsstudygroup.com/> |
| 4   | - **Workshop:** Amazon EKS - CI/CD với CodePipeline <br>&emsp; + Tạo IAM roles cho EKS <br>&emsp; + Cấu hình aws-auth ConfigMap <br>&emsp; + Thiết lập tích hợp GitHub <br>&emsp; + Triển khai lên EKS cluster        | 12/11/2025   | 12/11/2025      | <https://000152.awsstudygroup.com/> |
| 5   | - **Workshop:** Amazon DynamoDB Immersion Day <br>&emsp; + Hands-on labs cho DynamoDB <br>&emsp; + Advanced design patterns <br>&emsp; + Change Data Capture <br>&emsp; + Xây dựng serverless event-driven apps       | 13/11/2025   | 13/11/2025      | <https://000039.awsstudygroup.com/> |
| 6   | - **Workshop:** Bắt đầu với AWS Step Functions <br>&emsp; + Điều phối workflows <br>&emsp; + Triển khai branching logic <br>&emsp; + Sử dụng parallel execution <br>&emsp; + Xử lý errors và callbacks                | 14/11/2025   | 14/11/2025      | <https://000047.awsstudygroup.com/> |

### Kết quả đạt được tuần 10:

- **Thứ 2 - CI/CD với ECS Container:**

  - Nắm vững tự động hóa CI/CD cho Amazon ECS deployments
  - Thiết lập continuous integration với GitLab
  - Cấu hình GitHub Actions cho container deployments
  - Tích hợp AWS CodeBuild với ECS pipelines
  - Triển khai Container Insights cho monitoring
  - Cấu hình Firelens cho log routing
  - Tự động hóa toàn bộ deployment workflow
  - Giảm lỗi triển khai thủ công
  - Nâng cao hiệu quả workflow với DevOps practices
  - Áp dụng ECS monitoring best practices
  - Đảm bảo ổn định và hiệu suất ứng dụng

- **Thứ 3 - CodePipeline cho EC2:**

  - Xây dựng CI/CD pipeline end-to-end với AWS CodePipeline
  - Cấu hình AWS CodeCommit cho Git-based repositories
  - Thiết lập AWS CodeBuild cho compilation và testing
  - Triển khai ứng dụng Node.js với CodeDeploy
  - Tự động hóa deployments đến EC2 instances
  - Cấu hình CodeDeploy agents trên EC2
  - Sử dụng CloudWatch Events để trigger pipelines
  - Lưu trữ build artifacts trong S3 buckets
  - Mã hóa artifacts với AWS KMS
  - Triển khai automated stage gates
  - Áp dụng continuous delivery best practices

- **Thứ 4 - EKS CI/CD với CodePipeline:**

  - Triển khai CI/CD cho Amazon EKS cluster
  - Tạo IAM roles cho EKS integration
  - Chỉnh sửa aws-auth ConfigMap cho permissions
  - Fork và cấu hình GitHub repository
  - Tạo GitHub access tokens
  - Thiết lập CodePipeline cho Kubernetes deployments
  - Kích hoạt automatic releases trên code commits
  - Triển khai sample services lên EKS
  - Giám sát automated deployments
  - Áp dụng EKS security best practices
  - Tích hợp version control với Kubernetes

- **Thứ 5 - DynamoDB Immersion Day:**

  - Hoàn thành hands-on labs cho Amazon DynamoDB
  - Nắm vững NoSQL data modeling best practices
  - Khám phá advanced DynamoDB design patterns
  - Triển khai Change Data Capture (CDC)
  - Xây dựng serverless event-driven architecture với DynamoDB Streams
  - Tích hợp Generative AI với DynamoDB và OpenSearch
  - Sử dụng Amazon Bedrock cho natural language queries
  - Triển khai global serverless applications
  - Mô hình hóa game player data patterns
  - Làm việc với design challenge scenarios
  - Hiểu single-digit millisecond performance
  - Áp dụng DynamoDB ở quy mô lớn

- **Thứ 6 - AWS Step Functions:**

  - Nắm vững workflow orchestration với AWS Step Functions
  - Tạo state machines cho service coordination
  - Triển khai Task state với Lambda functions
  - Sử dụng Choice state cho branching logic
  - Áp dụng Parallel state cho concurrent execution
  - Triển khai pause/resume với waitForTaskToken
  - Thiết kế error handling strategies
  - Trực quan hóa workflows trong Step Functions console
  - Debug và audit workflow executions
  - Xây dựng tự động hóa workflow fully managed
  - Áp dụng serverless orchestration patterns

- **Kết quả tổng thể tuần 10:**
  - Hoàn thành 5 workshop về CI/CD, Containers, và Serverless
  - Nắm vững CI/CD pipelines cho ECS, EC2, và EKS
  - Triển khai automated deployment workflows
  - Khám phá advanced DynamoDB patterns và use cases
  - Điều phối workflows phức tạp với Step Functions
  - Sẵn sàng xây dựng production-grade DevOps pipelines
