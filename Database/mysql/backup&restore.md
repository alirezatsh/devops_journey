# MySQL Backup and Restore (Docker)

Assuming you have MySQL running in Docker with the following setup:

- Container name: `my_mysql`
- Port: `3306`
- Root Password: `1234`
- Database: `mydb`
- User: `user`
- User Password: `password`
- Volume: `mysql_data`

```bash
# Backup entire MySQL database from Docker container
docker exec my_mysql mysqldump -u root -p1234 mydb > ~/mysql_backups/mydb_backup.sql

# Backup a specific database user (example: user)
docker exec my_mysql mysqldump -u user -ppassword mydb > ~/mysql_backups/mydb_user_backup.sql

# Restore entire MySQL database from backup
cat ~/mysql_backups/mydb_backup.sql | docker exec -i my_mysql mysql -u root -p1234 mydb

# Restore a specific database or user backup
cat ~/mysql_backups/mydb_user_backup.sql | docker exec -i my_mysql mysql -u user -ppassword mydb
