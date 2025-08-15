# MySQL Overview

## What is MySQL?
MySQL is an open-source, relational database management system (RDBMS) that uses SQL (Structured Query Language) for storing, querying, and managing data.  
It is widely used for web applications, enterprise solutions, and as the backend for many software systems due to its reliability, performance, and ease of use.

---

## How MySQL Works
- Table-Oriented: Data is stored in rows and columns inside tables.
- Strict Schema: Requires predefined structures (tables, columns, data types).
- ACID Compliance: Ensures atomicity, consistency, isolation, and durability.
- Storage Engines: Supports multiple engines like InnoDB (default) and MyISAM.
- Concurrency: Handles multiple simultaneous connections efficiently.

---

## Key Features
- Open-Source and widely supported.
- Full ACID compliance with InnoDB.
- Advanced indexing, foreign keys, and constraints.
- Support for complex queries, joins, and stored procedures.
- Replication and clustering for high availability.
- JSON support for semi-structured data.
- Partitioning and sharding capabilities.

---

## Use Cases
- Web and mobile applications.
- E-commerce platforms.
- Content management systems (CMS).
- Analytics and reporting systems.
- Enterprise applications (ERP, CRM).
- Any system requiring relational data and consistency.

---

## Disadvantages
- Schema changes require migrations.
- Horizontal scaling is more complex than in NoSQL systems.
- Large datasets may need partitioning or external clustering solutions.
- Performance can degrade without proper indexing and optimization.
- Some NoSQL databases outperform MySQL for unstructured or high-volume write workloads.

---

## Best Compatibility
MySQL works well with:
- PHP (via MySQLi, PDO)
- Python (via mysql-connector-python, SQLAlchemy)
- Node.js (via mysql2)
- Java (via JDBC, Hibernate)
- Go, Ruby, C#, Kotlin — official and community drivers.
- Docker and Kubernetes for containerized deployments.

---

## Stability and Reliability
- Mature and widely used in production for decades.
- InnoDB provides crash recovery and ACID compliance.
- Supports replication and clustering for high availability.
- Backup and restore using mysqldump and MySQL Enterprise Backup.

---

## Load and Scalability
- Vertical Scaling: Performs well on powerful servers.
- Horizontal Scaling: Achievable with replication, clustering, or proxy layers.
- Can handle millions of rows efficiently with proper indexing and configuration.

---

## Data Size Limits
- Maximum database size: 256 TB (depending on filesystem).
- Maximum table size: 64 TB (InnoDB).
- Maximum row size: 65,535 bytes (depends on columns and storage engine).
- Maximum columns per table: 1017 (depends on storage engine).

---

## Benchmark Performance
Note: Performance depends on hardware, query optimization, and storage engine.

- Reads/Writes: Efficient for transactional and analytical workloads.
- Latency: Sub-millisecond for indexed reads on small datasets.
- Concurrency: Supports thousands of concurrent connections with proper tuning.

---

## Security
- Authentication: Password-based authentication, LDAP, PAM.
- Authorization: Role-based access control and privileges.
- Encryption: TLS/SSL for in-transit, InnoDB tablespace encryption for at-rest.
- Audit logging and firewall rules for advanced security.

---

## Installation

Follow these steps to set up PostgreSQL using Docker:

1. Clone the repo

```bash
git clone https://github.com/alirezatsh/devops_journey.git

```
2. Open a terminal and navigate to the installation folder:

```bash
cd devops_journey/Database/mysql
‍```

3. Start the MySQL container:

```bash
docker-compose up -d
```

---

# MySQL Resources

- [Official MySQL Documentation](https://dev.mysql.com/doc/)
- [MySQL GitHub Repository](https://github.com/mysql/mysql-server)
- [MySQL Docker Hub](https://hub.docker.com/_/mysql)
