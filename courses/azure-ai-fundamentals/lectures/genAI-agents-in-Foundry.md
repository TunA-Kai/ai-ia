---
title: 'GenAI and Agents in Foundry'
course: 'Azure AI Fundamentals'
date: 2026-02-23
topic: 'Generative AI'
tags: [AI, Generative AI, Foundry]
---

# Lecture: GenAI and Agents in Foundry

## Detailed Notes

### Agents

- Agents are applications that can respond to user input or assess situations autonomously, and take appropriate actions.
- Agents contain three main components:
  - A language model that powers reasoning and language understanding
  - Instructions that define the agent’s goals, behavior, and constraints
  - Tools, or functions, that enable the agent to complete tasks

- Categorize gen AI applications:
  - Ready-to-use: Pre-built applications that can be used immediately.
  - Extendable: Applications that can be customized or extended with additional functionality.
  - Build-your-own: Applications that require building from scratch starting with a language model and tools.

### Foundry

- Foundry is Microsoft's unified platform for enterprise AI operations, model builders, and application development. As a PaaS (platform as a service), Microsoft Foundry gives developers control over the customization of language models used for building applications. These models can be deployed in the cloud and consumed from custom-developed apps and services.

- Customizing models:
  - Using grounding data
  - Implementing RAG
  - Fine-tuning: take a pretrained model and further train it on a specific dataset to improve performance on a particular task.
  - Managing security and governance controls

### Observability

- 3 dimensions for evaluating and monitoring gen AI:
  - Performance and quality evaluation: Assessing the accuracy, relevance, and coherence of the generated content.
  - Risk and safety evaluators: assess potential risks associated with AI-generated content to safeguard against content risks. This includes evaluating an AI system's predisposition towards generating harmful or inappropriate content.
  - Custom evaluators: industry-specific metrics to meet specific needs and goals

- Evaluators in Foundry:
  - Groundedness
  - Relevance
  - Fluency
  - Coherence
  - Content safety

## Resources

- [Lecture](https://learn.microsoft.com/en-us/training/modules/get-started-generative-ai-azure/)
