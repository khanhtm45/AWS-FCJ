---
title: "Announcing the Developer Preview of DynamoDB Mapper for Kotlin"
date: 2024-10-30
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Announcing the Developer Preview of DynamoDB Mapper for Kotlin

**by Ian Botsford | on 30 OCT 2024**

We're excited to announce the Developer Preview of [DynamoDB Mapper for Kotlin](https://docs.aws.amazon.com/sdk-for-kotlin/latest/developer-guide/ddb-mapper.html). This high-level library provides streamlined, idiomatic ways for developers to map data between their business logic written in Kotlin and their tables in DynamoDB. DynamoDB Mapper works with most Kotlin data classes right out of the box and also offers powerful features for modeling data flexibly and handling more complex schemas. DynamoDB Mapper is part of the [AWS SDK for Kotlin](https://aws.amazon.com/sdk-for-kotlin/) and will be released on the same daily schedule as other SDK components.

You can test out this new feature by using the DynamoDB Mapper Schema Generator plugin for Gradle and annotating your data classes:

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

The preceding code sample will automatically generate item schemas at build time. These schemas may then be used to access DynamoDB table items as `Planet` instances as shown in the following code:

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

// Write the `saturn` object to the planets table
planetsTable.putItem { item = saturn }

// Get a Planet instance from an item with the key "Jupiter"
val jupiter = planetsTable.getItem("Jupiter").item

println(jupiter)
// Prints "Planet(name=Jupiter, radiusKilometers=71492.0, ...)"
```

## Preview functionality

This DynamoDB Mapper is being released as a Developer Preview, meaning it is not yet feature complete, may contain bugs, and is not suitable for production workloads. The goal of this Developer Preview is to gather early feedback from eager adopters, which may lead to redesigns and backwards-incompatible changes. See the [AWS SDKs and Tools maintenance policy](https://docs.aws.amazon.com/sdkref/latest/guide/maint-policy.html#version-life-cycle) for more details on product lifecycle.

The initial Developer Preview supports the following DynamoDB operations:

- `deleteItem`
- `getItem`
- `putItem`
- `queryPaginated`
- `scanPaginated`

It also supports the following types of DynamoDB expressions:

- Filter expressions
- Key condition expressions

Support for more operations such as `updateItem` and `createTable`, along with support for more types of expressions such as update expressions and projection expressions, will be added before DynamoDB Mapper exits Developer Preview.

## Next steps

To get started with the DynamoDB Mapper for Kotlin, check out the following links:

- [Getting started guide](https://docs.aws.amazon.com/sdk-for-kotlin/latest/developer-guide/ddb-mapper.html)
- [API reference documentation](https://sdk.amazonaws.com/kotlin/api/latest/dynamodb-mapper/aws.sdk.kotlin.hll.dynamodbmapper/index.html)
- [Our GitHub repository](https://github.com/awslabs/aws-sdk-kotlin)

Let us know how this new feature works for you and whether it meets your needs. If you are curious about something, post or join [a discussion in our GitHub repo](https://github.com/awslabs/aws-sdk-kotlin/discussions). If you've found a bug, please [file an issue in our GitHub repo](https://github.com/awslabs/aws-sdk-kotlin/issues/new/choose).

---

**Tags:** Amazon DynamoDB, aws-sdk, Kotlin, SDK

**Author:** Ian Botsford - Ian is a developer working on the AWS SDK for Kotlin. He is passionate about making AWS easy to use through fluent, idiomatic SDKs. You can find him on GitHub at [@ianbotsf](https://github.com/ianbotsf).

**Source:** [AWS Developer Tools Blog](https://aws.amazon.com/blogs/developer/announcing-dev-preview-of-dynamodb-mapper-for-kotlin/)
