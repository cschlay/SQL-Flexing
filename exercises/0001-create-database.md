# Creating the Database

Ref: https://www.postgresql.org/docs/13/tutorial-createdb.html

First, I need to connect to the shell that has access to the database. The docker-compose shell need to be open too.

In Docker to run any Postgres command I need to first open the shell

```bash
docker-compose exec db bash
```

The commands `createdb` and `dropdb` are to be run directly in the shell. For that purpose permissions need to exist and roles need to be properly set for the __Operating System__ user. So the user need to be properly set up first.

Because Docker container uses `root` user we give him permissions to create databases. In real-life non-root users will be given the permission.

```bash
psql -U postgres
CREATE USER root; # In real-life, replace root with your username.
ALTER USER root SUPERUSER CREATEDB;
```

After that commands `createdb` and `dropdb` should work, the are run in normal shell not psql

```bash
docker-compose exec db createdb main
docker-compose exec db dropdb main
```
