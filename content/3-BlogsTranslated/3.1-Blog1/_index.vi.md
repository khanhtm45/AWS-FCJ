---
title: "Công bố Bản Xem trước Dành cho Nhà phát triển của DynamoDB Mapper cho Kotlin"
date: 2024-10-30
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Công bố Bản Xem trước Dành cho Nhà phát triển của DynamoDB Mapper cho Kotlin

**Tác giả: Ian Botsford | ngày 30 tháng 10 năm 2024**

Chúng tôi vui mừng thông báo về Bản Xem trước Dành cho Nhà phát triển của [DynamoDB Mapper cho Kotlin](https://docs.aws.amazon.com/sdk-for-kotlin/latest/developer-guide/ddb-mapper.html). Thư viện cấp cao này cung cấp các cách thức hợp lý và tự nhiên cho các nhà phát triển ánh xạ dữ liệu giữa logic nghiệp vụ của họ được viết bằng Kotlin và các bảng của họ trong DynamoDB. DynamoDB Mapper hoạt động với hầu hết các data class Kotlin ngay từ đầu và cũng cung cấp các tính năng mạnh mẽ để mô hình hóa dữ liệu linh hoạt và xử lý các schema phức tạp hơn. DynamoDB Mapper là một phần của [AWS SDK cho Kotlin](https://aws.amazon.com/sdk-for-kotlin/) và sẽ được phát hành theo cùng lịch trình hàng ngày như các thành phần SDK khác.

Bạn có thể thử nghiệm tính năng mới này bằng cách sử dụng plugin DynamoDB Mapper Schema Generator cho Gradle và chú thích các data class của bạn:

```kotlin
@DynamoDbItem
data class Planet(
    @DynamoDbPartitionKey
    val name: String,

    val radiusKilometers: Double,
    val atmosphericGasses: List<String>,
    val hasRings: Boolean,
    val numberOfMoons: Int,
)
```

Đoạn code mẫu trên sẽ tự động tạo các item schema tại thời điểm build. Các schema này sau đó có thể được sử dụng để truy cập các item trong bảng DynamoDB dưới dạng các instance `Planet` như được trình bày trong đoạn code sau:

```kotlin
val client = DynamoDbClient.fromEnvironment()
val mapper = DynamoDbMapper(client)
val planetsTable = mapper.getTable("all-planets", PlanetSchema)

val saturn = Planet(
    name = "Saturn",
    radiusKilometers = 60268.0,
    atmosphericGasses = listOf("hydrogen", "helium", "methane"),
    hasRings = true,
    numberOfMoons = 146,
)

// Ghi đối tượng `saturn` vào bảng planets
planetsTable.putItem { item = saturn }

// Lấy một instance Planet từ một item có key là "Jupiter"
val jupiter = planetsTable.getItem("Jupiter").item

println(jupiter)
// In ra "Planet(name=Jupiter, radiusKilometers=71492.0, ...)"
```

## Chức năng Xem trước

DynamoDB Mapper này đang được phát hành dưới dạng Bản Xem trước Dành cho Nhà phát triển, nghĩa là nó chưa hoàn thiện đầy đủ tính năng, có thể chứa lỗi và không phù hợp cho các khối lượng công việc sản xuất. Mục tiêu của Bản Xem trước Dành cho Nhà phát triển này là thu thập phản hồi sớm từ những người áp dụng nhiệt tình, điều này có thể dẫn đến việc thiết kế lại và thay đổi không tương thích ngược. Xem [chính sách bảo trì AWS SDK và Công cụ](https://docs.aws.amazon.com/sdkref/latest/guide/maint-policy.html#version-life-cycle) để biết thêm chi tiết về vòng đời sản phẩm.

Bản Xem trước Dành cho Nhà phát triển ban đầu hỗ trợ các thao tác DynamoDB sau:

- `deleteItem`
- `getItem`
- `putItem`
- `queryPaginated`
- `scanPaginated`

Nó cũng hỗ trợ các loại biểu thức DynamoDB sau:

- Biểu thức lọc (Filter expressions)
- Biểu thức điều kiện khóa (Key condition expressions)

Hỗ trợ cho nhiều thao tác hơn như `updateItem` và `createTable`, cùng với hỗ trợ cho nhiều loại biểu thức hơn như biểu thức cập nhật (update expressions) và biểu thức chiếu (projection expressions), sẽ được thêm vào trước khi DynamoDB Mapper thoát khỏi Bản Xem trước Dành cho Nhà phát triển.

## Các bước tiếp theo

Để bắt đầu với DynamoDB Mapper cho Kotlin, hãy xem các liên kết sau:

- [Hướng dẫn bắt đầu](https://docs.aws.amazon.com/sdk-for-kotlin/latest/developer-guide/ddb-mapper.html)
- [Tài liệu tham khảo API](https://sdk.amazonaws.com/kotlin/api/latest/dynamodb-mapper/aws.sdk.kotlin.hll.dynamodbmapper/index.html)
- [Kho lưu trữ GitHub của chúng tôi](https://github.com/awslabs/aws-sdk-kotlin)

Hãy cho chúng tôi biết tính năng mới này hoạt động như thế nào đối với bạn và liệu nó có đáp ứng nhu cầu của bạn hay không. Nếu bạn tò mò về điều gì đó, hãy đăng hoặc tham gia [thảo luận trong kho GitHub của chúng tôi](https://github.com/awslabs/aws-sdk-kotlin/discussions). Nếu bạn tìm thấy lỗi, vui lòng [gửi issue trong kho GitHub của chúng tôi](https://github.com/awslabs/aws-sdk-kotlin/issues/new/choose).

---

**Thẻ:** Amazon DynamoDB, aws-sdk, Kotlin, SDK

**Tác giả:** Ian Botsford - Ian là nhà phát triển làm việc trên AWS SDK cho Kotlin. Anh ấy đam mê làm cho AWS dễ sử dụng thông qua các SDK trôi chảy và tự nhiên. Bạn có thể tìm thấy anh ấy trên GitHub tại [@ianbotsf](https://github.com/ianbotsf).

**Nguồn:** [AWS Developer Tools Blog](https://aws.amazon.com/blogs/developer/announcing-dev-preview-of-dynamodb-mapper-for-kotlin/)
