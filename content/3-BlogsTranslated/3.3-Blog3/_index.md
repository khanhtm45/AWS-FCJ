---
title: "Maximizing the value of Smart Machines with generative AI and IoT"
date: 2025-07-11
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Maximizing the value of Smart Machines with generative AI and IoT

**by Dimitrios Spiliopoulos, Gabriel Verreault, and Gary Emmerton | on 11 JUL 2025**

In today's competitive industrial landscape, providers of industrial machines, such as construction and mining equipment, and factory machinery, look for innovative ways to maximize the potential of their products. By connecting these machines to the cloud with IoT, machine builders gain visibility into how their equipment performs in real-world conditions—understanding utilization patterns, identifying recurring failure modes, and discovering optimization opportunities that drive both equipment improvements and new service offerings.

Building a comprehensive machine-to-cloud connected solution can be complex and time-consuming. In the blog [Building Smart Industrial Machines with AWS: A Comprehensive Guide](https://aws.amazon.com/blogs/iot/building-smart-industrial-machines-with-aws-iot-a-comprehensive-guide/), we demonstrated how AWS IoT services enable secure, scalable industrial solutions without extensive infrastructure investment. In this blog, we will explore the transformative potential of combining generative AI with IoT for Smart Machines with a focus on how equipment manufacturers can leverage these capabilities in conjunction to revolutionize industrial operations, create new insights, and drive tangible business outcomes leveraging AWS generative AI services, like [Amazon Bedrock](https://aws.amazon.com/bedrock/), combined with AWS IoT services, like [AWS IoT Core](https://aws.amazon.com/iot-core/) and [AWS IoT SiteWise](https://aws.amazon.com/iot-sitewise/).

## Generative AI for Smart Machines

[Generative AI](https://aws.amazon.com/what-is/generative-ai/) can drive significant innovation in industrial use cases by drawing actionable insights from operational and product data. They empower machine operators or service engineers to resolve issues faster, consistently, and repeatably. According to [research from Capgemini](https://prod.ucwe.capgemini.com/wp-content/uploads/2023/07/Final-Web-Version-Report-Harnessing-the-Value-of-Gen-AI.1.pdf), a majority of manufacturers are not just curious about generative AI; 55% are actively exploring its potential and 45% are currently working on pilot projects.

AWS and AWS Partners make it easier for companies to build and scale generative AI-based applications effectively. We will explore four Smart Machines use cases for original equipment manufacturers (OEMs) powered by the combination of generative AI and IoT:

### 1. Assisted Diagnosis and Troubleshooting

The combination of IoT and generative AI can revolutionize maintenance management. For example, consider the scenario where data from IoT sensors on equipment triggers anomaly alerts due to a threshold, such as temperature, pressure, or vibration, being breached. These alerts can be enriched with additional context from generative AI analysis of equipment manuals, standard operating procedure docs (SOPs), historical maintenance records, captured human experience, spare parts history, and more.

Accompanying alerts, maintenance teams can receive complete context about the problem, detailed step-by-step repair guidance, specific spare parts recommendations, and a lists of tools needed for the repair. This simplifies troubleshooting and reduces time to repair for both OEM service technicians and end-customer maintenance staff, reducing the need for experienced service engineers on-site.

For a sample implementation of this use case, consult [Guidance for Assisted Diagnosis and Troubleshooting on AWS](https://aws.amazon.com/solutions/guidance/assisted-diagnosis-and-troubleshooting-on-aws/). This combination provides comprehensive maintenance guidance that goes beyond fault detection and can even be delivered through [voice-enabled AI assistants](https://aws.amazon.com/blogs/messaging-and-targeting/building-voice-interface-for-genai-assistant/) with speech-to-speech models that allow technicians to verbally request diagnostic information while keeping their hands free for repair work.

### 2. Enhanced Field Service Operations

Building on the foundation of on-site assisted diagnosis and troubleshooting, machine builders can transform field service operations with generative AI through remote diagnostics and intelligent pre-visit preparation. Field service teams receive AI-generated diagnostic reports, allowing them to analyze machine data, such as sensor readings and error codes, remotely and quickly prepare what is needed for each repair if an on-site visit is needed.

This preparation includes spare parts insights, appropriate tools needed, and matching technician expertise to the specific problem. The result is a reduction in multiple site visits, reduced maintenance costs and significant improvements in first-time fix rates and time-to-repair. Better fault analysis and preparation enables better resource allocation, faster repair times, more efficient technician deployment and improved customer experience.

Watch [this video](https://www.youtube.com/watch?v=ip7Q-mYrMq4) to see how KONE, a global leader in elevators and escalators, together with AWS, developed an AI-powered technician assistant to help technicians fix elevators faster by analyzing maintenance history, IoT data, and relevant documentation from their connected elevators.

### 3. Machine Fleet Analysis for OEMs

Traditional fleet analytics require data scientists and complex data engineering to extract insights from thousands of deployed machines. Generative AI transforms this by enabling natural language queries across vast datasets, automatically generating narrative insights that combine telemetry data with unstructured sources, like service reports and operator feedback.

Instead of manually building dashboards to understand performance patterns, OEMs can ask questions, like "What are the common failure modes for excavators in high-temperature environments?", and receive comprehensive analyses that identify trends, correlate environmental factors, and recommend design improvements. This makes fleet insights accessible beyond technical teams, enabling sales and product teams to quickly understand how equipment performs across different use cases and environments.

These insights can also enable new 'servitization' business models. The system automatically generates detailed performance narratives by asset type, customer segment, and geography, revealing patterns that would previously require significant manual analysis.

### 4. AI-generated Diagnostic Reports

OEMs can leverage generative AI to create comprehensive operational reports from their products, synthesizing multiple data sources, including telemetry data, maintenance history, environmental conditions, and incident logs. These reports can create strategic insights for their own teams, also saving also time from manual reporting and data collection.

Unlike reactive diagnostics, these reports analyze broader performance patterns to inform product development, identify design improvements, and optimize service and customer support strategies. These reports can have a dual-reporting approach creating value at both levels: strategic intelligence for manufacturers and automated multidimensional reporting for customers.

OEMs can offer these diagnostic capabilities as premium services to their customers, generating recurring revenue while building stronger customer relationships through enhanced equipment reliability, better customer service and insights to manage customer operations.

Watch [this video](https://www.youtube.com/watch?v=oKYbuubSK_g) to see how HP is transforming the future of industrial printing with AWS, utilizing IoT, machine learning, and generative AI to create the Intelligent Printing factory of the future.

## Bridging IoT Data with Generative AI

The [Guidance for Deploying Smart Machines on AWS](https://aws.amazon.com/solutions/guidance/deploying-smart-machines-on-aws/) provides a starting point for your Smart Machines journey. This guidance establishes the fundamental building blocks needed to connect and manage smart machines effectively at scale, while creating an industrial data foundation that allows you to prepare, contextualize, and maintain quality data for various applications. With this foundation in place, machine builders can develop new capabilities using generative AI on AWS.

Industrial IoT data is ingested either directly into AWS IoT SiteWise using AWS IoT SiteWise Edge or via AWS IoT Core rules. Within the system, this data is organized into digital asset models that combine both static (e.g. serial numbers, machine type) and dynamic properties (e.g. sensor readings, GPS location). These individual assets, such as motors, actuators, and pumps are then connected in parent-child relationships to represent larger machines and equipment.

The foundation of structured IoT data becomes even more powerful when combined with generative AI capabilities, transforming raw operational data into actionable insights and intelligent automated responses for assisted maintenance and fleet management analysis. This pattern can also extend to third-party industrial systems such as a maintenance platform to obtain spare parts and maintenance records information.

## Amazon Bedrock: A flexible solution for IoT and generative AI Integration

Machine builders working on smart machine solutions can start their generative AI journey with Amazon Bedrock. Amazon Bedrock is a fully managed service that provides easy access to a choice of leading foundation models (FMs). With [Amazon Bedrock Knowledge Bases](https://aws.amazon.com/bedrock/knowledge-bases/), you can easily connect these models with your organization's data to provide accurate, relevant, and contextual responses based on your specific information sources.

Amazon Bedrock Knowledge Bases connect with your existing data in Amazon S3, external systems, and customer solutions including Salesforce, Confluence and SharePoint as well as custom endpoints, allowing rapid deployment. Setting up an Amazon Bedrock Knowledge Base is quick and straightforward using the steps defined [here](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base-create.html).

Combining the models and your data with [Amazon Bedrock Agents](https://aws.amazon.com/bedrock/agents/) allows you to quickly derive insights from your IoT data and proprietary information, regardless of where your data is stored. Through natural language interactions, you can monitor a single machine or seamlessly scale to manage entire fleets and generate operational summaries. Amazon Bedrock Agents can orchestrate and execute tasks against external systems, allowing you to query your IoT data and your maintenance systems to create new incident tickets and alerts.

For example, Amazon Bedrock agents can automatically create support tickets in [Amazon Connect](https://aws.amazon.com/connect/), enriched with IoT data and knowledge base insights. When equipment issues occur, the system instantly notifies operators with contextual information, enabling faster resolution and proactive customer service. For more details on this contact center pattern, consult [Guidance for Connecting Automated Inputs to Contact Centers on AWS](https://aws.amazon.com/solutions/guidance/connecting-automated-inputs-to-contact-centers-on-aws/).

Amazon Bedrock also supports [multi-agent collaboration](https://docs.aws.amazon.com/bedrock/latest/userguide/agents-multi-agent-collaboration.html) to accelerate the build of agentic systems for more complex workflows. See [Amazon Bedrock multi-agent collaboration](https://catalog.us-east-1.prod.workshops.aws/workshops/1031afa5-be84-4a6a-9886-4e19ce67b9c2/en-US) for a hands-on demonstration of this capability.

## Edge Intelligence for Smart Machines

Deploying generative AI capabilities directly at the edge is a compelling option for industrial equipment operating in environments with limited or unstable connectivity. Depending on connectivity and compute availability, a hybrid approach can also be employed where smaller routine tasks execute against the edge models and more complex queries are offloaded to large language models (LLMs) in the cloud if connectivity is available.

Embedding small language models (SLMs) directly into their smart machines is also possible, enabling continuous AI-powered support even in offline conditions. Check out these blogs for a deeper dive on [Edge Intelligence with AWS](https://aws.amazon.com/blogs/iot/unlocking-real-time-intelligence-at-the-edge-with-awss-connected-edge-intelligence/) and [Best Practices for Generative AI and IoT at the edge](https://aws.amazon.com/blogs/iot/emerging-architecture-patterns-for-integrating-iot-and-generative-ai-on-aws/).

## AWS IoT SiteWise Assistant: A native solution for Industrial IoT and generative AI integration

While Amazon Bedrock provides a flexible foundation for any IoT data source, AWS also offers a purpose-built solution for industrial equipment manufacturers who utilize AWS IoT SiteWise for their industrial data collection, storage, and analysis needs. [AWS IoT SiteWise Assistant](https://aws.amazon.com/about-aws/whats-new/2024/11/aws-iot-sitewise-generative-ai-powered-industrial-assistant/) enhances AWS IoT SiteWise capabilities by enabling natural language queries of your machine data instead of needing to write complex technical query statements to gain insights into machine performance, trends, and operational metrics.

For a more detailed overview, see [Transforming industrial decision making with AWS IoT SiteWise Assistant](https://aws.amazon.com/blogs/industries/transforming-industrial-decision-making-with-aws-iot-sitewise-assistant/).

## Generative AI within connected Smart Machines with AWS Partners

AWS Partners play a key role in supporting AWS customers building smart machine solutions, from strategy consulting and ideation to delivery of scalable and secure solutions that leverage the [Guidance for Deploying Smart Machines on AWS](https://aws.amazon.com/solutions/guidance/deploying-smart-machines-on-aws/). In this section, we address how some of these system integrator (SI) AWS Partners are helping customers and advancing the broader smart machine industry with the combination of IoT and generative AI.

- [**Deloitte**](https://aws.amazon.com/partners/deloitte/) harnesses generative AI to enable assisted maintenance and autonomous decision-making for Smart Machines, optimizing both aftermarket support and the shift towards Equipment-as-a-Service (EaaS).

- [**SoftServe's**](https://partners.amazonaws.com/partners/001E000000e4HhNIAU/) unified [IIoT platform](https://aws.amazon.com/marketplace/pp/prodview-tcq7u7n3bp6mg) and [generative AI solution](https://aws.amazon.com/marketplace/pp/prodview-uxeclu57sy2g6) combine Industrial IoT (IIoT), generative AI, Digital Twins and NVIDIA capabilities to transform Smart Machines. Their Schunk implementation empowers remote and field support engineers to efficiently troubleshoot customer equipment.

- [**Twisthink**](https://partners.amazonaws.com/partners/0010L00001jTjLpQAK/) is now supporting [Smart Machines use cases](https://twisthink.com/event/webinar-revolutionize-smart-machines-with-aws-iot/) using generative AI for prescriptive maintenance and fleet management analytics with less development effort and investment.

- [**Green Custard**](https://www.green-custard.com/) combines IoT and generative AI on AWS to revolutionize its Smart Machine offerings through assisted maintenance real-time performance optimization, and enhanced customer support. Their [Britvic's Aqua Libra Flavour Tap](https://www.green-custard.com/generative-ai-for-connected-products-service-and-support/) implementation demonstrates enhanced customer service through intelligent analysis of IoT data and support documentation.

## Conclusion

Combining IoT and generative AI is transformative for smart machine builders, enhancing maintenance operations, expanding fleet management processes, and generating new revenue streams through new applications for your customers. AWS and AWS Partners offer services and solutions to help manufacturers expand their current IoT solutions or build new smart machines that positions manufacturers to stay competitive and drive revenue growth.

Ready to transform your products with IoT and generative AI? Start your smart machine journey today by [reaching out to AWS](https://pages.awscloud.com/GLOBAL-ln-GC-A4IND-Contact-Us-interest.html) or your AWS partner. For more information on generative AI at AWS, see the resources below:

- [Generative AI for Industrial](https://aws.amazon.com/industrial/generative-ai/)
- [Generative AI Innovation Center](https://aws.amazon.com/ai/generative-ai/innovation-center/)
- [Best practices for building robust generative AI applications with Amazon Bedrock Agents](https://aws.amazon.com/blogs/machine-learning/best-practices-for-building-robust-generative-ai-applications-with-amazon-bedrock-agents-part-1/)
- [AWS Internet of Things](https://aws.amazon.com/iot/)

---

**Tags:** AWS IoT, aws manufacturing, Generative AI, Smart Machines

**Authors:**

- **Dimitrios Spiliopoulos** - Worldwide Principal IIoT GTM Specialist in AWS
- **Gabriel Verreault** - Senior Partner Solutions Architect at AWS for the Manufacturing segment
- **Gary Emmerton** - Senior Solutions Architect in AWS based in the UK

**Source:** [AWS for Industries Blog](https://aws.amazon.com/blogs/industries/maximizing-the-value-of-smart-machines-with-generative-ai-and-iot/)
