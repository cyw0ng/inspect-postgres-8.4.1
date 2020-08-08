# Test Env

- Test Container

```
docker run --name postgres-8.4.1 -p 8080:8080 -p 5432:5432 -e POSTGRES_PASSWORD=postgres841 -d postgres:8.4
```