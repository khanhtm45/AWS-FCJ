---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 4:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** Bắt đầu với AWS CLI <br>&emsp; + Cài đặt và cấu hình AWS CLI <br>&emsp; + Làm việc với S3, SNS, IAM qua CLI <br>&emsp; + Quản lý VPC và EC2 thông qua CLI <br>&emsp; + Khắc phục sự cố CLI                               | 29/09/2025   | 29/09/2025      | <https://000011.awsstudygroup.com/> |
| 3   | - **Workshop:** Làm việc với Amazon DynamoDB <br>&emsp; + Tìm hiểu các khái niệm cơ bản DynamoDB <br>&emsp; + Thực hành Python với DynamoDB <br>&emsp; + Sử dụng AWS SDK cho CRUD operations <br>&emsp; + Làm việc với tables và indexes | 30/09/2025   | 30/09/2025      | <https://000060.awsstudygroup.com/> |
| 4   | - **Workshop:** Amazon ElastiCache - Redis <br>&emsp; + Tìm hiểu cơ bản về ElastiCache Redis <br>&emsp; + Tạo ElastiCache cluster <br>&emsp; + Sử dụng AWS SDK để đọc/ghi dữ liệu <br>&emsp; + Tối ưu hiệu suất cache                    | 01/10/2025   | 01/10/2025      | <https://000061.awsstudygroup.com/> |
| 5   | - **Workshop:** AWS Networking và Content Delivery <br>&emsp; + Tìm hiểu sâu các thành phần VPC <br>&emsp; + Transit Gateway và Site-to-Site VPN <br>&emsp; + VPC Endpoints và Peering <br>&emsp; + Cấu hình Route53 DNS                 | 02/10/2025   | 02/10/2025      | <https://000092.awsstudygroup.com/> |
| 6   | - **Workshop:** CloudFront với S3 Bucket Origin <br>&emsp; + Tạo S3 bucket cho static hosting <br>&emsp; + Cấu hình CloudFront distribution <br>&emsp; + Tăng tốc phân phối nội dung <br>&emsp; + Bảo mật với OAI                        | 03/10/2025   | 03/10/2025      | <https://000094.awsstudygroup.com/> |

### Kết quả đạt được tuần 4:

- **Thứ 2 - AWS CLI:**

  - Nắm vững AWS Command Line Interface cho quản lý cloud hiệu quả
  - Cài đặt thành công AWS CLI trên Windows, Linux, và macOS
  - Cấu hình AWS CLI với profiles cho nhiều môi trường
  - Học cấu hình CLI: Access Keys, Secret Keys, regions, output formats
  - Quản lý S3 buckets và objects sử dụng CLI commands
  - Tạo và cấu hình SNS topics và subscriptions qua CLI
  - Thực hiện các thao tác IAM: users, groups, roles, policies
  - Quản lý VPC resources: subnets, route tables, security groups
  - Tạo và cấu hình EC2 instances thông qua CLI
  - Tự động hóa các tác vụ AWS với CLI scripts
  - Khắc phục các vấn đề và lỗi CLI thường gặp
  - Hiểu các định dạng output: JSON, YAML, text, table

- **Thứ 3 - Amazon DynamoDB:**

  - Hiểu toàn diện về DynamoDB NoSQL database
  - Học các khái niệm cốt lõi: tables, items, attributes
  - Hiểu partition keys và sort keys
  - Nắm vững DynamoDB data types và naming rules
  - Thực hành lập trình Python với AWS SDK (Boto3)
  - Triển khai CRUD operations trên DynamoDB tables
  - Tạo và query DynamoDB indexes (GSI, LSI)
  - Tối ưu hiệu suất và throughput của DynamoDB
  - Hiểu các mô hình pricing của DynamoDB
  - Áp dụng best practices cho NoSQL data modeling

- **Thứ 4 - Amazon ElastiCache Redis:**

  - Hiểu ElastiCache như managed in-memory data store
  - Học Redis fundamentals và use cases
  - Tạo ElastiCache Redis cluster
  - Cấu hình cluster parameters và node types
  - Kết nối ứng dụng đến ElastiCache endpoint
  - Sử dụng AWS SDK để ghi và đọc dữ liệu từ Redis
  - Triển khai caching strategies cho hiệu suất
  - Hiểu Redis data structures (strings, lists, sets, hashes)
  - Cấu hình security groups cho ElastiCache access
  - Giám sát ElastiCache performance metrics
  - Áp dụng caching best practices cho scalability

- **Thứ 5 - AWS Networking và Content Delivery:**

  - Nắm vững kiến trúc AWS networking toàn diện
  - Tìm hiểu sâu VPC components: subnets, route tables, IGW, NAT Gateway
  - Hiểu về Availability Zones và Regions
  - Cấu hình Elastic Network Interfaces (ENI) và Elastic IPs
  - Triển khai VPC Endpoints cho private AWS service access
  - Cấu hình Security Groups và Network ACLs
  - Thiết lập Transit Gateway cho centralized connectivity
  - Cấu hình Site-to-Site VPN connections
  - Triển khai VPC Peering cho multi-VPC communication
  - Cấu hình Route53 DNS endpoints và hosted zones
  - Thiết lập VPC Endpoint Services cho private connectivity
  - Quản lý Transit Gateway Network Manager
  - Hiểu kiến trúc AWS Direct Connect
  - Cấu hình Network Load Balancer (Layer 4)

- **Thứ 6 - CloudFront với S3:**

  - Hiểu Amazon CloudFront CDN service
  - Tạo S3 bucket cho static website hosting
  - Upload static content (HTML, CSS, JS) lên S3
  - Cấu hình CloudFront distribution với S3 origin
  - Triển khai Origin Access Identity (OAI) cho bảo mật
  - Cấu hình CloudFront cache behaviors
  - Thiết lập custom domain với Route53
  - Kích hoạt HTTPS với SSL/TLS certificates
  - Tối ưu content delivery với edge locations
  - Hiểu mô hình pricing của CloudFront
  - Giám sát CloudFront performance và metrics
  - Áp dụng best practices cho global content delivery

- **Kết quả tổng thể:**
  - Hoàn thành 5 workshop AWS nâng cao về CLI, databases, và networking
  - Nắm vững AWS CLI cho tự động hóa hạ tầng
  - Phát triển kỹ năng với NoSQL (DynamoDB) và caching (Redis)
  - Xây dựng chuyên môn về các khái niệm networking nâng cao của AWS
  - Triển khai global content delivery với CloudFront CDN
  - Sẵn sàng thiết kế các giải pháp AWS phức tạp, phân tán
