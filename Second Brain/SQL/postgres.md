\\l --- to see what databases are present 
You can connect to a database by entering 
`\c database_name`

Drop your `column_name` column.
```sql
ALTER TABLE table_name DROP COLUMN column_name;
```
add a column:
```sql
ALTER TABLE table_name ADD COLUMN column_name DATATYPE;
```
rename a column:

```sql
ALTER TABLE table_name RENAME COLUMN column_name TO new_name;
```

DELETE row 
```sql 
DELETE FROM second_table WHERE username='Luigi'; 
```
