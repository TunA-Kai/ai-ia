---
title: "Detecting and Responding to Security Incidents"
course: "AWS Cloud Practitioner Essentials"
date: 2026-04-12
topic: "AWS Security"
tags: [cloud, AWS, fundamentals]
---

# Lecture: Detecting and Responding to Security Incidents

## Key Concepts

### Amazon Inspector

Amazon Inspector helps improve the security and compliance of applications by running automated security assessments for Amazon EC2 instances, containers, and Lambda functions. It checks applications for security vulnerabilities and deviations from security best practices, such as open access to EC2 instances and installations of vulnerable software versions.

### Amazon GuardDuty

Amazon GuardDuty provides intelligent threat detection across your infrastructure and resources. GuardDuty identifies threats by continuously monitoring streams of your account metadata and network activity in your environment. It uses known malicious IP addresses, anomaly detection, and machine learning to identify threats more accurately.

### Amazon Detective

After a threat has been detected, you can use Amazon Detective to further investigate the root cause. Detective helps you analyze threats with interactive visualizations contained in a unified AWS Management Console view. These visualizations include resource and user interactions over a configurable timeline with recommended steps for remediation.

### AWS Security Hub

Security Hub brings multiple security services together into a single place and format. With this service, you can quickly see your security and compliance state in one comprehensive view. Security Hub automatically aggregates security findings from AWS and partner services and organizes them into actionable, meaningful groupings called insights.

## Summary

| Feature / Service         | **Amazon Inspector**                     | **Amazon GuardDuty**                                   | **Amazon Detective**                 | **AWS Security Hub**                      |
| ------------------------- | ---------------------------------------- | ------------------------------------------------------ | ------------------------------------ | ----------------------------------------- |
| **Primary Purpose**       | Vulnerability scanning                   | Threat detection                                       | Investigation & analysis             | Centralized security management           |
| **Focus Area**            | Known vulnerabilities (CVEs, misconfigs) | Malicious activity & anomalies                         | Root cause analysis of incidents     | Aggregation of security findings          |
| **Data Source**           | EC2, ECR (containers), Lambda            | VPC Flow Logs, DNS logs, CloudTrail                    | GuardDuty, CloudTrail, VPC Flow Logs | Inspector, GuardDuty, Macie, others       |
| **Type of Analysis**      | Continuous scanning                      | Continuous monitoring (ML + threat intel)              | Behavioral graph analysis            | Correlation & prioritization              |
| **Real-time Detection**   | ✅ (continuous scans)                    | ✅ (real-time alerts)                                  | ❌ (post-incident analysis)          | ✅ (aggregates near real-time findings)   |
| **Findings Type**         | CVEs, package vulnerabilities, exposure  | Suspicious activity (e.g., crypto mining, brute force) | Attack patterns, timelines           | Unified findings dashboard                |
| **Automated Remediation** | ❌ (manual or via other tools)           | ❌                                                     | ❌                                   | ❌ (but integrates with automation tools) |
| **Use Case**              | “What vulnerabilities exist?”            | “Is something malicious happening?”                    | “What happened and how?”             | “What’s my overall security posture?”     |
| **Scope**                 | Resource-level scanning                  | Account-level threat detection                         | Cross-resource investigation         | Multi-account, multi-service view         |
| **Integration Role**      | Feeds into Security Hub                  | Feeds into Security Hub                                | Works with GuardDuty findings        | Central aggregator                        |

### 🧠 Simple way to remember

- **Inspector** → _Finds weaknesses_ (vulnerabilities)
- **GuardDuty** → _Detects threats_ (attacks happening)
- **Detective** → _Investigates incidents_ (why/how it happened)
- **Security Hub** → _Brings everything together_ (single dashboard)

### 🏁 Bottom line

They are **complementary**, not replacements:

- Use **Inspector** to prevent issues
- Use **GuardDuty** to detect attacks
- Use **Detective** to analyze them
- Use **Security Hub** to manage everything centrally
