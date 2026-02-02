---
title: 'Understand Azure'
course: 'Azure AI Fundamentals'
date: 2026-02-02
topic: 'Understanding Azure for AI Applications'
tags: [AI application, components, Azure]
---

# Lecture: Understand Azure

### Overview 🚀

- Short summary: **Azure** is Microsoft’s cloud platform that gives you on-demand computing, storage, networking, and app services so you can build, run, and manage applications without owning physical servers.
- **Foundry** is an AI development layer that runs on Azure and provides managed tools and models to build generative AI apps with enterprise governance. You start from an Azure subscription, create a Foundry project resource, then build your AI application.

---

### Key points explained simply ☁️

- **Compute** = the workers (virtual machines, containers, serverless functions) that run your programs.
- **Storage** = where your data lives (like file cabinets: Blob Storage, Azure Files).
- **Networking** = the roads and gates that connect and protect resources (virtual networks, load balancers).
- **Application services** = ready-made tools for hosting web apps, APIs, and mobile backends so you don’t build everything from scratch.

---

### How Azure organizes things — plain language 🧭

Think of Azure like a company with folders and accounts:

- **Tenant** = the company directory (where identities and access rules live).
- **Subscription** = a billing account or budget for a set of resources.
- **Resource group** = a folder that holds related resources (so you can manage them together).
- **Resource** = an individual item you use (a VM, database, storage account, or a Foundry project).

This hierarchy helps with security, billing, and managing everything at scale.

---

### What Foundry means on Azure 🔧

- **Foundry projects and hubs** are treated like other Azure resources — they tie into Azure networking, storage, and security.
- **Foundry tools and models** are cloud-based and accessed through a Foundry resource, and they are managed using the same Azure resource lifecycle (create, delete, availability, billing).
- Practical takeaway: start with a subscription → create a Foundry project resource → use the Foundry tools/models and Azure services to build and run your AI app.

---

### Why this matters — simple benefits ✅

- Faster AI development because Foundry provides ready tools and models.
- Consistent management and billing because Foundry uses the Azure resource model.
- Enterprise-grade governance and integration with your existing Azure security, networking, and storage.

## Resources

- [Lecture](https://learn.microsoft.com/en-us/training/modules/get-started-ai-in-foundry/6-about-azure/?ns-enrollment-type=learningpath&ns-enrollment-id=learn.introduction-ai-azure)
