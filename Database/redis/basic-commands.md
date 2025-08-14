# Redis Basic Commands

This file contains basic Redis commands for managing databases, keys, and values.

---

## Connect to Redis

Connect to Redis server

```bash

redis-cli
redis-cli -h <host> -p <port> -a <password>
docker exec -it redis-container-name redis-cli

‍‍```

## Manage database

Select, flush, and check databases

```bash

SELECT 0
SELECT 1
FLUSHDB
FLUSHALL
DBSIZE

```

## Manage keys

Set, get, delete, and list keys

```bash

SET key1 "value1"
GET key1
DEL key1
EXISTS key1
KEYS *
RENAME key1 key2
EXPIRE key1 60
TTL key1

```

## Manage data types

Work with strings, hashes, lists, sets, and sorted sets

```bash

# Strings
SET name "Alireza"
GET name

# Hashes
HSET user:1 name "Alireza" age 25
HGETALL user:1

# Lists
LPUSH mylist "item1"
RPUSH mylist "item2"
LRANGE mylist 0 -1
LPOP mylist
RPOP mylist

# Sets
SADD myset "val1"
SADD myset "val2"
SMEMBERS myset
SREM myset "val1"

# Sorted Sets
ZADD myzset 1 "one"
ZADD myzset 2 "two"
ZRANGE myzset 0 -1 WITHSCORES
ZREM myzset "one"


```

## Expire and persistence

Set expiration and save data

```bash

EXPIRE key1 300
TTL key1
PERSIST key1
SAVE
BGSAVE

```