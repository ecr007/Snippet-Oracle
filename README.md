# Conocer el Host Name en Oracle

```sql
SELECT host_name FROM v$instance;
```

# Listado de tables

```sql
SELECT table_name, owner FROM all_tables ORDER BY owner, table_name
```

## Check all Views

```sql
SELECT 
    c.owner,
    c.table_name AS view_name,
    c.column_name,
    c.data_type,
    c.data_length,
    c.data_precision,
    c.data_scale,
    c.nullable
FROM all_tab_columns c
JOIN all_views v 
    ON c.owner = v.owner AND c.table_name = v.view_name
ORDER BY c.owner, c.table_name, c.column_id;
```
