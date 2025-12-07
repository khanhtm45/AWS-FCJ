---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 3:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                       | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** Amazon Lightsail - Tối ưu chi phí <br>&emsp; + Triển khai database trên Lightsail <br>&emsp; + Triển khai WordPress, Prestashop, Akaunting <br>&emsp; + Bảo mật ứng dụng & snapshots <br>&emsp; + Tạo alarms và scale instances | 22/09/2025   | 22/09/2025      | <https://000045.awsstudygroup.com/> |
| 3   | - **Workshop:** Amazon Lightsail Container <br>&emsp; + Tìm hiểu về Lightsail Container service <br>&emsp; + Tạo container service <br>&emsp; + Triển khai public Docker images <br>&emsp; + Triển khai custom images                           | 23/09/2025   | 23/09/2025      | <https://000046.awsstudygroup.com/> |
| 4   | - **Workshop:** Auto Scaling Group với Load Balancer <br>&emsp; + Tạo Launch Template <br>&emsp; + Thiết lập Application Load Balancer <br>&emsp; + Cấu hình Auto Scaling Group <br>&emsp; + Test khả năng mở rộng                              | 24/09/2025   | 24/09/2025      | <https://000006.awsstudygroup.com/> |
| 5   | - **Workshop:** Giám sát AWS CloudWatch <br>&emsp; + CloudWatch Metrics <br>&emsp; + CloudWatch Logs <br>&emsp; + CloudWatch Alarms <br>&emsp; + CloudWatch Dashboards                                                                          | 25/09/2025   | 25/09/2025      | <https://000008.awsstudygroup.com/> |
| 6   | - **Workshop:** Hybrid DNS với Route 53 Resolver <br>&emsp; + Thiết lập Route 53 Resolver <br>&emsp; + Triển khai Microsoft AD <br>&emsp; + Cấu hình inbound/outbound endpoints <br>&emsp; + Thiết lập kiến trúc hybrid DNS                     | 26/09/2025   | 26/09/2025      | <https://000010.awsstudygroup.com/> |

### Kết quả đạt được tuần 3:

- **Thứ 2 - Amazon Lightsail:**

  - Nắm vững Amazon Lightsail như một dịch vụ compute đơn giản hóa của AWS
  - Triển khai thành công Lightsail managed database
  - Triển khai ứng dụng WordPress blog/website trên Lightsail
  - Triển khai nền tảng e-commerce Prestashop
  - Triển khai ứng dụng tài chính Akaunting
  - Triển khai các best practices bảo mật ứng dụng
  - Tạo snapshots để backup và disaster recovery
  - Mở rộng instances lên kích thước lớn hơn cho tăng trưởng doanh nghiệp
  - Cấu hình CloudWatch alarms cho giám sát chủ động
  - Hiểu các chiến lược tối ưu chi phí của Lightsail
  - Hoàn thành trong giới hạn free tier (720 giờ)

- **Thứ 3 - Lightsail Container:**

  - Hiểu khả năng của Lightsail Container service
  - Học lợi ích của containerization và Docker fundamentals
  - Tạo Lightsail Container service
  - Triển khai public Docker images từ DockerHub
  - Xây dựng và triển khai custom Docker images
  - Cấu hình scaling và capacity của container service
  - Hiểu về container networking và load balancing
  - Quản lý containerized applications với giao diện đơn giản
  - Học khi nào nên dùng Lightsail Container so với EC2/ECS

- **Thứ 4 - Auto Scaling Group:**

  - Nắm vững kiến trúc EC2 Auto Scaling Group
  - Tạo Launch Templates cho cấu hình instance
  - Cấu hình Application Load Balancer cho phân phối traffic
  - Thiết lập Target Groups và health checks
  - Tạo Auto Scaling Group với scaling policies
  - Triển khai dynamic scaling dựa trên workload
  - Test fault tolerance và high availability
  - Hiểu về scaling metrics và thresholds
  - Áp dụng nguyên tắc AWS Well-Architected Framework
  - Tối ưu chi phí với điều chỉnh capacity tự động

- **Thứ 5 - AWS CloudWatch:**

  - Hiểu toàn diện về CloudWatch monitoring
  - Làm việc với CloudWatch Metrics để theo dõi hiệu suất
  - Cấu hình CloudWatch Logs cho centralized logging
  - Tạo CloudWatch Alarms cho cảnh báo tự động
  - Xây dựng CloudWatch Dashboards cho visualization
  - Hiểu về metric granularity (độ phân giải 1 giây)
  - Tìm hiểu về metric retention (lưu trữ 15 tháng)
  - Triển khai Container Insights cho containerized apps
  - Cấu hình automated actions dựa trên alarms
  - Áp dụng best practices cho observability và monitoring
  - Giảm MTTR (Mean Time To Resolution) với cảnh báo chủ động

- **Thứ 6 - Route 53 Hybrid DNS:**

  - Hiểu khả năng của Route 53 DNS service
  - Tìm hiểu về kiến trúc Route 53 Resolver
  - Cấu hình inbound endpoints cho truy vấn từ on-premise
  - Thiết lập outbound endpoints cho phân giải từ AWS ra on-premise
  - Tạo Route 53 Resolver Rules cho domain forwarding
  - Triển khai Microsoft Active Directory trên AWS
  - Kết nối đến RDGW (Remote Desktop Gateway)
  - Triển khai kiến trúc hybrid DNS
  - Tích hợp on-premise DNS với AWS Route 53
  - Hiểu luồng DNS query trong môi trường hybrid
  - Áp dụng best practices cho hybrid cloud connectivity

- **Kết quả tổng thể:**
  - Hoàn thành 5 workshop AWS nâng cao về scalability và monitoring
  - Nắm vững compute tối ưu chi phí với Lightsail
  - Phát triển kỹ năng containerization với Lightsail Container
  - Xây dựng kiến trúc highly available với Auto Scaling và Load Balancing
  - Triển khai giám sát toàn diện với CloudWatch
  - Cấu hình hybrid cloud DNS với Route 53 Resolver
  - Sẵn sàng thiết kế và triển khai các giải pháp AWS production-grade
