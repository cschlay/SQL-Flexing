# Accessing Database

Ref: https://www.postgresql.org/docs/13/tutorial-accessdb.html

I create a database I want to access name `accessdb` and open it:

```bash
docker-compose exec db createdb accessdb
docker-compose exec db psql accessdb
```

Then I would have psql shell open and I test the queries in the documentation.
