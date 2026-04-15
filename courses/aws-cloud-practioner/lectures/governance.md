---
title: "Governance"
course: "AWS Cloud Practitioner Essentials"
date: 2026-04-14
topic: "Monitoring, Compliance and Governance in the AWS Cloud"
tags: [cloud, AWS, fundamentals]
---

# Lecture: Governance

## Key Concepts

### What is Governance

Governance refers to the policies, procedures, and controls that ensure your cloud resources and data are managed in a secure, compliant, and efficient manner. It encompasses compliance, risk management, and operational best practices.

### AWS Control Tower vs. AWS Organizations

| Feature                              | **AWS Control Tower**                                                         | **AWS Organizations**                                                     |
| ------------------------------------ | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| **Primary purpose**                  | Set up and govern a multi-account AWS environment with best-practice defaults | Centrally manage multiple AWS accounts                                    |
| **Ease of setup**                    | **Higher** — automates landing zone creation                                  | **Lower** — you configure governance and structure yourself               |
| **Governance**                       | Built-in **guardrails** for security and compliance                           | Uses **SCPs** and manual policies for governance                          |
| **Account provisioning**             | **Account Factory** simplifies new account creation                           | You can create/manage accounts, but it’s less automated                   |
| **Best for**                         | Teams that want **opinionated, turnkey governance**                           | Teams that want **basic multi-account management** or full custom control |
| **Monitoring/compliance visibility** | Includes a dashboard and compliance visibility                                | No comparable out-of-the-box governance dashboard                         |
| **Customization**                    | More opinionated, less flexible                                               | More flexible, but you build more yourself                                |
| **Dependency**                       | Built on top of AWS Organizations                                             | Core AWS account management service                                       |

- **AWS Organizations** = the foundation for managing accounts.
- **AWS Control Tower** = a higher-level service that **uses Organizations** and adds automated setup, guardrails, and governance.
