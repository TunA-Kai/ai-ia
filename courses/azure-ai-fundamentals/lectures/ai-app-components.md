---
title: 'Components of an AI application'
course: 'Azure AI Fundamentals'
date: 2026-02-02
topic: 'Layer of an AI Application on Azure'
tags: [AI application, components, Azure]
---

# Lecture: Components of an AI application

Here's a simplified breakdown of how Microsoft supports AI applications:

### Data Layer

- **Purpose**: The foundation for AI, handling the collection, storage, and management of data.
- **Components**:
  - **Azure SQL, PostgreSQL**: For structured data.
  - **Azure Cosmos DB, Azure Data Lake**: For large-scale data storage and management.
- **Function**: Provides the necessary data for training and decision-making.

### Model Layer

- **Purpose**: Focuses on AI model selection, training, and deployment.
- **Components**:
  - **Pretrained Models**: Like Azure OpenAI in Foundry Models.
  - **Custom Models**: Built with Azure Machine Learning.
- **Tools**: Used for fine-tuning and evaluating model performance.

### Compute Layer

- **Purpose**: Provides computing power to train and run AI models.
- **Options**:
  - **Azure App Service**: For hosting web apps and APIs.
  - **Azure Functions**: For serverless AI task execution.
  - **Containers**: Using Azure Container Instances (ACI) for fast deployment, and Azure Kubernetes Service (AKS) for managing AI workloads.

### Integration & Orchestration Layer

- **Purpose**: Connects data and models to business logic and user interfaces.
- **Features**:
  - **Intelligent Agents**: Built with Foundry for reasoning and actions.
  - **AI Tools**: Speech, vision, and language APIs.
  - **SDKs and APIs**: For integrating AI into applications.

### Key Term

- **Foundry**: Microsoft's platform for developing and managing enterprise AI applications, helping integrate smart capabilities directly into applications.

This setup helps developers build applications with intelligent features efficiently and effectively.

## Resources

- [Lecture](https://learn.microsoft.com/en-us/training/modules/get-started-ai-in-foundry/3-components)
