# MinIO - Object Storage Service

## Overview

MinIO is a high-performance, S3-compatible object storage service designed for storing unstructured data such as photos, videos, log files, backups, and container images. It can be used for both private and public cloud deployments and is widely adopted in cloud-native environments, Kubernetes, and microservices architectures.

## Architecture & Infrastructure

- **Object Storage**: Stores data as objects with metadata, unlike traditional file or block storage.
- **S3 Compatibility**: Fully compatible with Amazon S3 APIs, making it easy to integrate with existing applications.
- **Server Deployment**: Can be deployed as a single server, distributed cluster, or in Docker containers.
- **High Availability**: Supports erasure coding, replication, and distributed mode for fault tolerance.
- **Scalability**: Scales horizontally to handle petabytes of data with minimal latency.

### Components

1. **MinIO Server**: Core storage service that manages buckets, objects, and API requests.
2. **MinIO Client (`mc`)**: Command-line tool for managing buckets, objects, users, policies, encryption, and server administration.
3. **Rclone**: Optional CLI tool that supports MinIO as an S3-compatible backend for advanced syncing, backups, and file management.

## Benefits

- Open-source and lightweight.
- High-performance, low-latency storage.
- Fully S3-compatible.
- Easy integration with cloud-native tools like Kubernetes and Docker.
- Advanced security features: encryption at rest, TLS, and IAM-style policies.
- Versioning, lifecycle management, and replication support.

## Limitations

- Designed primarily for object storage; not suitable for relational databases or block storage.
- Large distributed deployments require careful configuration for networking and storage volumes.
- Web UI is basic; advanced features often require CLI (`mc`) or SDKs.

## Installation

Follow these steps to set up MinIO using Docker:


1. Clone the repo

```bash
git clone https://github.com/alirezatsh/devops_journey.git
```

2. Open a terminal and navigate to the installation folder:

```bash
cd devops_journey/Storage/minio/installation 
```

3. Create a folder for MinIO data:

```bash
mkdir data
```

4. Start the MinIO container:

```bash
docker-compose up -d
```
