---
title: "Block Storage (EBS)"
course: "AWS Cloud Practitioner Essentials"
date: 2026-04-05
topic: "AWS Block Storage (EBS)"
tags: [cloud, AWS, fundamentals]
---

# Lecture: Block Storage (EBS)

## Key Concepts

### EC2 instance store

EC2 instance store refers to the block-level storage that is physically attached to the EC2 instance host computer. Depending on the type of instance, EC2 instance store might come attached as the default storage. Since its data is lost when an instance is stopped or terminated, EC2 instance store is best for temporary memory-based storage needs like buffers, caches, and scratch data. It is not recommended for applications that require data retention.

Benefits:

- Automatically available storage
- Cost effective (included in instance cost)
- High performance

### EBS (Elastic Block Store)

EBS provides persistent block storage for EC2 instances. Unlike instance store, EBS volumes persist independently of the life of an instance, making them suitable for data that needs to be retained.

Use cases:

- Database hosting
- Backup storage for applications
- Rapid deployment of development environments using volume snapshots

Benefits:

- Data migration
- Instance type changes
- Disaster recovery
- Cost optimization
- Performance tuning

### EBS Snapshots

EBS snapshots are point-in-time backups of EBS volume. They can be used for disaster recovery, data migration, volume resizing, and for creating consistent backups of production workloads. EBS snapshots are incremental, so they only save the blocks on the volume that have changed after your most recent snapshot.

EBS snapshots can be used to create multiple new volumes, and new volumes created from a snapshot are an exact copy of the original volume at the time the snapshot was taken. Snapshots of EBS volumes are stored redundantly in multiple Availability Zones using Amazon S3.

### Data Lifecycle Manager

Data Lifecycle Manager (DLM) is a service that automates the creation, retention, and deletion of EBS snapshots. DLM allows you to define lifecycle policies for your EBS volumes, which can help you manage your snapshots more efficiently and reduce costs by automatically deleting old snapshots that are no longer needed.
