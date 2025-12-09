---
title: "Công bố Phát hành Chính thức của AWS SDK cho Swift"
date: 2024-09-17
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Công bố Phát hành Chính thức của AWS SDK cho Swift

**Tác giả: Josh Elkins | ngày 17 tháng 9 năm 2024**

Chúng tôi vui mừng thông báo về việc Phát hành Chính thức của [AWS SDK cho Swift](https://aws.amazon.com/sdk-for-swift/), giải pháp AWS để truy cập Amazon Web Services từ các ứng dụng được xây dựng bằng ngôn ngữ lập trình Swift. AWS SDK cho Swift cung cấp một giao diện Swift hiện đại, thân thiện với người dùng và bản địa để truy cập Amazon Web Services từ các nền tảng Apple, AWS Lambda và các ứng dụng [Swift trên Server](https://www.swift.org/documentation/server/) dựa trên Linux.

AWS SDK cho Swift [bắt đầu Bản Xem trước Dành cho Nhà phát triển vào năm 2021](https://aws.amazon.com/blogs/developer/announcing-new-aws-sdk-for-swift-alpha-release/) với lời hứa mang đến trải nghiệm AWS hạng nhất, hiện đại cho cộng đồng nhà phát triển Swift. Chúng tôi rất vui mừng khi nó hiện đang ra khỏi Bản Xem trước với bộ tính năng AWS SDK đầy đủ tương đương với những gì được cung cấp trên AWS SDK cho các ngôn ngữ khác. AWS SDK cho Swift đã sẵn sàng để bạn sử dụng ngay hôm nay trong các ứng dụng dựa trên Swift của riêng bạn, từ Apple Watch đến các máy chủ Linux và Mac mạnh mẽ.

Swift là ngôn ngữ hiện đại được lựa chọn để phát triển bản địa trên các thiết bị Apple và cũng được sử dụng rộng rãi trên Linux cho các mục đích máy chủ và tiện ích. AWS SDK cho Swift cho phép các nhà phát triển ứng dụng thêm tích hợp chặt chẽ với các dịch vụ AWS vào các ứng dụng di động và máy tính để bàn bản địa của họ. AWS SDK cho Swift hoàn toàn sử dụng các tính năng ngôn ngữ Swift hiện đại và cung cấp quyền truy cập vào các dịch vụ AWS với giao diện sẽ cảm thấy tự nhiên đối với cộng đồng nhà phát triển Swift.

## Bắt đầu Nhanh

Các bước sau đây cho thấy cách tạo một công cụ dòng lệnh Swift đơn giản sử dụng client AWS Simple Token Service (STS) được bao gồm trong AWS SDK cho Swift. Tất cả những gì bạn cần là:

- một Mac với Xcode mới nhất, hoặc một máy Linux với Swift 5.9 hoặc bộ công cụ mới hơn được cài đặt. Xem [hướng dẫn Bắt đầu của swift.org](https://www.swift.org/getting-started/) nếu bạn chưa có Swift trên máy của mình.
- Thông tin xác thực AWS và vùng AWS mặc định được cấu hình trên máy của bạn, sử dụng [AWS Command-Line Tools](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html).

Trong Terminal, tạo một gói Swift mới:

```bash
$ mkdir MySwiftApp
$ cd MySwiftApp
$ swift package init --name MySwiftApp
```

Chỉnh sửa tệp `Package.swift` để yêu cầu AWS SDK cho Swift làm phụ thuộc gói và thêm client dịch vụ AWS STS vào target của bạn:

```swift
// swift-tools-version: 5.9

import PackageDescription

let package = Package(
    name: "MySwiftApp",
    platforms: [.macOS(.v10_15)],
    dependencies: [
        .package(url: "https://github.com/awslabs/aws-sdk-swift.git", from: "1.0.0")
    ],
    targets: [
        .executableTarget(name: "MySwiftApp", dependencies: [
            .product(name: "AWSSTS", package: "aws-sdk-swift")
        ])
    ]
)
```

Sau đó, chỉnh sửa `Sources/MySwiftApp/MySwiftApp.swift` để tạo một client trong code và sử dụng nó để kiểm tra thông tin xác thực của bạn với AWS STS:

```swift
import AWSSTS

@main
struct MySwiftApp {

    static func main() async throws {
        let client = try await STSClient()
        let input = GetCallerIdentityInput()
        let output = try await client.getCallerIdentity(input: input)
        print("Request succeeded")
        print("User ID: \(output.userId)")
        print("Account: \(output.account)")
    }
}
```

Cuối cùng, chạy gói Swift của bạn từ terminal, và nó sẽ cài đặt các phụ thuộc, biên dịch và chạy:

```bash
$ swift run
...
Request succeeded
User ID: <your AWS user ID>
Account: <your AWS user account ID>
```

Tham khảo [hướng dẫn Bắt đầu](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/getting-started.html) chính thức của AWS SDK cho Swift để có hướng dẫn từng bước toàn diện để tích hợp AWS SDK cho Swift vào gói Swift hoặc ứng dụng Xcode hiện có của bạn.

## Các Tính năng

### Hỗ trợ Đầy đủ cho Swift Structured Concurrency

AWS SDK cho Swift sử dụng [Swift Structured Concurrency](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/concurrency/) xuyên suốt để dễ sử dụng và hoạt động hiệu quả, cả trong các API công khai và nội bộ. Không cần các khối hoàn thành và luồng điều khiển không đồng bộ phức tạp; Swift `async` / `await` trên các thao tác AWS giúp dễ dàng viết code Swift không đồng bộ đơn giản, ngắn gọn và chính xác.

```swift
// Tạo một client để liệt kê các S3 bucket của người dùng hiện tại
let client = try await S3Client()

// Lấy danh sách các bucket. Việc thực thi tạm dừng trong khi yêu cầu được thực hiện
// đến AWS S3.
let input = ListBucketsInput()
let output = try await client.listBucketsV2(input: input)

// Sau khi yêu cầu hoàn tất, việc thực thi tiếp tục và các bucket được in ra.
print(output.buckets)
```

### Streaming Dữ liệu Nhị phân

AWS SDK cho Swift dễ dàng streaming dữ liệu nhị phân cho cả yêu cầu và phản hồi. Dữ liệu có thể được streaming từ hoặc đến một tệp hoặc bộ đệm trong bộ nhớ. Giao diện cho dữ liệu nhị phân được streaming sử dụng Swift [AsyncSequence](https://developer.apple.com/documentation/swift/asyncsequence) để dễ dàng và hiệu quả truyền tải các payload nhị phân lớn dưới dạng các khối dữ liệu tuần tự nhỏ.

Trong ví dụ sau, một tệp lớn được streaming đến AWS S3 từ một tệp trên hệ thống tệp cục bộ.

```swift
// Tạo một client S3 và một file handle Foundation tham chiếu đến một tệp dữ liệu cục bộ.
let client = try await S3Client()
let fileHandle = FileHandle(forReadingAtPath: "/tmp/my-local-file")!

// Tạo một stream với file handle và sử dụng nó làm body của một yêu cầu S3 PutObject
// để tạo một đối tượng S3 mới có tên my-new-file.
let stream = FileStream(fileHandle: fileHandle)
let body = ByteStream.stream(stream)
let input = PutObjectInput(body: body, bucket: "amzn-s3-demo-bucket", key: "my-new-file")

// Stream dữ liệu trong tệp cục bộ đến AWS S3 và lưu trữ nó trong một đối tượng mới.
// Nếu tệp lớn, AWS SDK cho Swift sẽ streaming nó theo từng khối cho đến khi
// tất cả đã được truyền tải.
let _ = try await client.putObject(input: input)
```

### Event Streaming

AWS SDK cho Swift cũng hỗ trợ AWS event streaming. Event stream cho phép truyền tải không đồng bộ các thông điệp tuần tự, rời rạc ("events") qua mạng. Event stream có thể là một chiều, hoặc với HTTP/2, hai chiều. Giống như binary data stream, event stream được cung cấp bởi Swift [AsyncSequence](https://developer.apple.com/documentation/swift/asyncsequence) để dễ dàng sử dụng.

Trong ví dụ streaming hai chiều sau, dịch vụ AWS Transcribe Streaming được sử dụng để streaming âm thanh đến máy chủ trong khi các sự kiện phiên âm được trả về theo thời gian thực.

```swift
// Tạo một TranscribeStreaming client và chuẩn bị âm thanh để truyền tải.
let client = try await TranscribeStreamingClient()
let input = StartStreamTranscriptionInput(audioStream: audioStream,
                                          languageCode: .enUs,
                                          mediaEncoding: .pcm,
                                          mediaSampleRateHertz: 8000)

// Bắt đầu yêu cầu phiên âm. Một kết nối HTTP/2 sẽ được mở.
// Dữ liệu âm thanh sẽ được streaming đến máy chủ trong khi máy chủ đồng thời
// streaming các sự kiện phiên âm trở lại khi các từ được phiên âm từ âm thanh.
let output = try await client.startStreamTranscription(input: input)
for try await event in output.transcriptResultStream! {
    print(event)
 }
```

Tham khảo [tài liệu](https://docs.aws.amazon.com/) cho từng dịch vụ AWS để xem dịch vụ nào hỗ trợ event streaming.

### Waiters

[Waiters](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/using-waiters.html) cho phép AWS SDK cho Swift tạm dừng và đợi một điều kiện dịch vụ mong đợi xảy ra, chẳng hạn như việc tạo hoặc xóa một tài nguyên, và tự động tiếp tục thực thi sau khi điều kiện được đáp ứng.

Trong ví dụ sau, AWS SDK cho Swift được sử dụng để đợi cho đến khi một instance EC2 đã được tạo trước đó đạt trạng thái Running.

```swift
// Một instance EC2 đã được tạo và khởi động trước đó với ID i-05450a63fe8ae3329.
// Instance có thể mất một thời gian trước khi nó chuyển sang running.

// Chúng ta muốn đợi cho đến khi instance của chúng ta đang chạy trước khi tiếp tục thực thi.
let input = DescribeInstancesInput(instanceIds: ["i-05450a63fe8ae3329"])

// Chúng ta muốn đợi không quá 240 giây (bốn phút) để instance
// đạt trạng thái Running.
let options = WaiterOptions(maxWaitTime: 240.0)

// Lệnh gọi phương thức này sẽ tạm dừng luồng gọi, kiểm tra định kỳ instance EC2
// để kiểm tra trạng thái của nó, và sẽ tiếp tục thực thi sau khi instance
// báo cáo rằng nó đang chạy.
let client = try await EC2Client()
let _ = try await client.waitUntilInstanceRunning(options: options, input: input)

// Sau khi đạt đến điểm này, instance hiện được xác minh là đang chạy.
```

Nhiều thao tác AWS hỗ trợ waiter. Tham khảo [tài liệu](https://docs.aws.amazon.com/) cho từng dịch vụ AWS để biết thêm chi tiết.

### Paginators

Paginator là một tính năng cho phép người gọi tự động truy xuất các tập dữ liệu lớn theo từng trang, mà không cần viết code để thực hiện từng truy xuất trang riêng lẻ.

Các thao tác được phân trang trả về các trang dữ liệu riêng lẻ bằng Swift [AsyncSequence](https://developer.apple.com/documentation/swift/asyncsequence) của các trang dữ liệu có kích thước rời rạc.

Trong ví dụ sau, AWS SDK cho Swift sử dụng phân trang để truy xuất danh sách nội dung của một S3 bucket chứa số lượng đối tượng rất lớn.

```swift
// Tạo một S3 client và xác định bucket bạn muốn liệt kê
let client = try await S3Client()
let input = ListObjectsV2Input(bucket: "amzn-s3-demo-bucket")

// Nhận một chuỗi không đồng bộ với các trang nội dung của bucket
let output = client.listObjectsV2Paginated(input: input)

// Lặp qua chuỗi bằng một vòng lặp để lấy nội dung từng trang một
for try await page in output {
    print(page.contents)
}
```

Nhiều thao tác AWS hỗ trợ phân trang kết quả của chúng. Tham khảo [tài liệu](https://docs.aws.amazon.com/) cho từng dịch vụ AWS để biết thêm chi tiết.

### Thử lại Tự động

AWS SDK cho Swift được cấu hình mặc định với [thử lại tự động](https://docs.aws.amazon.com/sdkref/latest/guide/feature-retry-behavior.html), đảm bảo rằng các yêu cầu AWS không thành công được thử lại khi các điều kiện mạng tạm thời hoặc máy chủ gây ra lỗi có thể khôi phục. Thử lại có thể được [tùy chỉnh](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/using-retry.html) bằng cách cấu hình các tham số, hoặc để kiểm soát nhiều hơn, bằng cách cung cấp một chiến lược thử lại tùy chỉnh.

### Tùy chọn HTTP Client Linh hoạt

AWS SDK cho Swift được cung cấp với hai HTTP client đầy đủ tính năng và có thể cấu hình cao, để cung cấp hỗ trợ mạng HTTP phù hợp trên tất cả các nền tảng được hỗ trợ:

- Một HTTP client đa nền tảng dựa trên [thư viện Common Runtime (CRT) của AWS](https://docs.aws.amazon.com/sdkref/latest/guide/common-runtime.html) cung cấp hiệu suất cao và ổn định, ngay cả trong điều kiện mạng khó khăn. Lý tưởng cho các ứng dụng Mac phía máy chủ và thông lượng cao.
- Một HTTP client dựa trên trình quản lý kết nối HTTP [URLSession](https://developer.apple.com/documentation/foundation/urlsession) của thư viện Apple Foundation, để có hiệu suất tốt nhất, bảo tồn năng lượng và tích hợp nền tảng chặt chẽ trên các thiết bị Apple.

Cả hai client đều hỗ trợ tất cả các tính năng dịch vụ AWS và có thể cấu hình cao để đáp ứng nhu cầu của ứng dụng bạn.

Dựa trên phản hồi của khách hàng, các HTTP client bổ sung có thể được cung cấp trong tương lai.

### Các Tính năng Khác

AWS SDK cho Swift cung cấp mọi thứ mà nhà phát triển cần để tích hợp đầy đủ ứng dụng của họ với các dịch vụ AWS.

- **Interceptors**: Interceptor cho phép tùy chỉnh hoàn toàn việc xử lý yêu cầu và phản hồi bằng cách chèn code vào vòng đời yêu cầu.
- [**Logging**](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/using-testing-debugging.html#using-logging): Kiểm soát chi tiết về logging cho bất kỳ logger tương thích [swift-log](https://github.com/apple/swift-log) nào.
- **Observability**: AWS SDK cho Swift được cung cấp với hỗ trợ cho các số liệu và truy vết chi tiết. Bạn có thể cung cấp một plug-in để chuyển tiếp dữ liệu vào Amazon CloudWatch hoặc các hệ thống thu thập backend khác.

## Công cụ & Nền tảng Được hỗ trợ

AWS SDK cho Swift hỗ trợ nhiều môi trường phát triển:

- Xcode 15.0 trở lên trên Mac. Xcode có sẵn từ [Mac App Store](https://apps.apple.com/us/app/xcode/id497799835?mt=12).
- Swift 5.9 trở lên trên Linux. Swift cho Linux có sẵn để cài đặt trên [swift.org](https://www.swift.org/install/linux/#platforms).

AWS SDK cho Swift biên dịch cho các nền tảng và phiên bản hệ điều hành tối thiểu sau:

- macOS 10.15
- iOS / iPadOS 13
- tvOS 13
- watchOS 9
- visionOS 1
- Amazon Linux 2
- Ubuntu 20.04

## Các Bước Tiếp theo

Chúng tôi rất vui mừng được thấy những gì bạn sẽ xây dựng với AWS SDK cho Swift, và chúng tôi ở đây để giúp bạn tích hợp nó vào ứng dụng của bạn một cách thành công. Sau đây là một số bước tiếp theo để giúp bạn bắt đầu đúng hướng:

- Vui lòng tham khảo [hướng dẫn Bắt đầu](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/getting-started.html) của chúng tôi để có hướng dẫn chi tiết, từng bước về cách tích hợp AWS SDK cho Swift vào gói Swift hoặc ứng dụng Xcode của riêng bạn.
- Code cho AWS SDK cho Swift là mã nguồn mở và [có sẵn trên Github](https://github.com/awslabs/aws-sdk-swift).
- Nếu bạn có câu hỏi về AWS SDK cho Swift hoặc có yêu cầu hoặc đề xuất, bạn có thể [bắt đầu thảo luận](https://github.com/awslabs/aws-sdk-swift/discussions) trên trang Github của chúng tôi. Nếu bạn tin rằng bạn đã tìm thấy lỗi, bạn cũng có thể [gửi issue](https://github.com/awslabs/aws-sdk-swift/issues).
- Hướng dẫn cài đặt AWS SDK cho Swift đầy đủ, các mẫu code và nhiều hơn nữa [có sẵn trong Hướng dẫn Nhà phát triển AWS SDK cho Swift](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/home.html).
- Tài liệu toàn diện cho toàn bộ các dịch vụ AWS [có sẵn trên trang Tài liệu AWS chính](https://docs.aws.amazon.com/).

---

**Thẻ:** aws-sdk, Swift

**Tác giả:** Josh Elkins - Josh là một nhà phát triển phần mềm cho AWS SDK cho Swift.

**Nguồn:** [AWS Developer Tools Blog](https://aws.amazon.com/blogs/developer/announcing-general-availability-of-the-aws-sdk-for-swift/)
