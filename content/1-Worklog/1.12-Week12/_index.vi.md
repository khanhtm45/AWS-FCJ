---
title: "Worklog Tuần 12"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.12 </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 12:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                          | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** Serverless - CI/CD với AWS CodePipeline <br>&emsp; + Xây dựng SAM pipeline <br>&emsp; + Tạo frontend pipeline <br>&emsp; + Tự động hóa deployments <br>&emsp; + Test CI/CD workflow                | 24/11/2025   | 24/11/2025      | <https://000084.awsstudygroup.com/> |
| 3   | - **Workshop:** DMS - Hệ thống Quản lý Tài liệu Lambda Functions <br>&emsp; + Tạo DynamoDB tables <br>&emsp; + Viết Lambda functions <br>&emsp; + Triển khai quản lý files <br>&emsp; + Test Lambda operations     | 25/11/2025   | 25/11/2025      | <https://000133.awsstudygroup.com/> |
| 4   | - **Workshop:** Serverless - Amplify Authentication và Storage <br>&emsp; + Cấu hình Amplify authentication <br>&emsp; + Thiết lập S3 storage <br>&emsp; + Triển khai access levels <br>&emsp; + Test file uploads | 26/11/2025   | 26/11/2025      | <https://000134.awsstudygroup.com/> |
| 5   | - **Workshop:** Serverless - Thiết lập S3 Static SSL Website <br>&emsp; + Tạo custom domain với Route 53 <br>&emsp; + Yêu cầu SSL certificate <br>&emsp; + Cấu hình CloudFront CDN <br>&emsp; + Bật HTTPS          | 27/11/2025   | 27/11/2025      | <https://000137.awsstudygroup.com/> |
| 6   | - **Workshop:** Serverless - Giám sát với CloudWatch và X-Ray <br>&emsp; + Cấu hình CloudWatch monitoring <br>&emsp; + Thiết lập X-Ray tracing <br>&emsp; + Phân tích performance <br>&emsp; + Debug applications  | 28/11/2025   | 28/11/2025      | <https://000140.awsstudygroup.com/> |

### Kết quả đạt được tuần 12:

- **Thứ 2 - Serverless CI/CD:**

  - Nắm vững thực hành CI/CD cho ứng dụng serverless
  - Xây dựng SAM (Serverless Application Model) pipeline
  - Tạo frontend pipeline cho static websites
  - Tự động hóa deployments với AWS CodePipeline
  - Tích hợp GitLab/CodeCommit với CodeBuild
  - Cấu hình CloudFormation cho serverless updates
  - Tự động hóa build và deployment đến S3
  - Triển khai continuous integration workflows
  - Áp dụng continuous delivery practices
  - Giảm thời gian và rủi ro deployment
  - Loại bỏ quy trình deployment thủ công
  - Xây dựng CI/CD pipelines production-ready

- **Thứ 3 - Hệ thống Quản lý Tài liệu:**

  - Xây dựng Document Management System (DMS) hoàn chỉnh
  - Tạo DynamoDB tables cho file metadata
  - Triển khai Lambda functions cho CRUD operations
  - Xây dựng file upload và download functionality
  - Triển khai khả năng tìm kiếm tài liệu
  - Tạo tính năng xóa tài liệu
  - Theo dõi thống kê files (count, size, updates)
  - Tích hợp với S3 cho file storage
  - Sử dụng Amplify cho authentication và storage
  - Triển khai với AWS SAM
  - Cấu hình SSL/TLS với CloudFront
  - Xây dựng ứng dụng serverless hoàn chỉnh

- **Thứ 4 - Amplify Auth & Storage:**

  - Triển khai AWS Amplify authentication
  - Cấu hình Cognito User Pools với Amplify
  - Thiết lập S3 storage với Amplify
  - Triển khai file upload lên S3
  - Cấu hình storage access levels
  - Quản lý user authentication flows
  - Tích hợp Amplify library với frontend
  - Xây dựng hệ thống quản lý files bảo mật
  - Áp dụng access control patterns
  - Đơn giản hóa triển khai authentication
  - Sử dụng Amplify CLI cho configuration
  - Xây dựng auth system production-ready

- **Thứ 5 - SSL Website với CloudFront:**

  - Bảo mật S3 static website với SSL/TLS
  - Tạo custom domain với Route 53
  - Yêu cầu SSL certificate từ ACM
  - Cấu hình CloudFront distribution
  - Bật HTTPS cho kết nối bảo mật
  - Triển khai in-flight encryption
  - Cấu hình CDN cho hiệu suất
  - Liên kết custom domain qua DNS
  - Áp dụng SSL certificate cho CloudFront
  - Cải thiện website security
  - Nâng cao content delivery performance
  - Xây dựng secure website production-ready

- **Thứ 6 - Giám sát CloudWatch & X-Ray:**

  - Triển khai giám sát toàn diện với CloudWatch
  - Thiết lập distributed tracing với X-Ray
  - Giám sát Lambda function performance
  - Phân tích application traces
  - Debug serverless applications
  - Cấu hình CloudWatch Logs
  - Tạo CloudWatch dashboards
  - Thiết lập CloudWatch Alarms
  - Trace requests across services
  - Xác định performance bottlenecks
  - Áp dụng observability best practices
  - Xây dựng hệ thống monitoring production

- **Kết quả tổng thể tuần 12:**
  - Hoàn thành 5 workshop serverless nâng cao
  - Nắm vững tự động hóa serverless CI/CD
  - Xây dựng Document Management System hoàn chỉnh
  - Triển khai authentication bảo mật với Amplify
  - Cấu hình SSL/TLS cho production websites
  - Thiết lập giám sát và tracing toàn diện
  - Sẵn sàng triển khai ứng dụng serverless doanh nghiệp
