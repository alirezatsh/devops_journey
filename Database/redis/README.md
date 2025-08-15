# Redis Overview

## What is Redis?
Redis is an open-source, in-memory data structure store used as a database, cache, and message broker.  
It supports various data types such as strings, hashes, lists, sets, sorted sets, bitmaps, and hyperloglogs, making it versatile and extremely fast.


## How Redis Works
- In-Memory Storage: Stores data in RAM for ultra-low latency access.
- Key-Value Store: Data is organized as key-value pairs.
- Persistence: Offers snapshotting (RDB) and append-only file (AOF) for durability.
- Pub/Sub Messaging: Supports message broadcasting and event notification.
- High Performance: Handles millions of operations per second with low latency.


## Key Features
- Extremely fast read and write operations.
- Simple key-value access and advanced data structures.
- Persistence via RDB snapshots and AOF logs.
- Replication and high availability through Redis Sentinel.
- Cluster mode for horizontal scaling and partitioning.
- Lightweight and easy to deploy in containers.


## Use Cases
- Caching layer to reduce database load.
- Session management for web applications.
- Real-time analytics dashboards.
- Message queues and pub/sub systems.
- Leaderboards and counting systems in games.
- Rate limiting and counters for APIs.


## Disadvantages
- Data stored in memory, so limited by RAM size.
- Persistence is optional; full durability requires AOF or snapshots.
- Not ideal for complex relational queries.
- Cluster management requires careful planning.
- Large datasets may require sharding or external storage.


## Best Compatibility
Redis works well with:
- Python (via redis-py)
- Node.js (via ioredis or node_redis)
- Java (via Jedis or Lettuce)
- Go, PHP, Ruby, C#, Kotlin — official and community clients.
- Docker and Kubernetes for containerized deployments.


## Stability and Reliability
- Mature and widely used in production since 2009.
- Redis Sentinel provides automatic failover.
- Replication ensures high availability.
- Optional persistence for durability in case of crashes.


## Load and Scalability
- In-memory nature allows extremely high throughput.
- Can handle millions of requests per second on commodity hardware.
- Supports clustering for distributing large datasets across multiple nodes.
- Low latency: typically sub-millisecond response times.


## Data Size Limits
- Limited by available RAM.
- Maximum string value: 512 MB.
- Practical dataset size depends on memory and cluster design.


## Benchmark Performance
Note: Performance depends on hardware, dataset size, and network configuration.

- Reads/Writes: Millions of operations per second for small keys/values.
- Latency: Typically sub-millisecond for both reads and writes.
- Pub/Sub: Efficient message broadcasting to thousands of subscribers.


## Security
- Authentication with `requirepass`.
- Access control lists (ACLs) for fine-grained permissions.
- TLS/SSL support for encrypted in-transit data.
- Protected mode and network binding for restricted access.


## Installation

Follow these steps to set up Redis using Docker:

1. Clone the repo

```bash
git clone https://github.com/alirezatsh/devops_journey.git

```
2. Open a terminal and navigate to the installation folder:

```bash
cd devops_journey/Database/redis
```

3. Start the Redis container:

```bash
docker-compose up -d
```


## Redis Resources

- [Official Redis Documentation](https://redis.io/docs/)
- [Redis GitHub Repository](https://github.com/redis/redis)
- [Redis Docker Hub](https://hub.docker.com/_/redis)
