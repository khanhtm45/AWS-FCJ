---
title: "Announcing General Availability of the AWS SDK for Swift"
date: 2024-09-17
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Announcing General Availability of the AWS SDK for Swift

**by Josh Elkins | on 17 SEP 2024**

We are excited to announce the General Availability of the [AWS SDK for Swift](https://aws.amazon.com/sdk-for-swift/), the AWS solution for accessing Amazon Web Services from applications built with the Swift programming language. AWS SDK for Swift provides a modern, user-friendly, and native Swift interface for accessing Amazon Web Services from Apple platforms, AWS Lambda, and Linux-based [Swift on Server](https://www.swift.org/documentation/server/) applications.

AWS SDK for Swift [entered Developer Preview in 2021](https://aws.amazon.com/blogs/developer/announcing-new-aws-sdk-for-swift-alpha-release/) with the promise to bring a first-class, modern AWS experience to the Swift developer community. We're delighted that it is now emerging from Preview with a complete AWS SDK feature set comparable to that offered on AWS SDKs for other languages. AWS SDK for Swift is ready for you to use today in your own Swift-based applications, from Apple Watch to high-powered Linux and Mac servers.

Swift is the modern language of choice for developing natively on Apple devices, and is also widely used on Linux for server and utility purposes. AWS SDK for Swift allows app developers to add tight integration with AWS services into their native mobile and desktop apps. AWS SDK for Swift fully embraces modern Swift language features and provides access to AWS services with an interface that will feel natural to the Swift developer community.

## Quick Start

The following steps show how to create a simple Swift command line tool that uses the AWS Simple Token Service (STS) client included in AWS SDK for Swift. All you need is:

- a Mac with latest Xcode, or a Linux machine with Swift 5.9 or newer toolchain installed. See [swift.org's Getting Started guide](https://www.swift.org/getting-started/) if you don't already have Swift on your machine.
- AWS credentials and default AWS region configured on your machine, using the [AWS Command-Line Tools](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html).

In the Terminal, create a new Swift package:

```bash
$ mkdir MySwiftApp
$ cd MySwiftApp
$ swift package init --name MySwiftApp
```

Edit the `Package.swift` file to require the AWS SDK for Swift as a package dependency and add the AWS STS service client to your target:

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

Then, edit `Sources/MySwiftApp/MySwiftApp.swift` to create a client in code and use it to check your credentials with AWS STS:

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

Finally, run your Swift package from the terminal, and it will install dependencies, compile, and run:

```bash
$ swift run
...
Request succeeded
User ID: <your AWS user ID>
Account: <your AWS user account ID>
```

Consult the official AWS SDK for Swift [Getting Started guide](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/getting-started.html) for comprehensive, step-by-step instructions to integrate AWS SDK for Swift into your existing Swift package or Xcode application.

## Features

### Full Support for Swift Structured Concurrency

The AWS SDK for Swift utilizes [Swift Structured Concurrency](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/concurrency/) throughout for ease of use and efficient operation, both in public APIs and internally. No need for completion blocks and convoluted asynchronous control flow; Swift `async` / `await` on AWS operations makes it easy to write simple, concise, and correct asynchronous Swift code.

```swift
// Create a client for listing the current user's S3 buckets
let client = try await S3Client()

// Obtain a list of buckets.  Execution suspends while the request is made
// to AWS S3.
let input = ListBucketsInput()
let output = try await client.listBucketsV2(input: input)

// Once the request completes, execution continues and the buckets are printed.
print(output.buckets)
```

### Binary Data Streaming

The AWS SDK for Swift effortlessly streams binary data for both requests and responses. Data can be streamed either to or from a file or an in-memory buffer. The interface for streamed binary data uses a Swift [AsyncSequence](https://developer.apple.com/documentation/swift/asyncsequence) to easily and efficiently transfer large binary payloads in the form of small, sequential chunks of data.

In the following example, a large file is streamed to AWS S3 from a file on the local filesystem.

```swift
// Create a S3 client and a Foundation file handle referring to a local data file.
let client = try await S3Client()
let fileHandle = FileHandle(forReadingAtPath: "/tmp/my-local-file")!

// Create a stream with the file handle, and use it as the body of a S3 PutObject
// request to create a new S3 object named my-new-file.
let stream = FileStream(fileHandle: fileHandle)
let body = ByteStream.stream(stream)
let input = PutObjectInput(body: body, bucket: "amzn-s3-demo-bucket", key: "my-new-file")

// Stream the data in the local file to AWS S3 and store it in a new object.
// If the file is large, AWS SDK for Swift will stream it in chunks until it
// has all been transferred.
let _ = try await client.putObject(input: input)
```

### Event Streaming

The AWS SDK for Swift also supports AWS event streaming. Event streams enable asynchronous transmission of discrete, serialized messages ("events") over the network. Event streams can be either unidirectional, or with HTTP/2, bidirectional. Like binary data streams, event streams are delivered by a Swift [AsyncSequence](https://developer.apple.com/documentation/swift/asyncsequence) for easy consumption by the caller.

In the following bidirectional streaming example, the AWS Transcribe Streaming service is used to stream audio to the server while transcription events are returned in real-time.

```swift
// Create a TranscribeStreaming client and prepare audio for transmission.
let client = try await TranscribeStreamingClient()
let input = StartStreamTranscriptionInput(audioStream: audioStream,
                                          languageCode: .enUs,
                                          mediaEncoding: .pcm,
                                          mediaSampleRateHertz: 8000)

// Start the transcription request.  An HTTP/2 connection will be opened.
// Audio data will be streamed to the server while the server simultaneously
// streams transcription events back as words are transcribed from the audio.
let output = try await client.startStreamTranscription(input: input)
for try await event in output.transcriptResultStream! {
    print(event)
 }
```

Consult the [documentation](https://docs.aws.amazon.com/) for individual AWS services to see which services support event streaming.

### Waiters

[Waiters](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/using-waiters.html) allow the AWS SDK for Swift to suspend and wait for an expected service condition to occur, such as the creation or deletion of a resource, and automatically resume execution once the condition has been satisfied.

In the following example, the AWS SDK for Swift is used to wait until a previously created EC2 instance reaches the Running state.

```swift
// An EC2 instance was previously created & started with the ID i-05450a63fe8ae3329.
// The instance may take some time before it transitions to running.

// We want to wait until our instance is running before continuing execution.
let input = DescribeInstancesInput(instanceIds: ["i-05450a63fe8ae3329"])

// We want to wait no longer than 240 seconds (four minutes) for the instance to
// reach the Running state.
let options = WaiterOptions(maxWaitTime: 240.0)

// This method call will suspend the calling thread, intermittently poll the EC2
// instance to check its state, and will resume execution once the instance
// reports that it is running.
//
// If the maximum wait time is reached or an unexpected error is encountered while
// polling, then this method call will throw an appropriate error back to the
// caller.
let client = try await EC2Client()
let _ = try await client.waitUntilInstanceRunning(options: options, input: input)

// Once this point is reached, the instance is now verified to be running.
```

Many AWS operations support waiters. Consult the [documentation](https://docs.aws.amazon.com/) for individual AWS services for more details.

### Paginators

Paginators are a feature that allows the caller to automatically retrieve large sets of data in pages, without writing code to perform each individual page retrieval.

Paginated operations return individual pages of data using a Swift [AsyncSequence](https://developer.apple.com/documentation/swift/asyncsequence) of discrete-sized pages of data.

In the following example, AWS SDK for Swift uses pagination to retrieve the list of contents of a S3 bucket containing a very large number of objects.

```swift
// Create a S3 client and define the bucket you want to list
let client = try await S3Client()
let input = ListObjectsV2Input(bucket: "amzn-s3-demo-bucket")

// Get an asynchronous sequence with pages of the bucket's contents
let output = client.listObjectsV2Paginated(input: input)

// Iterate over the sequence with a loop to get the contents a page at a time
for try await page in output {
    print(page.contents)
}
```

Many AWS operations support pagination of their results. Consult the [documentation](https://docs.aws.amazon.com/) for individual AWS services for more details.

### Automatic Retry

The AWS SDK for Swift is configured by default with [automatic retry](https://docs.aws.amazon.com/sdkref/latest/guide/feature-retry-behavior.html), ensuring that failed AWS requests are retried when transient network or server conditions cause recoverable errors. Retry may be [customized](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/using-retry.html) by configuring parameters, or for greater control, by providing a custom retry strategy.

### Flexible HTTP Client Options

AWS SDK for Swift is supplied with two fully-featured and highly configurable HTTP clients, to provide the right HTTP networking support across all supported platforms:

- A cross-platform HTTP client based on [AWS's Common Runtime (CRT) libraries](https://docs.aws.amazon.com/sdkref/latest/guide/common-runtime.html) that provides high performance and stability, even in challenging network conditions. Ideal for server-side and high-throughput Mac applications.
- A HTTP client based on the Apple Foundation library's [URLSession](https://developer.apple.com/documentation/foundation/urlsession) HTTP connection manager, for the best performance, power conservation and tight platform integration on Apple devices.

Both clients support all AWS service features and are highly configurable to meet your application's needs.

Based on customer feedback, additional HTTP clients may be provided in the future.

### Other Features

The AWS SDK for Swift provides everything a developer needs to fully integrate their application with their AWS services.

- **Interceptors**: Interceptors allow for full customization of request & response handling by injecting code into the request lifecycle.
- [**Logging**](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/using-testing-debugging.html#using-logging): Fine-grained control over logging to any [swift-log](https://github.com/apple/swift-log) compatible logger.
- **Observability**: AWS SDK for Swift is provided with support for detailed metrics and tracing. You can provide a plug-in to forward data into Amazon CloudWatch or other backend collection systems.

## Supported Tools & Platforms

AWS SDK for Swift supports multiple development environments:

- Xcode 15.0 and higher on Mac. Xcode is available from the [Mac App Store](https://apps.apple.com/us/app/xcode/id497799835?mt=12).
- Swift 5.9 or higher on Linux. Swift for Linux is available for install on [swift.org](https://www.swift.org/install/linux/#platforms).

AWS SDK for Swift compiles to the following platforms & minimum OS versions:

- macOS 10.15
- iOS / iPadOS 13
- tvOS 13
- watchOS 9
- visionOS 1
- Amazon Linux 2
- Ubuntu 20.04

## What's Next

We're excited to see what you'll build with AWS SDK for Swift, and we're here to help you integrate it into your app successfully. The following are some next steps to get you started on the right foot:

- Please consult our [Getting Started guide](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/getting-started.html) for detailed, step-by-step instructions on how to integrate AWS SDK for Swift into your own Swift package or Xcode application.
- Code for the AWS SDK for Swift is open-source and is [available on Github](https://github.com/awslabs/aws-sdk-swift).
- If you have questions about AWS SDK for Swift or have a request or suggestion, you can [start a discussion](https://github.com/awslabs/aws-sdk-swift/discussions) on our Github page. If you believe you've found a bug, you can [file an issue](https://github.com/awslabs/aws-sdk-swift/issues) as well.
- Complete AWS SDK for Swift setup instructions, code samples, and more are [available in the AWS SDK for Swift Developer Guide](https://docs.aws.amazon.com/sdk-for-swift/latest/developer-guide/home.html).
- Comprehensive documentation for the entire range of AWS services is [available on the main AWS Documentation site](https://docs.aws.amazon.com/).

---

**Tags:** aws-sdk, Swift

**Author:** Josh Elkins - Josh is a software developer for the AWS SDK for Swift.

**Source:** [AWS Developer Tools Blog](https://aws.amazon.com/blogs/developer/announcing-general-availability-of-the-aws-sdk-for-swift/)
