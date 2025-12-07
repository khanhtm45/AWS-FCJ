---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 5:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** VM Import/Export <br>&emsp; + Thiết lập môi trường VMware Workstation <br>&emsp; + Import VM images vào Amazon EC2 <br>&emsp; + Export EC2 instances về on-premises <br>&emsp; + Quản lý vòng đời VM migration                                                | 06/10/2025   | 06/10/2025      | <https://000014.awsstudygroup.com/> |
| 3   | - **Workshop:** Database Schema Conversion & Migration <br>&emsp; + Sử dụng AWS Schema Conversion Tool (SCT) <br>&emsp; + Cấu hình AWS Database Migration Service (DMS) <br>&emsp; + Thực hiện heterogeneous database migration <br>&emsp; + Giám sát và khắc phục migrations | 07/10/2025   | 07/10/2025      | <https://000043.awsstudygroup.com/> |
| 4   | - **Workshop:** AWS Elastic Disaster Recovery <br>&emsp; + Cấu hình DRS settings và IAM <br>&emsp; + Cài đặt DRS agent trên source servers <br>&emsp; + Cấu hình EC2 Launch Templates <br>&emsp; + Thực hiện failover testing                                                 | 08/10/2025   | 08/10/2025      | <https://000100.awsstudygroup.com/> |
| 5   | - **Workshop:** Tối ưu chi phí EC2 với Lambda <br>&emsp; + Tạo instance tags cho tự động hóa <br>&emsp; + Cấu hình IAM roles cho Lambda <br>&emsp; + Tạo Lambda functions cho auto start/stop <br>&emsp; + Lập lịch với EventBridge                                           | 09/10/2025   | 09/10/2025      | <https://000022.awsstudygroup.com/> |
| 6   | - **Workshop:** Bắt đầu với Grafana <br>&emsp; + Cài đặt Grafana trên Linux EC2 <br>&emsp; + Cấu hình data sources <br>&emsp; + Tạo monitoring dashboards <br>&emsp; + Trực quan hóa CloudWatch metrics                                                                       | 10/10/2025   | 10/10/2025      | <https://000029.awsstudygroup.com/> |

### Kết quả đạt được tuần 5:

- **Thứ 2 - VM Import/Export:**

  - Nắm vững VM Import/Export cho hybrid cloud migrations
  - Thiết lập môi trường VMware Workstation virtualization
  - Học cách export VM images từ on-premises
  - Import virtual machine images vào Amazon EC2
  - Cấu hình các thiết lập và parameters cho VM conversion
  - Upload VM images lên S3 cho quá trình import
  - Export EC2 instances về định dạng on-premises
  - Hiểu yêu cầu tương thích của VM
  - Quản lý vòng đời VM migration và dependencies
  - Áp dụng best practices cho VM migrations
  - Kích hoạt các kịch bản disaster recovery và backup

- **Thứ 3 - Database Migration:**

  - Có chuyên môn về AWS Database Migration Service (DMS)
  - Nắm vững AWS Schema Conversion Tool (SCT)
  - Thực hiện heterogeneous database migrations
  - Chuyển đổi database schemas giữa các engines khác nhau
  - Cấu hình DMS source và target endpoints
  - Thiết lập serverless DMS replication
  - Triển khai continuous data replication
  - Giám sát migration tasks và metrics
  - Khắc phục các vấn đề migration thường gặp
  - Giảm thiểu downtime trong production migrations
  - Migration từ on-premises sang RDS/Aurora
  - Chuyển đổi stored procedures và functions

- **Thứ 4 - AWS Elastic Disaster Recovery:**

  - Hiểu dịch vụ AWS Elastic Disaster Recovery (DRS)
  - Cấu hình DRS settings và replication
  - Tạo DRS IAM users và roles
  - Cài đặt DRS agent trên source servers (Windows/Linux)
  - Cấu hình continuous block-level replication
  - Thiết lập EC2 Launch Templates cho recovery
  - Thực hiện drill và recovery failover operations
  - Test recovery point objectives (RPO) và recovery time objectives (RTO)
  - Giám sát replication lag và health
  - Triển khai point-in-time recovery
  - Giảm thiểu downtime và mất dữ liệu
  - Áp dụng DR best practices cho business continuity

- **Thứ 5 - Lambda Cost Optimization:**

  - Triển khai tối ưu chi phí EC2 với Lambda
  - Tạo chiến lược instance tagging cho tự động hóa
  - Cấu hình IAM roles với quyền phù hợp cho Lambda
  - Phát triển Lambda functions cho EC2 start/stop automation
  - Lập lịch thực thi Lambda với EventBridge (CloudWatch Events)
  - Lọc instances theo tags cho selective automation
  - Triển khai time-based instance scheduling
  - Tính toán tiết kiệm chi phí từ automated schedules
  - Tìm hiểu về Savings Plans cho 24/7 instances
  - Áp dụng các chiến lược tối ưu chi phí
  - Giám sát Lambda execution và errors
  - Giảm chi phí EC2 runtime không cần thiết

- **Thứ 6 - Grafana Monitoring:**

  - Cài đặt và cấu hình Grafana trên Linux EC2
  - Thiết lập Grafana service và security
  - Tích hợp Grafana với CloudWatch data source
  - Tạo custom monitoring dashboards
  - Trực quan hóa AWS metrics và logs
  - Cấu hình dashboard panels và queries
  - Thiết lập alerts và notifications
  - Giám sát EC2, RDS, và các AWS resources khác
  - Tạo time-series visualizations
  - Triển khai real-time monitoring
  - Áp dụng dashboard best practices
  - Nâng cao observability với Grafana

- **Kết quả tổng thể:**
  - Hoàn thành 5 workshop nâng cao về migration, DR, và optimization
  - Nắm vững VM và database migration sang AWS
  - Triển khai disaster recovery với AWS DRS
  - Tự động hóa tối ưu chi phí với Lambda
  - Xây dựng giám sát toàn diện với Grafana
  - Sẵn sàng thiết kế các kiến trúc cloud resilient, cost-effective
