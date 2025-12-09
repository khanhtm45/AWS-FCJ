---
title: "Worklog Tuần 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 1:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                            | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** Tạo tài khoản AWS đầu tiên <br>&emsp; + Tạo tài khoản AWS mới <br>&emsp; + Thiết lập MFA cho root user <br>&emsp; + Tạo Administrator Group và Admin User <br>&emsp; + Cấu hình AWS Management Console               | 08/09/2025   | 08/09/2025      | <https://000001.awsstudygroup.com/> |
| 3   | - **Workshop:** Quản lý chi phí với AWS Budgets <br>&emsp; + Tìm hiểu các loại AWS Budgets <br>&emsp; + Tạo Cost Budget <br>&emsp; + Tạo Usage Budget <br>&emsp; + Tạo Reservation Budget <br>&emsp; + Tạo Savings Plans Budget      | 09/09/2025   | 09/09/2025      | <https://000007.awsstudygroup.com/> |
| 4   | - **Workshop:** Yêu cầu hỗ trợ với AWS Support <br>&emsp; + Tìm hiểu các gói AWS Support <br>&emsp; + Truy cập AWS Support Center <br>&emsp; + Quản lý yêu cầu hỗ trợ và cases                                                       | 10/09/2025   | 10/09/2025      | <https://000009.awsstudygroup.com/> |
| 5   | - **Workshop:** Kiểm soát truy cập với AWS IAM <br>&emsp; + Tạo IAM Users và Groups <br>&emsp; + Cấu hình IAM Policies <br>&emsp; + Tạo và quản lý IAM Roles <br>&emsp; + Thực hành chuyển đổi roles                                 | 11/09/2025   | 11/09/2025      | <https://000002.awsstudygroup.com/> |
| 6   | - **Workshop:** Amazon VPC và Site-to-Site VPN <br>&emsp; + Giới thiệu về Amazon VPC <br>&emsp; + Cấu hình Security Groups và Network ACLs <br>&emsp; + Triển khai EC2 instances <br>&emsp; + Thiết lập kết nối AWS Site-to-Site VPN | 12/09/2025   | 12/09/2025      | <https://000003.awsstudygroup.com/> |

### Kết quả đạt được tuần 1:

- **Thứ 2 - Thiết lập tài khoản AWS:**

  - Tạo thành công tài khoản AWS mới với cấu hình phù hợp
  - Kích hoạt Multi-Factor Authentication (MFA) cho tài khoản root user để tăng cường bảo mật
  - Tạo IAM Group quản trị viên với các policies phù hợp
  - Tạo Admin User và thêm vào Administrator Group
  - Cấu hình AWS Management Console và làm quen với giao diện
  - Học các best practices về bảo mật tài khoản AWS và quản lý root user

- **Thứ 3 - Quản lý chi phí AWS:**

  - Hiểu được tầm quan trọng của AWS Budgets trong việc kiểm soát và giám sát chi phí
  - Tìm hiểu các loại ngân sách khác nhau: Cost, Usage, Reservation, và Savings Plans
  - Tạo thành công Cost Budgets để theo dõi chi tiêu AWS
  - Cấu hình Usage Budgets để giám sát mức tiêu thụ dịch vụ cụ thể
  - Thiết lập Reservation Budgets để theo dõi việc sử dụng Reserved Instances
  - Tạo Savings Plans Budgets để giám sát các cam kết tiết kiệm
  - Cấu hình cảnh báo ngân sách với nhiều ngưỡng (50%, 80%, 90%, 100%)
  - Tìm hiểu về các hành động tự động và biện pháp kiểm soát chi phí

- **Thứ 4 - AWS Support:**

  - Hiểu các gói AWS Support khác nhau: Basic, Developer, Business, và Enterprise
  - Tìm hiểu về thời gian phản hồi và tính năng hỗ trợ của từng gói
  - Truy cập thành công AWS Support Center qua Management Console
  - Tạo và quản lý các support cases
  - Học cách cung cấp thông tin cần thiết cho yêu cầu hỗ trợ hiệu quả
  - Hiểu về vòng đời của support case và quy trình theo dõi

- **Thứ 5 - Kiểm soát truy cập IAM:**

  - Nắm vững các khái niệm cốt lõi của AWS Identity and Access Management (IAM)
  - Tạo thành công IAM Users với các quyền phù hợp
  - Tạo IAM Groups và áp dụng policies để quản lý truy cập có tổ chức
  - Cấu hình IAM Roles cho truy cập tạm thời và các tình huống cross-account
  - Thực hành chuyển đổi giữa các IAM roles với các mức quyền khác nhau
  - Triển khai nguyên tắc least privilege trong kiểm soát truy cập
  - Hiểu sự khác biệt giữa IAM Users, Groups, và Roles
  - Học các best practices và khuyến nghị bảo mật của IAM

- **Thứ 6 - Amazon VPC và Site-to-Site VPN:**

  - Hiểu sâu về Amazon Virtual Private Cloud (VPC)
  - Tìm hiểu các thành phần của VPC: subnets, route tables, internet gateways
  - Cấu hình Security Groups cho bảo mật cấp instance
  - Thiết lập Network ACLs cho bảo mật cấp subnet
  - Triển khai thành công EC2 instances trong môi trường VPC
  - Cấu hình kết nối AWS Site-to-Site VPN để kết nối hybrid an toàn
  - Hiểu về định tuyến VPN và các giao thức mã hóa
  - Tìm hiểu về kiến trúc VPC production-ready với thiết lập multi-AZ
  - Triển khai VPC Flow Logs để giám sát mạng

- **Kết quả tổng thể:**
  - Hoàn thành 5 workshop AWS toàn diện về các dịch vụ nền tảng
  - Có kinh nghiệm thực hành với quản lý tài khoản AWS và bảo mật
  - Phát triển kỹ năng quản lý và giám sát chi phí
  - Nắm vững kiểm soát truy cập IAM và các best practices bảo mật
  - Xây dựng kiến thức thực tế về mạng VPC và kết nối an toàn
  - Sẵn sàng triển khai các giải pháp AWS an toàn và tiết kiệm chi phí
