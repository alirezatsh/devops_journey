# PostgreSQL Overview

## What is PostgreSQL?
PostgreSQL is a powerful, open-source relational database management system (RDBMS) that uses SQL (Structured Query Language) for querying and managing data.  
It is known for its reliability, feature-rich capabilities, and full ACID compliance, making it a preferred choice for both small and large-scale applications.


## How PostgreSQL Works
- Table-Oriented: Data is stored in rows and columns inside tables.
- Strict Schema: Requires predefined structures (tables, columns, data types).
- ACID Compliance: Ensures atomicity, consistency, isolation, and durability.
- Extensible: Allows custom data types, operators, and functions.
- Concurrency: Uses MVCC (Multi-Version Concurrency Control) for high performance without locking issues.


## Key Features
- Open-Source and Free.
- Full ACID compliance.
- Advanced indexing (B-Tree, Hash, GiST, GIN, BRIN).
- Support for complex queries, joins, and stored procedures.
- JSON and JSONB support for semi-structured data.
- High concurrency with MVCC.
- Replication (Streaming, Logical).
- Partitioning and sharding capabilities.


## Use Cases
- Financial and banking systems.
- E-commerce platforms.
- Analytics and data warehousing.
- ERP and CRM systems.
- GIS applications (Geographic Information Systems).
- Any system requiring complex queries and strict consistency.


## Disadvantages
- Requires predefined schema changes for structure updates.
- Slightly slower write speed compared to some NoSQL databases for unstructured data.
- Horizontal scaling is more complex than in NoSQL systems.
- Large-scale sharding requires additional tools (e.g., Citus).
- More resource-intensive for very high concurrent connections without tuning.


## Best Compatibility
PostgreSQL works well with:
- Python (via psycopg2, SQLAlchemy, Django ORM)
- Node.js (via pg library)
- Java (via JDBC, Hibernate)
- Go, PHP, Ruby, .NET — official and community drivers.
- Docker and Kubernetes for containerized deployments.


## Stability and Reliability
- Extremely stable and widely used in enterprise environments since 1996.
- WAL (Write-Ahead Logging) ensures durability.
- Point-in-time recovery (PITR) for disaster recovery.
- Supports synchronous and asynchronous replication.


## Load and Scalability
- Vertical Scaling: Performs very well on single powerful machines.
- Horizontal Scaling: Achievable through partitioning, replication, and extensions like Citus.
- Handles billions of rows efficiently with proper indexing and tuning.


## Data Size Limits
- Maximum table size: 32 TB.
- Maximum row size: 1.6 TB.
- Maximum field size: 1 GB for `TEXT`, `BYTEA`.
- Practically unlimited database size (limited by storage).


## Benchmark Performance
Note: Actual performance depends on hardware, configuration, and query optimization.

- Reads/Writes:  
  With proper indexing, PostgreSQL can achieve sub-millisecond read latency and tens of thousands of writes per second.
- Aggregations:  
  Optimized query planner and indexing enable efficient grouping and filtering.
- Concurrency:  
  MVCC allows many concurrent readers and writers without blocking.


## Security
- Authentication: Password, SCRAM-SHA-256, GSSAPI, LDAP, and more.
- Authorization: Role-based access control.
- Encryption: TLS/SSL for in-transit, pgcrypto extension for at-rest.
- Row-Level Security (RLS) for fine-grained access control.


## Installation

Follow these steps to set up PostgreSQL using Docker:

1. Clone the repo

```bash
git clone https://github.com/alirezatsh/devops_journey.git

```
2. Open a terminal and navigate to the installation folder:

```bash
cd devops_journey/Database/postgresql
```

3. Start the PostgreSQL container:

```bash
docker-compose up -d
```


# PostgreSQL Resources

- [Official PostgreSQL Documentation](https://www.postgresql.org/docs/)
- [PostgreSQL GitHub Repository](https://github.com/postgres/postgres)
- [PostgreSQL Docker Hub](https://hub.docker.com/_/postgres)
