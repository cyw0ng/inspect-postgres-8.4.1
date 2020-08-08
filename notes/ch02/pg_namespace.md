# pg_namespace

- pg_namespace query result, init'ed by initdb
```
> SELECT * FROM pg_catalog.pg_namespace;

nspname           |nspowner|nspacl                             |
------------------|--------|-----------------------------------|
pg_catalog        |      10|{postgres=UC/postgres,=U/postgres} |
pg_toast          |      10|NULL                               |
public            |      10|{postgres=UC/postgres,=UC/postgres}|
pg_temp_1         |      10|NULL                               |
pg_toast_temp_1   |      10|NULL                               |
information_schema|      10|{postgres=UC/postgres,=U/postgres} |
```

- original code: src/include/catalog/pg_namespace.h

```C
DATA(insert OID = 11 ( "pg_catalog" PGUID _null_ ));
DESCR("system catalog schema");
#define PG_CATALOG_NAMESPACE 11
DATA(insert OID = 99 ( "pg_toast" PGUID _null_ ));
DESCR("reserved schema for TOAST tables");
#define PG_TOAST_NAMESPACE 99
DATA(insert OID = 2200 ( "public" PGUID _null_ ));
DESCR("standard public schema");
#define PG_PUBLIC_NAMESPACE 2200
```