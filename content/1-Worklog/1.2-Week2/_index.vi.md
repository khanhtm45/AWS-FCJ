---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 2:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** Giới thiệu về Amazon EC2 <br>&emsp; + Khởi chạy Windows và Linux instances <br>&emsp; + Tìm hiểu các khái niệm cơ bản của EC2 <br>&emsp; + Triển khai ứng dụng AWS User Management <br>&emsp; + Quản lý chi phí và sử dụng | 15/09/2025   | 15/09/2025      | <https://000004.awsstudygroup.com/> |
| 3   | - **Workshop:** IAM Role để cấp quyền cho ứng dụng <br>&emsp; + Cấp quyền truy cập AWS services cho ứng dụng <br>&emsp; + Tìm hiểu tại sao không nên dùng access keys <br>&emsp; + Cấu hình IAM Role trên EC2                              | 16/09/2025   | 16/09/2025      | <https://000048.awsstudygroup.com/> |
| 4   | - **Workshop:** Bắt đầu với AWS Cloud9 <br>&emsp; + Tạo Cloud9 IDE instance <br>&emsp; + Học các thao tác cơ bản của Cloud9 <br>&emsp; + Sử dụng AWS CLI trong môi trường Cloud9                                                           | 17/09/2025   | 17/09/2025      | <https://000049.awsstudygroup.com/> |
| 5   | - **Workshop:** Bắt đầu với Amazon S3 <br>&emsp; + Kích hoạt static website hosting <br>&emsp; + Cấu hình public access và objects <br>&emsp; + Tăng tốc với CloudFront <br>&emsp; + Bucket versioning và replication                      | 18/09/2025   | 18/09/2025      | <https://000057.awsstudygroup.com/> |
| 6   | - **Workshop:** Amazon RDS (Relational Database Service) <br>&emsp; + Tạo RDS database instance <br>&emsp; + Kết nối EC2 với RDS <br>&emsp; + Triển khai ứng dụng với database <br>&emsp; + Sao lưu và khôi phục                           | 19/09/2025   | 19/09/2025      | <https://000005.awsstudygroup.com/> |

### Kết quả đạt được tuần 2:

- **Thứ 2 - Amazon EC2:**

  - Khởi chạy thành công Windows Server 2022 và Amazon Linux 2023 instances
  - Nắm vững các khái niệm cơ bản của EC2: instance types, AMIs, EBS volumes
  - Kết nối đến instances qua RDP (Windows) và SSH (Linux)
  - Triển khai ứng dụng AWS User Management Node.js trên cả hai nền tảng
  - Triển khai quản lý chi phí với IAM policies
  - Tìm hiểu về EC2 security groups và cấu hình mạng
  - Hiểu các mô hình giá và chiến lược tối ưu chi phí EC2
  - Hoàn thành dọn dẹp tài nguyên để tránh phát sinh chi phí

- **Thứ 3 - IAM Role cho ứng dụng:**

  - Hiểu rủi ro bảo mật khi sử dụng access keys và secret keys
  - Học các best practices để cấp quyền truy cập AWS services cho ứng dụng
  - Cấu hình thành công IAM Roles cho EC2 instances
  - Triển khai cấp quyền ứng dụng an toàn không cần hardcode credentials
  - So sánh phương pháp access key với phương pháp IAM Role
  - Hiểu về nguyên tắc temporary security credentials
  - Áp dụng least privilege access cho quyền ứng dụng

- **Thứ 4 - AWS Cloud9:**

  - Tạo và cấu hình môi trường Cloud9 IDE
  - Làm quen với giao diện phát triển web-based của Cloud9
  - Học các tính năng và thao tác cơ bản của Cloud9
  - Cấu hình preferences và themes của code editor
  - Sử dụng AWS CLI trong terminal của Cloud9
  - Hiểu về tích hợp Cloud9 với các dịch vụ AWS
  - Thực hành coding và debugging trong môi trường cloud
  - Học khi nào nên sử dụng Cloud9 cho phát triển AWS

- **Thứ 5 - Amazon S3:**

  - Hiểu sâu về Amazon S3 object storage
  - Tạo S3 buckets và upload objects
  - Kích hoạt và cấu hình static website hosting trên S3
  - Quản lý cài đặt public access và bucket policies
  - Cấu hình public objects với quyền phù hợp
  - Tăng tốc phân phối website sử dụng CloudFront CDN
  - Triển khai bucket versioning để bảo vệ dữ liệu
  - Cấu hình S3 Cross-Region Replication (CRR)
  - Tìm hiểu các storage classes và lifecycle policies của S3
  - Hiểu các best practices và cân nhắc bảo mật của S3

- **Thứ 6 - Amazon RDS:**

  - Nắm vững các khái niệm cốt lõi của Amazon RDS và database engines được hỗ trợ
  - Hiểu các tùy chọn storage của RDS (General Purpose, Provisioned IOPS)
  - Tạo RDS database instance với cấu hình phù hợp
  - Cấu hình VPC security groups cho truy cập database
  - Kết nối ứng dụng EC2 với RDS database
  - Triển khai web application với RDS backend
  - Triển khai automated backups và point-in-time recovery
  - Tìm hiểu về Multi-AZ deployments cho high availability
  - Hiểu về Read Replicas cho read scaling
  - Thực hành các thao tác backup và restore
  - Áp dụng các best practices bảo mật RDS (encryption, IAM authentication)

- **Kết quả tổng thể:**
  - Hoàn thành 5 workshop AWS toàn diện về các dịch vụ cốt lõi
  - Có kinh nghiệm thực hành với compute, storage, và database services
  - Nắm vững các mẫu triển khai ứng dụng an toàn
  - Phát triển kỹ năng thực tế với EC2, IAM, Cloud9, S3, và RDS
  - Xây dựng ứng dụng end-to-end sử dụng các dịch vụ AWS managed services
  - Sẵn sàng thiết kế và triển khai các kiến trúc AWS có khả năng mở rộng
