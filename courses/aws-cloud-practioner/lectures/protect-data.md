---
title: "Protect Data"
course: "AWS Cloud Practitioner Essentials"
date: 2026-04-12
topic: "AWS Security"
tags: [cloud, AWS, fundamentals]
---

# Lecture: Protect Data

## Key Concepts

### Encryption

Encryption is the process of converting data into a form that cannot be easily understood by unauthorized individuals. It uses algorithms to transform plaintext data into ciphertext, which can only be decrypted back to its original form with the correct decryption key.

### Types of encryption

- **At rest**: Data that is stored on disk or in a database.
- **In transit**: Data that is being transmitted over a network. SSL/TLS certificates are used to establish encrypted network connections from one system to another.

### AWS built-in data protection

- S3: By default, all new S3 buckets have encryption configured, and all uploaded objects are encrypted at rest.
- EBS: Amazon EBS volumes and snapshots can be encrypted at rest, including both boot and data volumes of an Amazon EC2 instance.
- DynamoDB: Server-side encryption at rest is enabled on all DynamoDB table data using encryption keys stored in AWS Key Management Service (AWS KMS).

### AWS Key Management Service (KMS)

You can use AWS KMS to create and manage cryptographic keys. These keys can then be used to encrypt and decrypt your data.

A cryptographic key is a random string of digits used for locking (encrypting) and unlocking (decrypting) data.

### Amazon Macie

Amazon Macie is a fully managed data security and data privacy service. Macie uses machine learning and pattern matching to help you discover, monitor, and protect your sensitive data in Amazon S3.

### AWS Certificate Manager (ACM)

AWS Certificate Manager (ACM) helps you to provision, manage, and renew publicly trusted TLS certificates on AWS based websites.
