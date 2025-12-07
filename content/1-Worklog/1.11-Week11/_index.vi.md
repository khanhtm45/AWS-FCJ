---
title: "Worklog Tuần 11"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 11:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                 | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                      |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------- |
| 2   | - **Workshop:** Cấu hình Tự động Triển khai với CodeStar <br>&emsp; + Thiết lập AWS CodeStar project <br>&emsp; + Sử dụng CodeCommit với Eclipse IDE <br>&emsp; + Triển khai lên Elastic Beanstalk <br>&emsp; + Triển khai CI/CD pipeline | 17/11/2025   | 17/11/2025      | <https://000051.awsstudygroup.com/> |
| 3   | - **Workshop:** Serverless Bookstore - Lambda Functions <br>&emsp; + Tạo Lambda functions <br>&emsp; + Xử lý S3 triggers <br>&emsp; + Xử lý ảnh với Lambda <br>&emsp; + Ghi dữ liệu vào DynamoDB                                          | 18/11/2025   | 18/11/2025      | <https://000078.awsstudygroup.com/> |
| 4   | - **Workshop:** Serverless - Xây dựng Frontend với API Gateway <br>&emsp; + Triển khai frontend lên Amplify <br>&emsp; + Tạo Lambda functions <br>&emsp; + Cấu hình API Gateway <br>&emsp; + Test APIs với Postman                        | 19/11/2025   | 19/11/2025      | <https://000079.awsstudygroup.com/> |
| 5   | - **Workshop:** Serverless - Xác thực với Cognito <br>&emsp; + Tạo Cognito User Pool <br>&emsp; + Triển khai sign-in/sign-up <br>&emsp; + Cấu hình Lambda authorizers <br>&emsp; + Test authentication flow                               | 20/11/2025   | 20/11/2025      | <https://000081.awsstudygroup.com/> |
| 6   | - **Workshop:** Serverless - Xử lý Đơn hàng với SQS và SNS <br>&emsp; + Tạo SQS queues <br>&emsp; + Thiết lập SNS topics <br>&emsp; + Triển khai xử lý orders <br>&emsp; + Tích hợp Lambda với SQS/SNS                                    | 21/11/2025   | 21/11/2025      | <https://000083.awsstudygroup.com/> |

### Kết quả đạt được tuần 11:

- **Thứ 2 - CodeStar Tự động Triển khai:**

  - Nắm vững AWS CodeStar cho quản lý CI/CD thống nhất
  - Thiết lập continuous delivery toolchain trong vài phút
  - Cấu hình AWS CodeCommit Git repositories
  - Sử dụng Eclipse IDE với CodeCommit integration
  - Triển khai AWS CodeBuild cho compilation và testing
  - Tạo AWS CodePipeline cho automated releases
  - Triển khai ứng dụng Java Spring lên Elastic Beanstalk
  - Triển khai CodeDeploy cho Windows Service deployment
  - Cấu hình automatic triggers trên code commits
  - Quản lý team access với CodeStar dashboard
  - Tích hợp JIRA cho issue tracking
  - Áp dụng lift-and-shift migration sang PaaS

- **Thứ 3 - Serverless Lambda Functions:**

  - Hiểu kiến trúc serverless cơ bản
  - Tạo AWS Lambda functions cho compute
  - Triển khai S3 event triggers
  - Xây dựng image resizing function với Lambda
  - Xử lý S3 object uploads tự động
  - Lưu trữ dữ liệu trong Amazon DynamoDB
  - Cấu hình Lambda IAM roles và permissions
  - Áp dụng serverless best practices
  - Loại bỏ overhead quản lý server
  - Xây dựng ứng dụng scalable không cần infrastructure
  - Sử dụng DynamoDB cho data persistence
  - Tích hợp nhiều AWS serverless services

- **Thứ 4 - API Gateway Frontend:**

  - Xây dựng frontend web application cho serverless backend
  - Triển khai static website lên AWS Amplify
  - Tạo Lambda functions cho API endpoints
  - Cấu hình Amazon API Gateway
  - Triển khai RESTful APIs
  - Kết nối frontend đến DynamoDB qua Lambda
  - Test APIs với Postman
  - Tích hợp API Gateway với Lambda
  - Cấu hình CORS cho frontend access
  - Triển khai end-to-end serverless web application
  - Áp dụng API Gateway best practices
  - Xây dựng kiến trúc serverless hoàn chỉnh

- **Thứ 5 - Xác thực Cognito:**

  - Triển khai authentication với Amazon Cognito
  - Tạo Cognito User Pools
  - Xây dựng sign-in và sign-up flows
  - Triển khai email verification
  - Cấu hình password reset functionality
  - Sử dụng Cognito Identity Pools cho AWS access
  - Tích hợp third-party authentication providers
  - Tạo Lambda authorizers cho API Gateway
  - Triển khai JWT token validation
  - Bảo mật serverless APIs với authentication
  - Áp dụng user management best practices
  - Xây dựng hệ thống authentication hoàn chỉnh

- **Thứ 6 - Xử lý Đơn hàng SQS và SNS:**

  - Xây dựng hệ thống xử lý orders với SQS và SNS
  - Tạo Amazon SQS queues cho message handling
  - Cấu hình Amazon SNS topics cho notifications
  - Triển khai pub/sub messaging patterns
  - Xử lý orders bất đồng bộ với queues
  - Gửi admin notifications qua SNS
  - Tạo Lambda functions cho order handling
  - Lưu trữ processed orders trong DynamoDB
  - Triển khai order management interface
  - Cấu hình message filtering và routing
  - Áp dụng decoupled architecture patterns
  - Xây dựng ứng dụng message-driven scalable

- **Kết quả tổng thể tuần 11:**
  - Hoàn thành 5 workshop về Serverless và DevOps automation
  - Nắm vững AWS Developer Tools (CodeStar, CodeCommit, CodeBuild, CodeDeploy, CodePipeline)
  - Xây dựng ứng dụng serverless web hoàn chỉnh
  - Triển khai authentication và authorization với Cognito
  - Tạo kiến trúc message-driven với SQS và SNS
  - Sẵn sàng xây dựng ứng dụng serverless production
