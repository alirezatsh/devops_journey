# MongoDB Backup and Restore (Docker)

Assuming you have MongoDB running in Docker with the following setup:

- Container name: `my_mongo`
- Port: `27017`
- Username: `user`
- Password: `password`
- Volume: `mongo_data`

```bash
# Backup entire MongoDB database from Docker container
docker exec my_mongo sh -c 'exec mongodump --archive' > ~/mongo_backups/mydb_backup.archive
```

```bash
# Backup a specific database
docker exec my_mongo sh -c 'exec mongodump --db myDatabase --archive' > ~/mongo_backups/myDatabase_backup.archive
```

```bash
# Restore entire database from archive
docker exec -i my_mongo sh -c 'exec mongorestore --archive' < ~/mongo_backups/mydb_backup.archive
```

```bash
# Restore a specific database from archive
docker exec -i my_mongo sh -c 'exec mongorestore --db myDatabase --archive' < ~/mongo_backups/myDatabase_backup.archive
```
