# Conocer el Host Name en Oracle

```sql
SELECT host_name FROM v$instance;
```

# Listado de tables

```sql
SELECT table_name, owner FROM all_tables ORDER BY owner, table_name
```
