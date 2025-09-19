# PostgreSQL Basic Commands

This file contains basic PostgreSQL commands for managing databases, tables, and records.



## Connect to PostgreSQL

Connect to PostgreSQL server and database

```bash

psql -U postgres
psql -U <username> -h <host> -p <port> -d <database>
docker exec -it postgres-container-name psql -U postgres

```

## Manage database

Create, drop, list, and switch databases

```bash

\l
\list
\c databasename
CREATE DATABASE dbname;
DROP DATABASE dbname;
\du
CREATE USER user1 WITH PASSWORD 'pass';
DROP USER user1;
ALTER USER user1 WITH PASSWORD 'newpass';
\dt

```

## Manage tables

Create, alter, drop, and describe tables

```bash

CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(50),
    age INT
);
DROP TABLE users;
ALTER TABLE users ADD COLUMN status VARCHAR(20);
ALTER TABLE users DROP COLUMN status;
\dt
\d users


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
