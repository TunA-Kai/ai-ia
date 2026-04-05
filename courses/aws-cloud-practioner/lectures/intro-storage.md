---
title: "Introduction to Storage"
course: "AWS Cloud Practitioner Essentials"
date: 2026-04-04
topic: "Cloud Storage Basics"
tags: [cloud, AWS, storage]
---

# Lecture: Introduction to Storage

## 📊 **Storage Types Comparison**

| Feature           | 🧱 Block Storage (EBS)        | 📁 File Storage (EFS/FSx)    | 📦 Object Storage (S3)     |
| ----------------- | ----------------------------- | ---------------------------- | -------------------------- |
| **Data Unit**     | Blocks (fixed size)           | Files & directories          | Objects (file + metadata)  |
| **Structure**     | No filesystem (OS creates it) | Hierarchical (folders/files) | Flat (buckets + keys)      |
| **Access Method** | Direct block access           | File path (NFS/SMB)          | API (HTTP/HTTPS)           |
| **Performance**   | Very high ⚡                  | Moderate                     | Moderate (higher latency)  |
| **Scalability**   | Limited per volume            | Scales automatically         | Virtually unlimited 📈     |
| **Sharing**       | Limited (usually single host) | Multi-host shared access 🤝  | Global access via API      |
| **Management**    | User-managed filesystem       | Managed filesystem           | Fully managed              |
| **Typical Use**   | Databases, OS disks           | Shared storage, CMS          | Backups, media, data lakes |

---

## 🧠 **Quick mental model**

- 🧱 **Block** → raw disk you control
- 📁 **File** → shared network drive
- 📦 **Object** → internet-scale storage with APIs

---

## ✅ **Rule of thumb**

- Need **speed + low latency** → Block
- Need **shared file system** → File
- Need **massive scale + cheap storage** → Object
