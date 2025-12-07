---
title: "Event 2"
date: 2024-10-15
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy it verbatim** into your report, including this warning.
{{% /notice %}}

# Summary Report: "Introduction to AI and AWS AI Services Workshop"

### Event Information

**Date:** October 15, 2024  
**Location:** University Workshop  
**Speakers:** Instructor Khanh and Instructor Vương  
**Format:** In-person Workshop with Hands-on Demonstrations

### Event Objectives

- Introduce fundamental concepts of Artificial Intelligence (AI)
- Explore the evolution from Machine Learning to Deep Learning and Generative AI
- Demonstrate AWS AI services and their practical applications
- Guide students on getting started with AWS platform
- Provide hands-on experience with real-world AI use cases

### Speakers

- **Instructor Khanh** – AWS Technical Instructor
- **Instructor Vương** – AWS Solutions Architect

### Key Highlights

#### Understanding AI: From Definition to Modern Applications

**What is Artificial Intelligence?**

AI is the capability of machines to perform tasks that typically require human intelligence, including:

- **Understanding**: Comprehending language, context, and meaning
- **Reasoning**: Making logical decisions based on available information
- **Learning**: Improving performance through experience

The speaker emphasized that AI is not magical—it follows mathematical models and algorithms that can be understood and controlled.

#### Evolution of AI Technologies

**1. Machine Learning (Traditional AI)**

- Uses algorithms to learn patterns from data
- Requires structured data and labeled datasets
- Example: Predicting lottery numbers based on 10 years of historical data
- Suitable for simpler, well-defined problems

**2. Deep Learning (Modern AI)**

- Mimics human neural networks with multiple layers
- Can process complex data types: images, audio, video
- Uses neural network architecture similar to the human brain
- Enables understanding of unstructured data

**3. Generative AI (Latest Evolution)**

- Learns from massive datasets (Large Language Models - LLMs)
- Can create entirely new content: text, images, videos
- Examples: ChatGPT, Google Gemini, Amazon Bedrock
- Capable of creative tasks like writing poetry or generating art

#### AWS Cloud Platform and AI Services

**Why AWS?**

AWS develops services based on:

1. **Internal use first**: Services are tested on Amazon.com operations
2. **Customer feedback**: Features developed based on actual customer needs
3. **Continuous innovation**: Over 200 services and 10,000+ features

**Three-Layer Architecture:**

1. **AI Services Layer (Top)**: Ready-to-use APIs

   - Amazon Comprehend: Text analysis and sentiment detection
   - Amazon Translate: Multi-language translation
   - Amazon Textract: Document data extraction
   - Amazon Transcribe: Speech-to-text conversion
   - Amazon Polly: Text-to-speech synthesis

2. **ML Platform Layer (Middle)**:

   - Amazon SageMaker: Build, train, and deploy custom models
   - Full control over training process and model optimization

3. **Infrastructure Layer (Bottom)**:
   - GPU instances for training
   - Partnership with NVIDIA for high-performance computing

#### Amazon Comprehend - Natural Language Processing

**Capabilities:**

- Sentiment analysis (positive, negative, neutral)
- Entity recognition (names, locations, organizations)
- Language detection
- Key phrase extraction
- Document classification

**Real-World Applications:**

1. **E-commerce Reviews Analysis**

   - Automatically classify customer reviews as positive/negative
   - Extract key themes from feedback
   - Monitor brand sentiment

2. **Social Media Monitoring**

   - Analyze public opinion on social platforms
   - Identify trending topics and sentiment shifts

3. **Customer Service**

   - Categorize support tickets automatically
   - Route urgent issues based on sentiment
   - Generate response suggestions

4. **Financial Document Analysis**
   - Extract key information from financial reports
   - Identify sensitive personal information for compliance
   - Mask PII (Personally Identifiable Information) automatically

#### Amazon Translate - Language Translation Service

**Features:**

- Supports 75+ languages including Vietnamese
- Real-time translation
- Batch document translation
- Custom terminology support

**Use Cases:**

1. **Multi-language Websites**

   - Automatic content translation for international users
   - Support for e-commerce platforms
   - Travel and tourism applications

2. **Document Translation**

   - Translate business documents
   - Process multilingual customer communications
   - Handle Khmer (Cambodian) documents with OCR preprocessing

3. **Language Learning Applications**
   - Examples: ELSA (English learning app)
   - Pronunciation checking
   - Real-time translation practice

#### Amazon Textract - Intelligent Document Processing

**Capabilities:**

- Extract text from PDFs and images
- Recognize tables and forms
- Preserve document structure
- Handwriting recognition

**Practical Applications:**

- Convert PDF to Word/PowerPoint
- Extract data from invoices and receipts
- Process government forms automatically
- Digitize historical documents

The instructor demonstrated live how Textract can capture text from photos with high accuracy, including Vietnamese text.

#### Cloud Service Models

The workshop explained three service delivery models:

1. **Software as a Service (SaaS)**

   - Ready-to-use applications (Google Translate, etc.)
   - No installation required
   - Pay-as-you-go pricing

2. **Platform as a Service (PaaS)**

   - AWS APIs and services
   - Developer tools and frameworks
   - Simplified deployment

3. **Infrastructure as a Service (IaaS)**
   - Virtual machines and storage
   - Full control over environment
   - Scalable resources

#### Learning Resources and Getting Started

**AWS Skill Builder:**

- Free training platform
- 2000+ courses (80% free)
- Hands-on labs and certifications
- Vietnamese language support coming soon

**AWS Free Tier:**

- $200 credits for students
- Sandbox environments for experimentation
- No credit card required for learning accounts

### Key Takeaways

1. **AI is Accessible**: Modern AI services are available through simple APIs, no PhD required
2. **Start Small**: Use existing AI services before building custom solutions
3. **Data is Critical**: Quality and quantity of data determine AI success
4. **Generated Data Works**: AI can generate synthetic data for testing and demos
5. **Open Source Options**: Many free alternatives exist (TensorFlow, PyTorch)
6. **Privacy Matters**: AWS doesn't use customer data for training models
7. **Cost Management**: Use free tiers and sandbox environments for learning

### Practical Advice for Students

**For Data Collection:**

- Web scraping (with ethical considerations)
- Kaggle datasets for practice projects
- AI-generated synthetic data for testing
- Public financial reports and open data sources

**For Project Development:**

- Start with open-source frameworks (PyTorch, TensorFlow)
- Use Google Colab or Jupyter notebooks
- Leverage AWS credits for scaling
- Focus on solving real business problems

**For Career Development:**

- Build practical projects, not just theory
- Understand end-to-end workflow
- Learn both technical and business aspects
- Contribute to open-source projects

### Q&A Session Highlights

**Q: How to handle company data privacy when using AI?**
A: Data stays on company servers; only API calls are made to AI services. AWS has strict data privacy commitments and doesn't train models on customer data.

**Q: How to get data for projects with limited resources?**
A:

1. Generate synthetic data with AI
2. Use web scraping (ethically)
3. Access Kaggle datasets
4. Use public domain datasets (COVID data, financial reports)
5. Leverage Yahoo Finance for financial data

**Q: How to test projects at scale without resources?**
A: Use AWS sandbox environments, apply for student credits ($200 available), and join competitions that provide infrastructure.

**Q: Can I analyze emotions from voice?**
A: Yes, but it requires two approaches:

1. Convert speech to text, then analyze sentiment
2. Analyze audio properties (decibel levels, tone, pitch)
   Both require labeled training data distinguishing different emotional states.

**Q: Is AI-generated data reliable for training?**
A: Suitable for demos and proof-of-concept, but not for production systems with real users. It's great for showing feasibility but needs real data for actual deployment.

### Personal Insights

This workshop was incredibly valuable for understanding the practical side of AI development. Rather than just theoretical concepts, the instructors showed real AWS services that are production-ready and used by major companies.

The emphasis on starting with existing services rather than building from scratch was eye-opening. As students, we often want to build everything ourselves, but leveraging existing APIs can accelerate development and let us focus on solving actual business problems.

The Q&A session was particularly insightful, addressing real concerns about data privacy, cost management, and project scalability. The advice to use open-source tools for learning and AWS services for scaling provides a clear path forward.

### Hands-on Demonstration Photos

_Add your workshop photos here showing:_

- Live demonstrations of AWS services
- Instructor presentations
- Hands-on exercises
- Q&A sessions

> This workshop demystified AI and cloud services, showing that modern AI development is accessible to students and requires more creativity and problem-solving than just technical expertise. The combination of AWS services and open-source tools provides everything needed to build real-world AI applications.

### Next Steps

1. **Create AWS Free Tier Account**: Get started with hands-on practice
2. **Explore AWS Skill Builder**: Complete introductory AI courses
3. **Try AWS Services**: Experiment with Comprehend, Translate, and Textract
4. **Build a Project**: Apply learned concepts to solve a real problem
5. **Join AWS Community**: Connect with other learners and builders

### Conclusion

The "Introduction to AI and AWS AI Services" workshop provided a comprehensive overview of modern AI technologies and practical tools for implementation. The combination of theoretical foundations, live demonstrations, and hands-on guidance makes AWS AI services accessible to developers at all levels. The key message: start building with existing tools, focus on solving real problems, and continuously learn and experiment.
