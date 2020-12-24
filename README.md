# SQL-Flexing
Trying out every feature from PostgreSQL with e-commerce database and writing own access model for SQL queries.

## Database installation

I use Docker image on development port `5000` in non-detached mode to prevent accidental deletions.

```bash
docker-compose up
```

To recreate empty database

```bash
docker-compose rm
docker-compsoe up
```

The connections credentials are

```
Host: 127.0.0.1
Port: 5000
User: postgres
Password: sqlflexpw
Database: postgres
```

Connect with DataGrip or PgAdmin.