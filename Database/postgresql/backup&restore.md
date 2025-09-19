# PostgreSQL Backup and Restore (Docker)

Assuming you have PostgreSQL running in Docker with the following setup:

- Container name: `my_postgres`
- Port: `5432`
- Username: `user`
- Password: `password`
- Database: `mydb`
- Volume: `postgres_data`

```bash
# Backup entire PostgreSQL database from Docker container
docker exec my_postgres pg_dump -U user -F c mydb > ~/pg_backups/mydb_backup.dump
```

```bash
# Backup a specific schema or table (example: public schema)
docker exec my_postgres pg_dump -U user -n public mydb > ~/pg_backups/mydb_public_backup.dump
```

```bash
# Restore entire PostgreSQL database from backup
cat ~/pg_backups/mydb_backup.dump | docker exec -i my_postgres pg_restore -U user -d mydb
```

```bash
# Restore a specific schema or table from backup
cat ~/pg_backups/mydb_public_backup.dump | docker exec -i my_postgres pg_restore -U user -d mydb
```

```bash
# Optional: Compress backup
docker exec my_postgres pg_dump -U user -F c mydb | gzip > ~/pg_backups/mydb_backup.dump.gz
```

```bash
# Restore from compressed backup
gunzip -c ~/pg_backups/mydb_backup.dump.gz | docker exec -i my_postgres pg_restore -U user -d mydb
```

