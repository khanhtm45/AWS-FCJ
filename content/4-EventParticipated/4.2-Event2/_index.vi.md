---
title: "Event 2"
date: 2024-10-15
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

# Bài Thu Hoạch: "Workshop Giới Thiệu AI và Dịch Vụ AI trên AWS"

### Thông Tin Sự Kiện

**Ngày:** 15 tháng 10, 2024  
**Địa điểm:** Hội trường Trường Đại học  
**Diễn giả:** Thầy Khánh và Thầy Vương  
**Hình thức:** Workshop trực tiếp với thực hành

### Mục Đích Của Sự Kiện

- Giới thiệu khái niệm cơ bản về Trí tuệ Nhân tạo (AI)
- Khám phá sự tiến hóa từ Machine Learning đến Deep Learning và Generative AI
- Trình diễn các dịch vụ AI của AWS và ứng dụng thực tế
- Hướng dẫn sinh viên bắt đầu với nền tảng AWS
- Cung cấp trải nghiệm thực hành với các use case thực tế

### Danh Sách Diễn Giả

- **Thầy Khánh** – Giảng viên Kỹ thuật AWS
- **Thầy Vương** – Solutions Architect AWS

### Nội Dung Nổi Bật

#### Hiểu về AI: Từ Định Nghĩa đến Ứng Dụng Hiện Đại

**Trí Tuệ Nhân Tạo là gì?**

AI là khả năng của máy móc thực hiện các tác vụ thường yêu cầu trí thông minh con người, bao gồm:

- **Hiểu biết**: Thấu hiểu ngôn ngữ, ngữ cảnh và ý nghĩa
- **Lý luận**: Đưa ra quyết định logic dựa trên thông tin có sẵn
- **Học tập**: Cải thiện hiệu suất thông qua kinh nghiệm

Diễn giả nhấn mạnh rằng AI không phải là ma thuật—nó tuân theo các mô hình toán học và thuật toán có thể hiểu và kiểm soát được.

#### Tiến Hóa của Công Nghệ AI

**1. Machine Learning (AI Truyền Thống)**

- Sử dụng thuật toán để học các pattern từ dữ liệu
- Yêu cầu dữ liệu có cấu trúc và được gán nhãn
- Ví dụ: Dự đoán số xổ số dựa trên dữ liệu 10 năm
- Phù hợp với các vấn đề đơn giản, được định nghĩa rõ

**2. Deep Learning (AI Hiện Đại)**

- Mô phỏng mạng nơ-ron não người với nhiều lớp
- Có thể xử lý các loại dữ liệu phức tạp: hình ảnh, âm thanh, video
- Sử dụng kiến trúc mạng nơ-ron tương tự não người
- Cho phép hiểu dữ liệu không có cấu trúc

**3. Generative AI (Tiến Hóa Mới Nhất)**

- Học từ bộ dữ liệu khổng lồ (Large Language Models - LLMs)
- Có thể tạo ra nội dung hoàn toàn mới: văn bản, hình ảnh, video
- Ví dụ: ChatGPT, Google Gemini, Amazon Bedrock
- Có khả năng thực hiện các tác vụ sáng tạo như viết thơ, tạo ảnh nghệ thuật

#### Nền Tảng AWS Cloud và Dịch Vụ AI

**Tại Sao Chọn AWS?**

AWS phát triển dịch vụ dựa trên:

1. **Sử dụng nội bộ trước**: Dịch vụ được test trên vận hành Amazon.com
2. **Phản hồi khách hàng**: Tính năng phát triển dựa trên nhu cầu thực tế
3. **Đổi mới liên tục**: Hơn 200 dịch vụ và 10,000+ tính năng

**Kiến Trúc Ba Tầng:**

1. **Tầng AI Services (Trên)**: API sẵn sàng sử dụng

   - Amazon Comprehend: Phân tích văn bản và phát hiện cảm xúc
   - Amazon Translate: Dịch đa ngôn ngữ
   - Amazon Textract: Trích xuất dữ liệu từ tài liệu
   - Amazon Transcribe: Chuyển đổi giọng nói thành chữ
   - Amazon Polly: Chuyển đổi chữ thành giọng nói

2. **Tầng ML Platform (Giữa)**:

   - Amazon SageMaker: Xây dựng, huấn luyện và triển khai model tùy chỉnh
   - Kiểm soát hoàn toàn quá trình training và tối ưu hóa model

3. **Tầng Infrastructure (Dưới)**:
   - GPU instances cho training
   - Hợp tác với NVIDIA cho tính toán hiệu năng cao

#### Amazon Comprehend - Xử Lý Ngôn Ngữ Tự Nhiên

**Khả Năng:**

- Phân tích cảm xúc (tích cực, tiêu cực, trung tính)
- Nhận diện thực thể (tên, địa điểm, tổ chức)
- Phát hiện ngôn ngữ
- Trích xuất cụm từ khóa
- Phân loại tài liệu

**Ứng Dụng Thực Tế:**

1. **Phân Tích Đánh Giá Thương Mại Điện Tử**

   - Tự động phân loại đánh giá khách hàng là tích cực/tiêu cực
   - Trích xuất chủ đề chính từ feedback
   - Theo dõi cảm xúc về thương hiệu

2. **Giám Sát Mạng Xã Hội**

   - Phân tích dư luận trên các nền tảng
   - Xác định xu hướng và thay đổi cảm xúc

3. **Dịch Vụ Chăm Sóc Khách Hàng**

   - Phân loại ticket hỗ trợ tự động
   - Định tuyến vấn đề khẩn cấp dựa trên cảm xúc
   - Tạo gợi ý phản hồi

4. **Phân Tích Tài Liệu Tài Chính**
   - Trích xuất thông tin quan trọng từ báo cáo tài chính
   - Xác định thông tin cá nhân nhạy cảm để tuân thủ
   - Tự động che giấu PII (Personally Identifiable Information)

#### Amazon Translate - Dịch Vụ Dịch Thuật

**Tính Năng:**

- Hỗ trợ 75+ ngôn ngữ bao gồm tiếng Việt
- Dịch real-time
- Dịch tài liệu hàng loạt
- Hỗ trợ thuật ngữ tùy chỉnh

**Use Cases:**

1. **Website Đa Ngôn Ngữ**

   - Tự động dịch nội dung cho người dùng quốc tế
   - Hỗ trợ nền tảng thương mại điện tử
   - Ứng dụng du lịch và tourism

2. **Dịch Tài Liệu**

   - Dịch tài liệu doanh nghiệp
   - Xử lý giao tiếp khách hàng đa ngôn ngữ
   - Xử lý tài liệu tiếng Khmer (Campuchia) với tiền xử lý OCR

3. **Ứng Dụng Học Ngôn Ngữ**
   - Ví dụ: ELSA (app học tiếng Anh)
   - Kiểm tra phát âm
   - Thực hành dịch real-time

#### Amazon Textract - Xử Lý Tài Liệu Thông Minh

**Khả Năng:**

- Trích xuất text từ PDF và hình ảnh
- Nhận diện bảng biểu và form
- Bảo toàn cấu trúc tài liệu
- Nhận diện chữ viết tay

**Ứng Dụng Thực Tế:**

- Chuyển đổi PDF sang Word/PowerPoint
- Trích xuất dữ liệu từ hóa đơn và biên lai
- Xử lý form chính phủ tự động
- Số hóa tài liệu lịch sử

Giảng viên đã demo trực tiếp cách Textract có thể chụp text từ ảnh với độ chính xác cao, bao gồm cả tiếng Việt.

#### Mô Hình Dịch Vụ Cloud

Workshop giải thích ba mô hình cung cấp dịch vụ:

1. **Software as a Service (SaaS)**

   - Ứng dụng sẵn sàng sử dụng (Google Translate, v.v.)
   - Không cần cài đặt
   - Tính phí theo sử dụng

2. **Platform as a Service (PaaS)**

   - API và dịch vụ AWS
   - Công cụ và framework cho developer
   - Triển khai đơn giản hóa

3. **Infrastructure as a Service (IaaS)**
   - Máy ảo và lưu trữ
   - Kiểm soát hoàn toàn môi trường
   - Tài nguyên có thể mở rộng

#### Tài Nguyên Học Tập và Bắt Đầu

**AWS Skill Builder:**

- Nền tảng đào tạo miễn phí
- 2000+ khóa học (80% miễn phí)
- Lab thực hành và chứng chỉ
- Sẽ hỗ trợ tiếng Việt sớm

**AWS Free Tier:**

- $200 credits cho sinh viên
- Môi trường sandbox để thử nghiệm
- Không cần thẻ tín dụng cho tài khoản học tập

### Bài Học Rút Ra

1. **AI Dễ Tiếp Cận**: Dịch vụ AI hiện đại có sẵn qua API đơn giản, không cần bằng tiến sĩ
2. **Bắt Đầu Nhỏ**: Sử dụng dịch vụ AI có sẵn trước khi xây dựng giải pháp tùy chỉnh
3. **Dữ Liệu Là Quan Trọng**: Chất lượng và số lượng dữ liệu quyết định thành công AI
4. **Dữ Liệu Tạo Ra Hoạt Động**: AI có thể tạo dữ liệu tổng hợp để test và demo
5. **Lựa Chọn Open Source**: Nhiều phương án miễn phí tồn tại (TensorFlow, PyTorch)
6. **Quyền Riêng Tư Quan Trọng**: AWS không sử dụng dữ liệu khách hàng để training model
7. **Quản Lý Chi Phí**: Sử dụng free tier và sandbox cho học tập

### Lời Khuyên Thực Tế Cho Sinh Viên

**Thu Thập Dữ Liệu:**

- Web scraping (với cân nhắc đạo đức)
- Dataset Kaggle cho dự án thực hành
- Dữ liệu tổng hợp do AI tạo để test
- Báo cáo tài chính công khai và nguồn dữ liệu mở

**Phát Triển Dự Án:**

- Bắt đầu với framework open-source (PyTorch, TensorFlow)
- Sử dụng Google Colab hoặc Jupyter notebooks
- Tận dụng credits AWS để scale
- Tập trung giải quyết vấn đề kinh doanh thực tế

**Phát Triển Nghề Nghiệp:**

- Xây dựng dự án thực tế, không chỉ lý thuyết
- Hiểu quy trình end-to-end
- Học cả khía cạnh kỹ thuật và kinh doanh
- Đóng góp cho dự án open-source

### Những Điểm Nổi Bật Từ Q&A

**H: Làm thế nào xử lý quyền riêng tư dữ liệu công ty khi dùng AI?**
Đ: Dữ liệu ở lại trên server công ty; chỉ có API call được thực hiện tới dịch vụ AI. AWS cam kết bảo mật dữ liệu nghiêm ngặt và không training model trên dữ liệu khách hàng.

**H: Làm sao lấy dữ liệu cho dự án với nguồn lực hạn chế?**
Đ:

1. Tạo dữ liệu tổng hợp với AI
2. Sử dụng web scraping (có đạo đức)
3. Truy cập dataset Kaggle
4. Dùng dataset public domain (dữ liệu COVID, báo cáo tài chính)
5. Tận dụng Yahoo Finance cho dữ liệu tài chính

**H: Làm thế nào test dự án ở quy mô lớn không có tài nguyên?**
Đ: Sử dụng môi trường sandbox AWS, đăng ký credits sinh viên ($200 có sẵn), và tham gia các cuộc thi cung cấp hạ tầng.

**H: Có thể phân tích cảm xúc từ giọng nói không?**
Đ: Có, nhưng cần hai cách tiếp cận:

1. Chuyển speech sang text, sau đó phân tích sentiment
2. Phân tích thuộc tính âm thanh (mức decibel, giọng điệu, cao độ)
   Cả hai đều cần dữ liệu training được gán nhãn phân biệt các trạng thái cảm xúc khác nhau.

**H: Dữ liệu do AI tạo có đáng tin để training không?**
Đ: Phù hợp cho demo và proof-of-concept, nhưng không dùng cho hệ thống production với người dùng thực. Tuyệt vời để chứng minh tính khả thi nhưng cần dữ liệu thật cho triển khai thực tế.

### Góc Nhìn Cá Nhân

Workshop này vô cùng giá trị để hiểu khía cạnh thực tế của phát triển AI. Thay vì chỉ là khái niệm lý thuyết, các giảng viên đã trình diễn các dịch vụ AWS thực tế đang được sử dụng trong production bởi các công ty lớn.

Việc nhấn mạnh vào việc bắt đầu với dịch vụ có sẵn thay vì xây dựng từ đầu thật sự mở mang tầm mắt. Là sinh viên, chúng ta thường muốn tự xây dựng mọi thứ, nhưng tận dụng API có sẵn có thể đẩy nhanh phát triển và để chúng ta tập trung giải quyết vấn đề kinh doanh thực tế.

Phần Q&A đặc biệt hữu ích, giải quyết các lo ngại thực tế về quyền riêng tư dữ liệu, quản lý chi phí và khả năng mở rộng dự án. Lời khuyên sử dụng công cụ open-source để học và dịch vụ AWS để scale cung cấp lộ trình rõ ràng.

### Hình Ảnh Workshop

_Thêm ảnh workshop của bạn tại đây:_

- Demo trực tiếp các dịch vụ AWS
- Bài thuyết trình của giảng viên
- Bài tập thực hành
- Phần Q&A

> Workshop này làm sáng tỏ AI và dịch vụ cloud, cho thấy rằng phát triển AI hiện đại dễ tiếp cận với sinh viên và đòi hỏi nhiều sáng tạo và giải quyết vấn đề hơn là chỉ chuyên môn kỹ thuật. Sự kết hợp giữa dịch vụ AWS và công cụ open-source cung cấp mọi thứ cần thiết để xây dựng ứng dụng AI thực tế.

### Các Bước Tiếp Theo

1. **Tạo Tài Khoản AWS Free Tier**: Bắt đầu thực hành
2. **Khám Phá AWS Skill Builder**: Hoàn thành các khóa học AI cơ bản
3. **Thử Dịch Vụ AWS**: Thử nghiệm với Comprehend, Translate và Textract
4. **Xây Dựng Dự Án**: Áp dụng kiến thức học được để giải quyết vấn đề thực tế
5. **Tham Gia Cộng Đồng AWS**: Kết nối với các learner và builder khác

### Kết Luận

Workshop "Giới Thiệu AI và Dịch Vụ AI trên AWS" cung cấp cái nhìn toàn diện về công nghệ AI hiện đại và công cụ thực tế để triển khai. Sự kết hợp giữa nền tảng lý thuyết, demo trực tiếp và hướng dẫn thực hành làm cho dịch vụ AI của AWS dễ tiếp cận với developer ở mọi cấp độ. Thông điệp chính: bắt đầu xây dựng với công cụ có sẵn, tập trung giải quyết vấn đề thực tế, và liên tục học hỏi và thử nghiệm.
