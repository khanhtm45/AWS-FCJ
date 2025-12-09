---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 9:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** Triển khai AWS Backup cho Hệ thống <br>&emsp; + Tạo backup plans <br>&emsp; + Tự động hóa backups cho EBS, RDS, DynamoDB <br>&emsp; + Test restore operations <br>&emsp; + Cấu hình SNS notifications      | 03/11/2025   | 03/11/2025      | <https://000013.awsstudygroup.com/> |
| 3   | - **Workshop:** Thiết lập VPC Peering <br>&emsp; + Tạo VPC Peering connections <br>&emsp; + Cấu hình Network ACLs <br>&emsp; + Cập nhật route tables <br>&emsp; + Bật cross-peer DNS                                       | 04/11/2025   | 04/11/2025      | <https://000019.awsstudygroup.com/> |
| 4   | - **Workshop:** Thiết lập AWS Transit Gateway <br>&emsp; + Tạo Transit Gateway <br>&emsp; + Cấu hình TGW attachments <br>&emsp; + Thiết lập TGW route tables <br>&emsp; + Kết nối nhiều VPCs                               | 05/11/2025   | 05/11/2025      | <https://000020.awsstudygroup.com/> |
| 5   | - **Workshop:** Kiến trúc Event-Driven với SNS và SQS <br>&emsp; + Tạo SNS topics <br>&emsp; + Cấu hình SQS queues <br>&emsp; + Triển khai message filtering <br>&emsp; + Xây dựng pub/sub patterns                        | 06/11/2025   | 06/11/2025      | <https://000077.awsstudygroup.com/> |
| 6   | - **Workshop:** Chia sẻ Dữ liệu An toàn với EBS NVMe Reservation <br>&emsp; + Cấu hình EBS Multi-Attach <br>&emsp; + Triển khai NVMe reservations <br>&emsp; + Thiết lập PostgreSQL backup <br>&emsp; + Test data recovery | 07/11/2025   | 07/11/2025      | <https://100000.awsstudygroup.com/> |

### Kết quả đạt được tuần 9:

- **Thứ 2 - Triển khai AWS Backup:**

  - Nắm vững AWS Backup cho bảo vệ dữ liệu tập trung
  - Tạo backup plans tự động cho AWS resources
  - Cấu hình backups cho EBS Volumes, RDS Databases, DynamoDB Tables
  - Thiết lập backup cho EFS File Systems
  - Test các thao tác backup và restore
  - Cấu hình AWS SNS cho backup notifications
  - Triển khai backup policies từ một vị trí duy nhất
  - Tự động hóa quy trình bảo vệ dữ liệu
  - Đảm bảo khả năng khôi phục dữ liệu
  - Áp dụng backup best practices cho tính liên tục kinh doanh
  - Xác thực backups thông qua restore testing

- **Thứ 3 - VPC Peering:**

  - Hiểu các khái niệm và kiến trúc VPC Peering
  - Tạo VPC Peering connections giữa các VPCs
  - Cấu hình Network ACLs cho stateless filtering
  - Cập nhật route tables cho peering communication
  - Bật cross-peering DNS cho name resolution
  - Triển khai security groups và NACLs kết hợp
  - Sử dụng private IPv4/IPv6 addresses cho routing
  - Nâng cao bảo mật bằng cách tránh public internet
  - Giảm latency với direct VPC connections
  - Áp dụng chiến lược bảo mật defense-in-depth
  - Hiểu giới hạn non-transitive peering

- **Thứ 4 - AWS Transit Gateway:**

  - Nắm vững AWS Transit Gateway cho mạng lưới scalable
  - Tạo Transit Gateway làm cloud router hub
  - Cấu hình Transit Gateway Attachments cho VPCs
  - Thiết lập Transit Gateway Route Tables
  - Kết nối nhiều VPCs thông qua single gateway
  - Đơn giản hóa kiến trúc mạng so với VPC Peering
  - Triển khai quản lý mạng tập trung
  - Giảm độ phức tạp vận hành
  - Hiểu sự đánh đổi giữa TGW và VPC Peering
  - Áp dụng transit gateway cho enterprise networking
  - Cấu hình encryption in transit

- **Thứ 5 - Kiến trúc Event-Driven:**

  - Xây dựng kiến trúc event-driven với SNS và SQS
  - Tạo Amazon SNS topics cho pub/sub messaging
  - Cấu hình Amazon SQS queues cho message processing
  - Triển khai message filtering với filter policies
  - Thiết kế simple pub/sub patterns
  - Áp dụng kỹ thuật advanced message filtering
  - Sử dụng JSON attributes cho message differentiation
  - Offload message routing logic khỏi publishers
  - Tạo điều kiện cho development teams hoạt động độc lập
  - Cải thiện application scalability với events
  - Xây dựng kiến trúc microservices decoupled

- **Thứ 6 - EBS NVMe Reservation:**

  - Triển khai chia sẻ dữ liệu an toàn với EBS NVMe reservations
  - Cấu hình EBS Multi-Attach cho io2 volumes
  - Sử dụng NVMe reservations cho storage fencing
  - Duy trì data consistency across instances
  - Thiết lập PostgreSQL trên nhiều EC2 instances
  - Triển khai database backup configurations
  - Test data recovery across VPCs
  - Áp dụng industry-standard storage fencing protocols
  - Phối hợp access control cho shared volumes
  - Làm việc với SUSE Linux, RHEL, và Amazon Linux 2
  - Nâng cao bảo mật với separate VPCs
  - Tối ưu hiệu suất với quản lý dữ liệu hiệu quả

- **Kết quả tổng thể tuần 9:**
  - Hoàn thành 5 workshop về Networking, Backup, và Event-Driven Architecture
  - Nắm vững bảo vệ dữ liệu với AWS Backup
  - Xây dựng kiến trúc mạng scalable với VPC Peering và Transit Gateway
  - Triển khai hệ thống event-driven với SNS/SQS
  - Bảo mật chia sẻ dữ liệu với EBS NVMe reservations
  - Sẵn sàng thiết kế kiến trúc cloud cấp doanh nghiệp
