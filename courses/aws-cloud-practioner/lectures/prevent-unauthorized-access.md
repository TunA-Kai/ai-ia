---
title: "Prevent Unauthorized Access"
course: "AWS Cloud Practitioner Essentials"
date: 2026-04-12
topic: "AWS Security"
tags: [cloud, AWS, fundamentals]
---

# Lecture: Prevent Unauthorized Access

## Key Concepts

### IAM (Identity and Access Management)

IAM is a service that helps you securely control access to AWS services and resources for your users.

With IAM, by default, all actions are denied. You must explicitly grant permission to someone before they can perform any actions in your account.

![iam](../images/M09_IAMIdentities.png)

### IAM Identity Center

IAM Identity Center centralizes identity and access management across AWS accounts and applications. IAM Identity Center can also connect to an existing identity source and provide your workforce with single sign-on access to all your connected AWS services and accounts. This is called federated identity management.

**Federated identity management** is a system that allows users to access multiple applications, services, or domains using a single set of credentials.

### AWS Secrets Manager

Secrets Manager provides a secure way to manage, rotate, and retrieve database credentials, API keys, and other secrets throughout their lifecycle.

### AWS Systems Manager

AWS Systems Manager helps you centrally view, manage, and operate nodes at scale in AWS, on-premises, and multicloud environments. With the launch of a unified console experience, Systems Manager consolidates various tools to help you complete common node tasks across AWS accounts and AWS Regions.
