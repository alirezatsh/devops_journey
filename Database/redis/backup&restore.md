# Redis Backup and Restore (Docker)

Assuming you have Redis running in Docker with the following setup:

- Container name: `my_redis`
- Port: `6379`
- Password: `1234`
- Volume: `redis_data`

```bash
# Backup Redis database (save RDB snapshot)
docker exec my_redis redis-cli -a 1234 SAVE
```

```bash
# Copy the dump.rdb file from container to host
docker cp my_redis:/data/dump.rdb ~/redis_backups/dump_$(date +%F_%H-%M-%S).rdb
```

```bash
# Restore Redis database (copy dump.rdb into container)
docker cp ~/redis_backups/dump_2025-09-19_18-00-00.rdb my_redis:/data/dump.rdb
```

```bash
# Restart container to load restored data
docker restart my_redis
```