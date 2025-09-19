# MySQL Basic Commands

This file contains basic MySQL commands for managing databases, tables, and records.



## Connect to MySQL

Connect to MySQL server

```bash

mysql -u root -p
mysql -u <username> -h <host> -P <port> -p
docker exec -it mysql-container-name mysql -u root -p

```

## Manage databases

Create, drop, list, and switch databases

```bash

SHOW DATABASES;
CREATE DATABASE dbname;
DROP DATABASE dbname;
USE dbname;
SHOW TABLES;
CREATE USER 'user1'@'localhost' IDENTIFIED BY 'pass';
DROP USER 'user1'@'localhost';
ALTER USER 'user1'@'localhost' IDENTIFIED BY 'newpass';

```

## Manage tables

Create, alter, drop, and describe tables

```bash

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    age INT
);
DROP TABLE users;
ALTER TABLE users ADD COLUMN status VARCHAR(20);
CREATE INDEX idx_name ON users(name);
DROP INDEX idx_name ON users;
ALTER TABLE users ADD CONSTRAINT chk_age CHECK (age >= 0);
ALTER TABLE users DROP COLUMN status;
DESCRIBE users;
SHOW TABLES;

```

## Manage records

Insert, update, delete, query records

```bash

INSERT INTO users (name, age) VALUES ('Alireza', 25);
INSERT INTO users (name, age) VALUES 
  ('User1', 30),
  ('User2', 22);
SELECT * FROM users;
SELECT * FROM users WHERE age = 25;
SELECT * FROM users WHERE name LIKE 'A%';
UPDATE users SET age = 26 WHERE name = 'Alireza';
UPDATE users SET status = 'young' WHERE age < 30;
DELETE FROM users WHERE name = 'Alireza';
DELETE FROM users WHERE age < 25;
SELECT * FROM users ORDER BY age DESC;
SELECT * FROM users LIMIT 5;


```
