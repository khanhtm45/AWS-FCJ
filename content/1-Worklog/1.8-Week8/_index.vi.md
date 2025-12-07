---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 8:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                      | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** AWS Web Application Firewall (WAF) <br>&emsp; + Tìm hiểu WAF cơ bản <br>&emsp; + Tạo WAF rules <br>&emsp; + Cấu hình web ACLs <br>&emsp; + Bảo vệ ứng dụng web                                 | 27/10/2025   | 27/10/2025      | <https://000026.awsstudygroup.com/> |
| 3   | - **Workshop:** Mã hóa dữ liệu với AWS KMS <br>&emsp; + Tạo KMS keys <br>&emsp; + Mã hóa S3 objects <br>&emsp; + Cấu hình CloudTrail logging <br>&emsp; + Truy vấn logs với Athena                             | 28/10/2025   | 28/10/2025      | <https://000033.awsstudygroup.com/> |
| 4   | - **Workshop:** AWS Secrets Manager với RDS và Fargate <br>&emsp; + Lưu trữ RDS credentials <br>&emsp; + Cấu hình secret rotation <br>&emsp; + Truy cập secrets từ Fargate <br>&emsp; + Test với shell scripts | 29/10/2025   | 29/10/2025      | <https://000096.awsstudygroup.com/> |
| 5   | - **Workshop:** Triển khai AWS Cognito Across Sites <br>&emsp; + Tạo Cognito User Pools <br>&emsp; + Cấu hình Identity Pools <br>&emsp; + Triển khai authentication <br>&emsp; + Tích hợp cross-site           | 30/10/2025   | 30/10/2025      | <https://000141.awsstudygroup.com/> |
| 6   | - **Workshop:** Tự động Patching với EC2 Image Builder <br>&emsp; + Cấu hình EC2 Image Builder <br>&emsp; + Tạo AMI pipeline <br>&emsp; + Tự động hóa với Systems Manager <br>&emsp; + Blue/green deployment   | 31/10/2025   | 31/10/2025      | <https://000099.awsstudygroup.com/> |

### Kết quả đạt được tuần 8:

- **Thứ 2 - AWS Web Application Firewall:**

  - Nắm vững kiến thức AWS WAF cho bảo vệ ứng dụng web
  - Tạo và cấu hình WAF web ACLs
  - Triển khai WAF rules cho traffic filtering
  - Bảo vệ ứng dụng khỏi các lỗ hổng web phổ biến
  - Cấu hình rate-based rules để ngăn chặn DDoS attacks
  - Sử dụng AWS managed rule groups
  - Tạo custom rule groups cho yêu cầu cụ thể
  - Giám sát WAF metrics và logs
  - Áp dụng WAF best practices cho bảo mật
  - Tích hợp WAF với CloudFront và ALB

- **Thứ 3 - Mã hóa KMS:**

  - Hiểu các khái niệm AWS Key Management Service (KMS)
  - Tạo và quản lý customer master keys (CMKs)
  - Mã hóa S3 objects với KMS keys
  - Cấu hình server-side encryption (SSE-KMS)
  - Thiết lập CloudTrail cho KMS API logging
  - Sử dụng Amazon Athena để truy vấn CloudTrail logs
  - Triển khai key rotation policies
  - Chia sẻ dữ liệu đã mã hóa an toàn giữa các accounts
  - Áp dụng encryption best practices cho data at rest
  - Quản lý key policies và grants
  - Đảm bảo tuân thủ yêu cầu mã hóa

- **Thứ 4 - Tích hợp AWS Secrets Manager:**

  - Nắm vững AWS Secrets Manager cho quản lý credential
  - Lưu trữ RDS database credentials an toàn
  - Cấu hình automatic secret rotation
  - Tích hợp Secrets Manager với Amazon RDS
  - Truy cập secrets từ EC2 instances
  - Lấy secrets từ AWS Fargate containers
  - Triển khai least privilege access với IAM
  - Tạo Docker containers với secret integration
  - Tự động hóa quản lý secret với shell scripts
  - Áp dụng preventative security controls (CSF framework)
  - Xây dựng kiến trúc VPC an toàn với private subnets

- **Thứ 5 - Xác thực AWS Cognito:**

  - Hiểu Amazon Cognito identity platform
  - Tạo và cấu hình Cognito User Pools
  - Thiết lập Cognito Identity Pools cho AWS access
  - Triển khai user authentication cho ứng dụng web/mobile
  - Tích hợp third-party identity providers (IdPs)
  - Cấu hình SAML 2.0 và OIDC authentication
  - Cấp phát authenticated JSON Web Tokens (JWTs)
  - Triển khai cross-site authentication
  - Sử dụng role-based và attribute-based access control
  - Áp dụng OAuth 2.0 authorization flows
  - Xây dựng user directory an toàn với self-service features

- **Thứ 6 - Pipeline Patching Tự động:**

  - Xây dựng giải pháp patching tự động với EC2 Image Builder
  - Tạo AMI builder pipelines
  - Cấu hình Systems Manager Automation documents
  - Triển khai blue/green deployment methodology
  - Sử dụng CloudFormation AutoScalingReplacingUpdate policy
  - Tự động hóa OS patching cho tuân thủ bảo mật
  - Giảm overhead vận hành với automation
  - Đảm bảo interruption tối thiểu cho application availability
  - Thiết lập traceability cho compliance audits
  - Triển khai updated AMIs đến application clusters
  - Áp dụng Well-Architected security best practices

- **Kết quả tổng thể tuần 8:**
  - Hoàn thành 5 workshop về AWS Security và Automation
  - Nắm vững bảo vệ ứng dụng web với WAF
  - Triển khai mã hóa dữ liệu với KMS
  - Bảo mật credentials với Secrets Manager
  - Xây dựng hệ thống authentication với Cognito
  - Tự động hóa patching với EC2 Image Builder
  - Sẵn sàng triển khai các giải pháp bảo mật doanh nghiệp
