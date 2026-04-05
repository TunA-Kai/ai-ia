---
title: "Object Storage (S3)"
course: "AWS Cloud Practitioner Essentials"
date: 2026-04-05
topic: "AWS Object Storage (S3)"
tags: [cloud, AWS, fundamentals]
---

# Lecture: Object Storage (S3)

## Key Concepts

### S3 (Simple Storage Service)

Amazon S3 is an object storage service that can store unlimited amounts of data in the AWS Cloud. Object storage is particularly well-suited for handling large amounts of unstructured data, such as documents, images, and videos.

Use cases:

- Content distribution
- Hosting static websites
- Delivering media files
- Application data storage
- Archiving
- Data lakes
- Compliance-driven data retention

### S3 Objects

An object in Amazon S3 is the fundamental unit of data storage. When you upload a file to Amazon S3, it becomes an object and is stored durably across multiple facilities within your chosen Region.

Each object typically includes the data itself, metadata, and a unique identifier, or key. Objects can be of any file type, such as images, videos, documents, or application data, and can range in size from a few bytes to several terabytes.

Each Amazon S3 object is uniquely identified within a bucket by its key, which is essentially its file name. Objects also have properties like version ID, access control information, and user-defined metadata.

![S3 Object](../images/M06_03_25_s3ElementsDataMetaKey.png)

### S3 Buckets

An S3 bucket is a container for storing objects in Amazon S3. Buckets have a globally unique name across all of AWS, which helps to identify and organize your stored data.

Buckets serve as the basic unit for access control and can hold a virtually unlimited number of objects.

### Security and privacy management

Everything you store in Amazon S3 is private by default. You must explicitly grant permissions to access these resources. If you want your Amazon S3 data to be available to everyone on the internet, you can choose to make your buckets and objects public. To more granularly define who can do what with your Amazon S3 resources, Amazon S3 provides several security management features.

- **Bucket policies**: Amazon S3 bucket policies are resource-based policies that can only be attached to S3 buckets. An S3 bucket policy specifies which actions are allowed or denied on the bucket, in addition to every object in that bucket. S3 Block Public Access settings override bucket policies.
  ![Bucket Policy](../images/s3-bucket-policy.png)

- **Identity-based policies**: Identity-based policies are attached to IAM users, groups, or roles. They specify what actions those identities can perform on which resources. For example, you can create an identity-based policy that allows a specific IAM user to read objects from a particular S3 bucket.
- **Encryption**: Amazon S3 provides encryption capabilities to protect data both at rest and in transit. These encryption features help maintain data confidentiality and comply with various security standards and regulations. These capabilities are as follows:
  - **Encryption at rest**: Secures data stored in S3 buckets, preventing unauthorized access to stored objects.
  - **Encryption in transit**: Safeguards data traveling to and from Amazon S3, maintaining secure communication between clients and the service.
