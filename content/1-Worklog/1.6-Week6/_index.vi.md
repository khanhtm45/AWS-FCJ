---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 6:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** AWS CloudWatch Deep Dive <br>&emsp; + Cấu hình CloudWatch Metrics <br>&emsp; + Thiết lập CloudWatch Logs <br>&emsp; + Tạo CloudWatch Alarms <br>&emsp; + Xây dựng CloudWatch Dashboards                                     | 13/10/2025   | 13/10/2025      | <https://000036.awsstudygroup.com/> |
| 3   | - **Workshop:** Quản lý tài nguyên với Tags và Resource Groups <br>&emsp; + Áp dụng tags cho AWS resources <br>&emsp; + Tạo tag-based queries <br>&emsp; + Xây dựng Resource Groups <br>&emsp; + Tự động hóa tasks trên resource groups     | 14/10/2025   | 14/10/2025      | <https://000027.awsstudygroup.com/> |
| 4   | - **Workshop:** Quản lý truy cập EC2 với Resource Tags qua IAM <br>&emsp; + Triển khai least privilege principle <br>&emsp; + Tạo IAM policies với conditions <br>&emsp; + Cấu hình tag-based access control <br>&emsp; + Xác minh policies | 15/10/2025   | 15/10/2025      | <https://000028.awsstudygroup.com/> |
| 5   | - **Workshop:** AWS Systems Manager - Patch Manager & Run Command <br>&emsp; + Cấu hình Patch Manager <br>&emsp; + Tạo maintenance windows <br>&emsp; + Thực thi Run Command <br>&emsp; + Tự động hóa patching                              | 16/10/2025   | 16/10/2025      | <https://000031.awsstudygroup.com/> |
| 6   | - **Workshop:** AWS Systems Manager - Session Manager <br>&emsp; + Kết nối instances không cần SSH <br>&emsp; + Cấu hình session logging đến S3 <br>&emsp; + Triển khai port forwarding <br>&emsp; + Bảo mật remote access                  | 17/10/2025   | 17/10/2025      | <https://000058.awsstudygroup.com/> |

### Kết quả đạt được tuần 6:

- **Thứ 2 - CloudWatch Deep Dive:**

  - Nắm vững CloudWatch monitoring và observability toàn diện
  - Cấu hình CloudWatch Metrics cho theo dõi hiệu suất
  - Thu thập custom metrics từ applications
  - Thiết lập CloudWatch Logs cho centralized log management
  - Tạo log groups và log streams
  - Cấu hình CloudWatch Alarms với nhiều ngưỡng
  - Thiết lập alarm actions với SNS notifications
  - Xây dựng CloudWatch Dashboards toàn diện
  - Trực quan hóa metrics với graphs và widgets
  - Giám sát containerized applications với Container Insights
  - Hiểu metric retention (15 tháng)
  - Áp dụng monitoring best practices cho production systems

- **Thứ 3 - Resource Tags và Groups:**

  - Nắm vững chiến lược AWS resource tagging
  - Áp dụng tags cho EC2, S3, và các AWS resources khác
  - Tạo tagging taxonomy nhất quán (purpose, owner, environment)
  - Xây dựng tag-based queries cho resource discovery
  - Tạo AWS Resource Groups cho logical organization
  - Tự động hóa tasks trên resource groups
  - Quản lý resources ở quy mô lớn với tags
  - Triển khai cost allocation tags
  - Sử dụng CloudFormation stack-based queries
  - Áp dụng resource organization best practices
  - Đơn giản hóa quản lý multi-resource

- **Thứ 4 - IAM với Resource Tags:**

  - Triển khai IAM least privilege principle
  - Tạo IAM policies với conditional statements
  - Cấu hình tag-based access control (TBAC)
  - Tạo IAM roles cho EC2 administrators
  - Định nghĩa policies với tag conditions
  - Hạn chế resource creation dựa trên tags
  - Cấu hình MFA cho IAM users
  - Triển khai assume role functionality
  - Xác minh policy effectiveness với testing
  - Áp dụng decentralized administration model
  - Nâng cao bảo mật với attribute-based access control

- **Thứ 5 - Systems Manager Patch & Run Command:**

  - Nắm vững khả năng AWS Systems Manager
  - Cấu hình Patch Manager cho automated patching
  - Tạo patch baselines cho OS updates
  - Thiết lập maintenance windows cho patching schedules
  - Thực thi Run Command trên nhiều instances
  - Tự động hóa tasks không cần SSH/RDP access
  - Tạo resource groups cho Systems Manager
  - Giám sát patch compliance status
  - Tập trung operational data từ multiple services
  - Tự động hóa các tác vụ quản trị lặp lại
  - Áp dụng patch management best practices

- **Thứ 6 - Session Manager:**

  - Hiểu AWS Systems Manager Session Manager
  - Kết nối đến EC2 instances không cần SSH keys hoặc bastion hosts
  - Cấu hình IAM roles cho Session Manager access
  - Thiết lập session logging đến S3 buckets
  - Kích hoạt session audit trails với CloudWatch Logs
  - Triển khai port forwarding cho secure tunneling
  - Kết nối đến private instances không cần public IPs
  - Quản lý sessions qua browser-based shell
  - Nâng cao bảo mật bằng cách loại bỏ inbound ports
  - Tập trung access control với IAM policies
  - Áp dụng secure remote access best practices

- **Kết quả tổng thể:**
  - Hoàn thành 5 workshop về monitoring, governance, và automation
  - Nắm vững CloudWatch cho comprehensive observability
  - Triển khai resource organization với tags và groups
  - Bảo mật access với tag-based IAM policies
  - Tự động hóa operations với Systems Manager
  - Thiết lập secure remote access với Session Manager
  - Sẵn sàng triển khai enterprise-grade AWS governance
