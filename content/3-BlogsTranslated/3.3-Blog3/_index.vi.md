---
title: "Tối đa hóa Giá trị của Smart Machines với AI Tạo sinh và IoT"
date: 2025-07-11
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Tối đa hóa Giá trị của Smart Machines với AI Tạo sinh và IoT

**Tác giả: Dimitrios Spiliopoulos, Gabriel Verreault, và Gary Emmerton | ngày 11 tháng 7 năm 2025**

Trong bối cảnh công nghiệp cạnh tranh ngày nay, các nhà cung cấp máy móc công nghiệp, chẳng hạn như thiết bị xây dựng và khai thác mỏ, và máy móc nhà máy, đang tìm kiếm những cách sáng tạo để tối đa hóa tiềm năng của sản phẩm của họ. Bằng cách kết nối các máy móc này với đám mây thông qua IoT, các nhà sản xuất máy móc có được khả năng hiển thị về cách thiết bị của họ hoạt động trong điều kiện thực tế—hiểu các mô hình sử dụng, xác định các chế độ lỗi lặp lại và khám phá các cơ hội tối ưu hóa thúc đẩy cả cải tiến thiết bị và các dịch vụ mới.

Việc xây dựng một giải pháp kết nối máy-đến-đám mây toàn diện có thể phức tạp và tốn thời gian. Trong blog [Xây dựng Máy Công nghiệp Thông minh với AWS: Hướng dẫn Toàn diện](https://aws.amazon.com/blogs/iot/building-smart-industrial-machines-with-aws-iot-a-comprehensive-guide/), chúng tôi đã trình bày cách các dịch vụ AWS IoT cho phép các giải pháp công nghiệp an toàn, có thể mở rộng mà không cần đầu tư cơ sở hạ tầng rộng lớn. Trong blog này, chúng tôi sẽ khám phá tiềm năng biến đổi của việc kết hợp AI tạo sinh với IoT cho Smart Machines với trọng tâm vào cách các nhà sản xuất thiết bị có thể tận dụng những khả năng này kết hợp để cách mạng hóa hoạt động công nghiệp, tạo ra những hiểu biết mới và thúc đẩy kết quả kinh doanh cụ thể bằng cách tận dụng các dịch vụ AI tạo sinh của AWS, như [Amazon Bedrock](https://aws.amazon.com/bedrock/), kết hợp với các dịch vụ AWS IoT, như [AWS IoT Core](https://aws.amazon.com/iot-core/) và [AWS IoT SiteWise](https://aws.amazon.com/iot-sitewise/).

## AI Tạo sinh cho Smart Machines

[AI Tạo sinh](https://aws.amazon.com/what-is/generative-ai/) có thể thúc đẩy đổi mới đáng kể trong các trường hợp sử dụng công nghiệp bằng cách rút ra những hiểu biết có thể hành động từ dữ liệu hoạt động và sản phẩm. Chúng trao quyền cho người vận hành máy hoặc kỹ sư dịch vụ giải quyết vấn đề nhanh hơn, nhất quán và có thể lặp lại. Theo [nghiên cứu từ Capgemini](https://prod.ucwe.capgemini.com/wp-content/uploads/2023/07/Final-Web-Version-Report-Harnessing-the-Value-of-Gen-AI.1.pdf), đa số các nhà sản xuất không chỉ tò mò về AI tạo sinh; 55% đang tích cực khám phá tiềm năng của nó và 45% hiện đang làm việc trên các dự án thí điểm.

AWS và các Đối tác AWS giúp các công ty dễ dàng xây dựng và mở rộng các ứng dụng dựa trên AI tạo sinh một cách hiệu quả hơn. Chúng tôi sẽ khám phá bốn trường hợp sử dụng Smart Machines cho các nhà sản xuất thiết bị gốc (OEM) được hỗ trợ bởi sự kết hợp của AI tạo sinh và IoT:

### 1. Chẩn đoán và Khắc phục Sự cố Có hỗ trợ

Sự kết hợp của IoT và AI tạo sinh có thể cách mạng hóa quản lý bảo trì. Ví dụ, xem xét tình huống trong đó dữ liệu từ các cảm biến IoT trên thiết bị kích hoạt cảnh báo bất thường do một ngưỡng, chẳng hạn như nhiệt độ, áp suất hoặc rung động, bị vi phạm. Các cảnh báo này có thể được làm phong phú thêm với ngữ cảnh bổ sung từ phân tích AI tạo sinh về sách hướng dẫn thiết bị, tài liệu quy trình vận hành tiêu chuẩn (SOP), hồ sơ bảo trì lịch sử, kinh nghiệm con người được ghi lại, lịch sử phụ tùng thay thế và nhiều hơn nữa.

Cùng với các cảnh báo, các nhóm bảo trì có thể nhận được ngữ cảnh đầy đủ về vấn đề, hướng dẫn sửa chữa chi tiết từng bước, khuyến nghị phụ tùng cụ thể và danh sách các công cụ cần thiết cho việc sửa chữa. Điều này đơn giản hóa việc khắc phục sự cố và giảm thời gian sửa chữa cho cả kỹ thuật viên dịch vụ OEM và nhân viên bảo trì của khách hàng cuối, giảm nhu cầu về các kỹ sư dịch vụ có kinh nghiệm tại chỗ.

Để có một triển khai mẫu của trường hợp sử dụng này, hãy tham khảo [Guidance for Assisted Diagnosis and Troubleshooting on AWS](https://aws.amazon.com/solutions/guidance/assisted-diagnosis-and-troubleshooting-on-aws/). Sự kết hợp này cung cấp hướng dẫn bảo trì toàn diện vượt xa phát hiện lỗi và thậm chí có thể được cung cấp thông qua [trợ lý AI hỗ trợ giọng nói](https://aws.amazon.com/blogs/messaging-and-targeting/building-voice-interface-for-genai-assistant/) với các mô hình giọng nói-đến-giọng nói cho phép các kỹ thuật viên yêu cầu thông tin chẩn đoán bằng lời nói trong khi giữ tay rảnh để sửa chữa.

### 2. Hoạt động Dịch vụ Hiện trường Nâng cao

Dựa trên nền tảng của chẩn đoán và khắc phục sự cố có hỗ trợ tại chỗ, các nhà sản xuất máy có thể chuyển đổi hoạt động dịch vụ hiện trường với AI tạo sinh thông qua chẩn đoán từ xa và chuẩn bị thông minh trước chuyến thăm. Các nhóm dịch vụ hiện trường nhận các báo cáo chẩn đoán do AI tạo ra, cho phép họ phân tích dữ liệu máy, chẳng hạn như số đọc cảm biến và mã lỗi, từ xa và nhanh chóng chuẩn bị những gì cần thiết cho mỗi lần sửa chữa nếu cần một chuyến thăm tại chỗ.

Việc chuẩn bị này bao gồm thông tin chi tiết về phụ tùng thay thế, các công cụ phù hợp cần thiết và phù hợp chuyên môn của kỹ thuật viên với vấn đề cụ thể. Kết quả là giảm nhiều lần thăm viếng hiện trường, giảm chi phí bảo trì và cải thiện đáng kể tỷ lệ sửa chữa lần đầu và thời gian sửa chữa. Phân tích lỗi và chuẩ bị tốt hơn cho phép phân bổ tài nguyên tốt hơn, thời gian sửa chữa nhanh hơn, triển khai kỹ thuật viên hiệu quả hơn và cải thiện trải nghiệm khách hàng.

Xem [video này](https://www.youtube.com/watch?v=ip7Q-mYrMq4) để biết cách KONE, một nhà lãnh đạo toàn cầu về thang máy và thang cuốn, cùng với AWS, đã phát triển một trợ lý kỹ thuật viên được hỗ trợ AI để giúp các kỹ thuật viên sửa chữa thang máy nhanh hơn bằng cách phân tích lịch sử bảo trì, dữ liệu IoT và tài liệu liên quan từ các thang máy được kết nối của họ.

### 3. Phân tích Đội tàu Máy cho OEM

Phân tích đội tàu truyền thống yêu cầu các nhà khoa học dữ liệu và kỹ thuật dữ liệu phức tạp để trích xuất thông tin chi tiết từ hàng nghìn máy đã triển khai. AI tạo sinh chuyển đổi điều này bằng cách cho phép các truy vấn ngôn ngữ tự nhiên trên các tập dữ liệu rộng lớn, tự động tạo ra những hiểu biết tường thuật kết hợp dữ liệu telemetry với các nguồn phi cấu trúc, như báo cáo dịch vụ và phản hồi của người vận hành.

Thay vì xây dựng thủ công các dashboard để hiểu các mô hình hiệu suất, OEM có thể đặt câu hỏi, như "Các chế độ lỗi phổ biến cho máy xúc trong môi trường nhiệt độ cao là gì?", và nhận được các phân tích toàn diện xác định xu hướng, tương quan các yếu tố môi trường và khuyến nghị cải tiến thiết kế. Điều này làm cho thông tin chi tiết về đội tàu có thể truy cập được ngoài các nhóm kỹ thuật, cho phép các nhóm bán hàng và sản phẩm nhanh chóng hiểu cách thiết bị hoạt động trên các trường hợp sử dụng và môi trường khác nhau.

Những hiểu biết này cũng có thể cho phép các mô hình kinh doanh 'servitization' mới. Hệ thống tự động tạo ra các tường thuật hiệu suất chi tiết theo loại tài sản, phân khúc khách hàng và địa lý, tiết lộ các mô hình mà trước đây sẽ yêu cầu phân tích thủ công đáng kể.

### 4. Báo cáo Chẩn đoán do AI Tạo ra

OEM có thể tận dụng AI tạo sinh để tạo các báo cáo hoạt động toàn diện từ sản phẩm của họ, tổng hợp nhiều nguồn dữ liệu, bao gồm dữ liệu telemetry, lịch sử bảo trì, điều kiện môi trường và nhật ký sự cố. Các báo cáo này có thể tạo ra những hiểu biết chiến lược cho các nhóm của họ, cũng tiết kiệm thời gian từ báo cáo thủ công và thu thập dữ liệu.

Không giống như chẩn đoán phản ứng, các báo cáo này phân tích các mô hình hiệu suất rộng hơn để thông báo phát triển sản phẩm, xác định cải tiến thiết kế và tối ưu hóa các chiến lược dịch vụ và hỗ trợ khách hàng. Các báo cáo này có thể có cách tiếp cận báo cáo kép tạo giá trị ở cả hai cấp: thông tin chiến lược cho các nhà sản xuất và báo cáo đa chiều tự động cho khách hàng.

OEM có thể cung cấp các khả năng chẩn đoán này như các dịch vụ cao cấp cho khách hàng của họ, tạo ra doanh thu định kỳ trong khi xây dựng mối quan hệ khách hàng mạnh mẽ hơn thông qua độ tin cậy thiết bị được cải thiện, dịch vụ khách hàng tốt hơn và thông tin chi tiết để quản lý hoạt động của khách hàng.

Xem [video này](https://www.youtube.com/watch?v=oKYbuubSK_g) để biết cách HP đang chuyển đổi tương lai của in ấn công nghiệp với AWS, sử dụng IoT, machine learning và AI tạo sinh để tạo ra nhà máy in ấn Thông minh của tương lai.

## Kết nối Dữ liệu IoT với AI Tạo sinh

[Guidance for Deploying Smart Machines on AWS](https://aws.amazon.com/solutions/guidance/deploying-smart-machines-on-aws/) cung cấp điểm khởi đầu cho hành trình Smart Machines của bạn. Hướng dẫn này thiết lập các khối xây dựng cơ bản cần thiết để kết nối và quản lý các máy thông minh một cách hiệu quả ở quy mô, trong khi tạo ra một nền tảng dữ liệu công nghiệp cho phép bạn chuẩn bị, ngữ cảnh hóa và duy trì chất lượng dữ liệu cho các ứng dụng khác nhau. Với nền tảng này, các nhà sản xuất máy có thể phát triển các khả năng mới sử dụng AI tạo sinh trên AWS.

Dữ liệu IoT công nghiệp được nhập trực tiếp vào AWS IoT SiteWise sử dụng AWS IoT SiteWise Edge hoặc thông qua các quy tắc AWS IoT Core. Trong hệ thống, dữ liệu này được tổ chức thành các mô hình tài sản kỹ thuật số kết hợp cả thuộc tính tĩnh (ví dụ: số sê-ri, loại máy) và động (ví dụ: số đọc cảm biến, vị trí GPS). Các tài sản riêng lẻ này, chẳng hạn như động cơ, bộ truyền động và bơm sau đó được kết nối trong mối quan hệ cha-con để đại diện cho các máy và thiết bị lớn hơn.

Nền tảng của dữ liệu IoT có cấu trúc trở nên mạnh mẽ hơn khi kết hợp với các khả năng AI tạo sinh, chuyển đổi dữ liệu hoạt động thô thành những hiểu biết có thể hành động và phản hồi tự động thông minh cho bảo trì có hỗ trợ và phân tích quản lý đội tàu. Mô hình này cũng có thể mở rộng sang các hệ thống công nghiệp của bên thứ ba như nền tảng bảo trì để có được thông tin về phụ tùng thay thế và hồ sơ bảo trì.

## Amazon Bedrock: Giải pháp Linh hoạt cho Tích hợp IoT và AI Tạo sinh

Các nhà sản xuất máy làm việc trên các giải pháp máy thông minh có thể bắt đầu hành trình AI tạo sinh của họ với Amazon Bedrock. Amazon Bedrock là một dịch vụ được quản lý hoàn toàn cung cấp quyền truy cập dễ dàng vào lựa chọn các mô hình nền tảng (FM) hàng đầu. Với [Amazon Bedrock Knowledge Bases](https://aws.amazon.com/bedrock/knowledge-bases/), bạn có thể dễ dàng kết nối các mô hình này với dữ liệu của tổ chức bạn để cung cấp các phản hồi chính xác, có liên quan và theo ngữ cảnh dựa trên các nguồn thông tin cụ thể của bạn.

Amazon Bedrock Knowledge Bases kết nối với dữ liệu hiện có của bạn trong Amazon S3, các hệ thống bên ngoài và các giải pháp khách hàng bao gồm Salesforce, Confluence và SharePoint cũng như các endpoint tùy chỉnh, cho phép triển khai nhanh chóng. Thiết lập Amazon Bedrock Knowledge Base nhanh chóng và đơn giản bằng cách sử dụng các bước được xác định [tại đây](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base-create.html).

Kết hợp các mô hình và dữ liệu của bạn với [Amazon Bedrock Agents](https://aws.amazon.com/bedrock/agents/) cho phép bạn nhanh chóng rút ra thông tin chi tiết từ dữ liệu IoT và thông tin độc quyền của bạn, bất kể dữ liệu của bạn được lưu trữ ở đâu. Thông qua các tương tác ngôn ngữ tự nhiên, bạn có thể giám sát một máy duy nhất hoặc mở rộng liền mạch để quản lý toàn bộ đội tàu và tạo tóm tắt hoạt động. Amazon Bedrock Agents có thể điều phối và thực hiện các tác vụ đối với các hệ thống bên ngoài, cho phép bạn truy vấn dữ liệu IoT của mình và các hệ thống bảo trì của bạn để tạo ticket sự cố và cảnh báo mới.

Ví dụ, Amazon Bedrock agents có thể tự động tạo các ticket hỗ trợ trong [Amazon Connect](https://aws.amazon.com/connect/), được làm phong phú với dữ liệu IoT và thông tin chi tiết từ knowledge base. Khi các vấn đề về thiết bị xảy ra, hệ thống ngay lập tức thông báo cho người vận hành với thông tin theo ngữ cảnh, cho phép giải quyết nhanh hơn và dịch vụ khách hàng chủ động. Để biết thêm chi tiết về mô hình trung tâm liên lạc này, hãy tham khảo [Guidance for Connecting Automated Inputs to Contact Centers on AWS](https://aws.amazon.com/solutions/guidance/connecting-automated-inputs-to-contact-centers-on-aws/).

Amazon Bedrock cũng hỗ trợ [hợp tác đa tác nhân](https://docs.aws.amazon.com/bedrock/latest/userguide/agents-multi-agent-collaboration.html) để tăng tốc xây dựng các hệ thống agentic cho các quy trình làm việc phức tạp hơn. Xem [Amazon Bedrock multi-agent collaboration](https://catalog.us-east-1.prod.workshops.aws/workshops/1031afa5-be84-4a6a-9886-4e19ce67b9c2/en-US) để có một minh họa thực hành về khả năng này.

## Edge Intelligence cho Smart Machines

Triển khai các khả năng AI tạo sinh trực tiếp tại edge là một lựa chọn hấp dẫn cho thiết bị công nghiệp hoạt động trong môi trường có kết nối hạn chế hoặc không ổn định. Tùy thuộc vào kết nối và khả năng tính toán có sẵn, một cách tiếp cận hybrid cũng có thể được sử dụng trong đó các tác vụ thường xuyên nhỏ hơn thực thi đối với các mô hình edge và các truy vấn phức tạp hơn được chuyển sang các mô hình ngôn ngữ lớn (LLM) trong đám mây nếu có kết nối.

Nhúng các mô hình ngôn ngữ nhỏ (SLM) trực tiếp vào các máy thông minh của họ cũng có thể, cho phép hỗ trợ liên tục được hỗ trợ AI ngay cả trong điều kiện ngoại tuyến. Xem các blog này để tìm hiểu sâu hơn về [Edge Intelligence với AWS](https://aws.amazon.com/blogs/iot/unlocking-real-time-intelligence-at-the-edge-with-awss-connected-edge-intelligence/) và [Thực hành Tốt nhất cho AI Tạo sinh và IoT tại edge](https://aws.amazon.com/blogs/iot/emerging-architecture-patterns-for-integrating-iot-and-generative-ai-on-aws/).

## AWS IoT SiteWise Assistant: Giải pháp Bản địa cho Tích hợp IoT Công nghiệp và AI Tạo sinh

Trong khi Amazon Bedrock cung cấp nền tảng linh hoạt cho bất kỳ nguồn dữ liệu IoT nào, AWS cũng cung cấp một giải pháp được xây dựng có mục đích cho các nhà sản xuất thiết bị công nghiệp sử dụng AWS IoT SiteWise cho các nhu cầu thu thập, lưu trữ và phân tích dữ liệu công nghiệp của họ. [AWS IoT SiteWise Assistant](https://aws.amazon.com/about-aws/whats-new/2024/11/aws-iot-sitewise-generative-ai-powered-industrial-assistant/) nâng cao khả năng của AWS IoT SiteWise bằng cách cho phép các truy vấn ngôn ngữ tự nhiên về dữ liệu máy của bạn thay vì cần viết các câu lệnh truy vấn kỹ thuật phức tạp để có được thông tin chi tiết về hiệu suất máy, xu hướng và số liệu hoạt động.

Để biết tổng quan chi tiết hơn, hãy xem [Chuyển đổi ra quyết định công nghiệp với AWS IoT SiteWise Assistant](https://aws.amazon.com/blogs/industries/transforming-industrial-decision-making-with-aws-iot-sitewise-assistant/).

## AI Tạo sinh trong Smart Machines được Kết nối với Đối tác AWS

Các Đối tác AWS đóng vai trò quan trọng trong việc hỗ trợ khách hàng AWS xây dựng các giải pháp máy thông minh, từ tư vấn chiến lược và ý tưởng đến cung cấp các giải pháp có thể mở rộng và an toàn tận dụng [Guidance for Deploying Smart Machines on AWS](https://aws.amazon.com/solutions/guidance/deploying-smart-machines-on-aws/). Trong phần này, chúng tôi đề cập đến cách một số Đối tác AWS tích hợp hệ thống (SI) này đang giúp khách hàng và thúc đẩy ngành công nghiệp máy thông minh rộng hơn với sự kết hợp của IoT và AI tạo sinh.

- [**Deloitte**](https://aws.amazon.com/partners/deloitte/) khai thác AI tạo sinh để cho phép bảo trì có hỗ trợ và ra quyết định tự chủ cho Smart Machines, tối ưu hóa cả hỗ trợ sau bán hàng và sự chuyển đổi sang Equipment-as-a-Service (EaaS).

- [**SoftServe**](https://partners.amazonaws.com/partners/001E000000e4HhNIAU/) [nền tảng IIoT](https://aws.amazon.com/marketplace/pp/prodview-tcq7u7n3bp6mg) thống nhất và [giải pháp AI tạo sinh](https://aws.amazon.com/marketplace/pp/prodview-uxeclu57sy2g6) kết hợp Industrial IoT (IIoT), AI tạo sinh, Digital Twins và khả năng NVIDIA để chuyển đổi Smart Machines. Triển khai Schunk của họ trao quyền cho các kỹ sư hỗ trợ từ xa và hiện trường khắc phục sự cố thiết bị của khách hàng một cách hiệu quả.

- [**Twisthink**](https://partners.amazonaws.com/partners/0010L00001jTjLpQAK/) hiện đang hỗ trợ [các trường hợp sử dụng Smart Machines](https://twisthink.com/event/webinar-revolutionize-smart-machines-with-aws-iot/) sử dụng AI tạo sinh cho bảo trì quy định và phân tích quản lý đội tàu với ít nỗ lực phát triển và đầu tư hơn.

- [**Green Custard**](https://www.green-custard.com/) kết hợp IoT và AI tạo sinh trên AWS để cách mạng hóa các dịch vụ Smart Machine của họ thông qua bảo trì có hỗ trợ, tối ưu hóa hiệu suất theo thời gian thực và hỗ trợ khách hàng nâng cao. Triển khai [Britvic's Aqua Libra Flavour Tap](https://www.green-custard.com/generative-ai-for-connected-products-service-and-support/) của họ chứng minh dịch vụ khách hàng được cải thiện thông qua phân tích thông minh dữ liệu IoT và tài liệu hỗ trợ.

## Kết luận

Kết hợp IoT và AI tạo sinh là sự chuyển đổi cho các nhà sản xuất máy thông minh, nâng cao hoạt động bảo trì, mở rộng quy trình quản lý đội tàu và tạo ra các nguồn doanh thu mới thông qua các ứng dụng mới cho khách hàng của bạn. AWS và Đối tác AWS cung cấp các dịch vụ và giải pháp để giúp các nhà sản xuất mở rộng các giải pháp IoT hiện tại của họ hoặc xây dựng các máy thông minh mới định vị các nhà sản xuất để duy trì cạnh tranh và thúc đẩy tăng trưởng doanh thu.

Sẵn sàng chuyển đổi sản phẩm của bạn với IoT và AI tạo sinh? Bắt đầu hành trình máy thông minh của bạn ngay hôm nay bằng cách [liên hệ với AWS](https://pages.awscloud.com/GLOBAL-ln-GC-A4IND-Contact-Us-interest.html) hoặc đối tác AWS của bạn. Để biết thêm thông tin về AI tạo sinh tại AWS, hãy xem các tài nguyên bên dưới:

- [Generative AI for Industrial](https://aws.amazon.com/industrial/generative-ai/)
- [Generative AI Innovation Center](https://aws.amazon.com/ai/generative-ai/innovation-center/)
- [Thực hành tốt nhất để xây dựng ứng dụng AI tạo sinh mạnh mẽ với Amazon Bedrock Agents](https://aws.amazon.com/blogs/machine-learning/best-practices-for-building-robust-generative-ai-applications-with-amazon-bedrock-agents-part-1/)
- [AWS Internet of Things](https://aws.amazon.com/iot/)

---

**Thẻ:** AWS IoT, aws manufacturing, Generative AI, Smart Machines

**Tác giả:**

- **Dimitrios Spiliopoulos** - Chuyên gia GTM IIoT Chính Toàn cầu tại AWS
- **Gabriel Verreault** - Kiến trúc sư Giải pháp Đối tác Cao cấp tại AWS cho phân khúc Sản xuất
- **Gary Emmerton** - Kiến trúc sư Giải pháp Cao cấp tại AWS có trụ sở tại Vương quốc Anh

**Nguồn:** [AWS for Industries Blog](https://aws.amazon.com/blogs/industries/maximizing-the-value-of-smart-machines-with-generative-ai-and-iot/)
