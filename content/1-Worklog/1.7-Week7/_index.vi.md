---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 7:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** AWS CloudFormation <br>&emsp; + Tìm hiểu IaC với CloudFormation <br>&emsp; + Tạo CloudFormation templates <br>&emsp; + Triển khai stacks với YAML/JSON <br>&emsp; + Sử dụng Cloud9 IDE                 | 22/09/2025   | 22/09/2025      | <https://000037.awsstudygroup.com/> |
| 3   | - **Workshop:** CDK Cơ bản <br>&emsp; + Hiểu khái niệm AWS CDK <br>&emsp; + Triển khai infrastructure bằng code <br>&emsp; + Cấu hình EC2 với user data <br>&emsp; + Sử dụng TypeScript/Python cho IaC                 | 23/09/2025   | 23/09/2025      | <https://000038.awsstudygroup.com/> |
| 4   | - **Workshop:** CDK Cơ bản 2 (Nâng cao) <br>&emsp; + Xây dựng kiến trúc API Gateway <br>&emsp; + Triển khai ECS và ALB <br>&emsp; + Tạo Lambda functions <br>&emsp; + Triển khai nested stacks                         | 24/09/2025   | 24/09/2025      | <https://000076.awsstudygroup.com/> |
| 5   | - **Workshop:** Giới thiệu Infrastructure as Code <br>&emsp; + So sánh các IaC frameworks <br>&emsp; + Tạo Lambda functions <br>&emsp; + Xây dựng VPC và EC2 <br>&emsp; + Triển khai kiến trúc three-tier              | 25/09/2025   | 25/09/2025      | <https://000102.awsstudygroup.com/> |
| 6   | - **Workshop:** Tối ưu kích thước EC2 với CloudWatch <br>&emsp; + Cấu hình CloudWatch Agent <br>&emsp; + Thu thập memory metrics <br>&emsp; + Sử dụng AWS Compute Optimizer <br>&emsp; + Áp dụng sizing best practices | 26/09/2025   | 26/09/2025      | <https://000032.awsstudygroup.com/> |

### Kết quả đạt được tuần 7:

- **Thứ 2 - AWS CloudFormation:**

  - Nắm vững khái niệm Infrastructure as Code (IaC) với CloudFormation
  - Tạo CloudFormation templates ở định dạng YAML và JSON
  - Triển khai và quản lý infrastructure thông qua stacks
  - Sử dụng AWS Cloud9 làm web-based IDE cho phát triển
  - Tự động hóa việc provisioning và quản lý resources
  - Triển khai các tính năng CloudFormation cơ bản
  - Khám phá khả năng nâng cao của CloudFormation
  - Hiểu vòng đời quản lý CloudFormation stack
  - Áp dụng IaC best practices cho triển khai infrastructure
  - Học cách version control infrastructure code

- **Thứ 3 - CDK Cơ bản:**

  - Hiểu các khái niệm nền tảng AWS Cloud Development Kit (CDK)
  - Triển khai infrastructure sử dụng ngôn ngữ lập trình
  - Sử dụng TypeScript/JavaScript cho phát triển CDK
  - Tạo CDK templates với các cấu trúc lập trình quen thuộc
  - Cấu hình EC2 instances thông qua user data
  - Cập nhật và chỉnh sửa CDK templates
  - Hiểu quá trình biên dịch CDK sang CloudFormation
  - Tận dụng CDK constructs cho phát triển nhanh hơn
  - Áp dụng nguyên lý hướng đối tượng cho infrastructure
  - Tích hợp CDK với kiến thức CloudFormation hiện có

- **Thứ 4 - CDK Cơ bản 2 (Nâng cao):**

  - Xây dựng kiến trúc ứng dụng phức tạp với CDK
  - Triển khai API Gateway cho RESTful APIs
  - Cấu hình Elastic Load Balancer (ALB)
  - Tạo deployments Elastic Container Service (ECS)
  - Tích hợp Lambda functions với CDK
  - Triển khai nested stack patterns
  - Kết nối S3 buckets với Lambda triggers
  - Thiết kế kiến trúc multi-tier với CDK
  - Sử dụng CDK 2.151.0 cho các tính năng nâng cao
  - Áp dụng architectural best practices với IaC

- **Thứ 5 - Giới thiệu Infrastructure as Code:**

  - So sánh các IaC frameworks và phương pháp khác nhau
  - Hiểu lợi ích của IaC cho tăng năng suất
  - Tạo Lambda functions thông qua IaC
  - Xây dựng VPC và EC2 infrastructure theo chương trình
  - Triển khai kiến trúc web three-tier
  - Quản lý infrastructure thông qua source code
  - Áp dụng version control cho infrastructure definitions
  - Tự động hóa các quy trình triển khai và quản lý
  - Hiểu ưu điểm của IaC so với provisioning thủ công
  - Chuẩn bị cho triển khai IaC quy mô doanh nghiệp

- **Thứ 6 - Tối ưu kích thước EC2:**

  - Triển khai tối ưu hóa EC2 resources với CloudWatch
  - Tạo IAM roles cho CloudWatch Agent
  - Cài đặt và cấu hình CloudWatch Agent trên EC2
  - Thu thập memory usage metrics (GB consumed)
  - Phân tích CloudWatch data points cho quyết định sizing
  - Sử dụng AWS Compute Optimizer cho recommendations
  - Áp dụng right-sizing best practices cho EC2
  - Tối ưu hóa compute configurations dựa trên metrics
  - Giảm chi phí thông qua sizing instance hợp lý
  - Triển khai continuous monitoring cho optimization

- **Kết quả tổng thể tuần 7:**
  - Hoàn thành 5 workshop về Infrastructure as Code
  - Nắm vững CloudFormation và CDK cho triển khai infrastructure
  - Xây dựng kiến trúc nâng cao với API Gateway, ECS, Lambda
  - Hiểu các IaC frameworks và phương pháp luận
  - Tối ưu hóa EC2 resources với CloudWatch monitoring
  - Sẵn sàng triển khai các giải pháp IaC cấp doanh nghiệp
