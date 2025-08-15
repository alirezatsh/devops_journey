# MongoDB Overview

## What is MongoDB?
MongoDB is an open-source NoSQL database that stores data in a flexible, JSON-like format called BSON (Binary JSON).  
Unlike relational databases, MongoDB is schema-less, allowing developers to store and query data without predefined table structures.


## How MongoDB Works
- Document-Oriented: Data is stored in documents (key-value pairs) inside collections.
- Schema Flexibility: You can have different fields in different documents within the same collection.
- Horizontal Scalability: MongoDB supports sharding, splitting data across multiple servers for performance.
- High Availability: Through replica sets, MongoDB provides automatic failover and redundancy.


## Key Features
- NoSQL & Schema-less: Flexible document structure.
- Rich Query Language: Supports filtering, aggregation, geospatial queries, and text search.
- High Performance: Handles high write and read throughput.
- Horizontal Scalability: Easily scale across multiple machines.
- Automatic Failover: Keeps your database online even during hardware failures.


## Use Cases
- Real-time analytics (dashboards, monitoring tools)
- Content management systems (CMS)
- IoT data storage
- E-commerce platforms
- Mobile and game backends
- Catalog and inventory management


## Disadvantages
- Memory Usage: Uses more RAM compared to relational databases because of document-based storage and indexes.
- No Joins by Default: While `$lookup` exists, it's slower than SQL joins for complex relationships.
- Document Size Limit: Max 16 MB per document, requiring GridFS for large files.
- Transaction Overhead: Multi-document ACID transactions are newer and may be slower than traditional RDBMS.
- Data Duplication: Without normalization, redundancy can increase storage requirements.
- Complex Sharding Management: Requires careful planning to avoid uneven data distribution.
- Less Suitable for Complex Multi-Table Relationships: Relational DBs handle such scenarios more efficiently.
- Indexing Overhead: Large indexes can reduce write performance.


## Best Compatibility
MongoDB works well with:
- Node.js / Express.js (via Mongoose ORM)
- Python (via PyMongo, Motor)
- Java / Spring Boot (via Spring Data MongoDB)
- Go, PHP, Ruby, C#, Kotlin — official drivers available.
- Docker and Kubernetes for containerized deployments.


## Stability and Reliability
- Mature and Production-Ready: First released in 2009, widely used in enterprise solutions.
- Replica Sets for redundancy and failover.
- Journaling ensures durability in case of crashes.
- ACID Transactions (since MongoDB 4.0) for multi-document safety.


## Load and Scalability
- Sharding: Distributes large datasets across multiple servers.
- Built for High Load: MongoDB can handle thousands of writes per second on commodity hardware.
- Data Volume: MongoDB databases with terabytes of data are common in production.


## Document Size Limits
- Maximum document size: 16 MB (BSON limit)
- For larger data: Use GridFS to store and retrieve files up to multiple gigabytes.


## Benchmark Performance
Note: Performance depends on use case, hardware, indexing strategy, and query patterns.

- Reads/Writes:  
  On SSD-backed clusters, MongoDB can handle more than 100k operations per second for small documents.  
- Latency:  
  Sub-millisecond reads for indexed queries, ~1–5 ms writes under normal load.  
- Aggregation:  
  Optimized via `$lookup`, `$group`, `$match`, and pipeline stages.


## Security
- Authentication: SCRAM-SHA-1, SCRAM-SHA-256, LDAP.
- Authorization: Role-based access control.
- Encryption: TLS/SSL for in-transit, Encrypted Storage Engine for at-rest.


## Installation

Follow these steps to set up MinIO using Docker:


1. Clone the repo

```bash
git clone https://github.com/alirezatsh/devops_journey.git
```

2. Open a terminal and navigate to the installation folder:

```bash
cd devops_journey/Database/mongodb
```

3. Start the MongoDB container:

```bash
docker-compose up -d
```


## Resources
- [Official MongoDB Documentation](https://www.mongodb.com/docs/)
- [MongoDB GitHub Repository](https://github.com/mongodb/mongo)
- [MongoDB Atlas Cloud](https://www.mongodb.com/atlas)
