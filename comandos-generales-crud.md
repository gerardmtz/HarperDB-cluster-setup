## CRUD Basic SQL operations

The SQL parser is still actively being developed, many SQL features may not be optimized or utilize indexes. This document will be updated as more features and functionality becomes available. Generally, the **REST interface** provides a more stable, secure, and performant interface for data interaction, but the SQL functionality can be useful for administrative ad-hoc querying, and utilizing existing SQL statements.

HarperDB adheres to the concept of database & tables. This allows developers to isolate table structures from each other all within one database.

The basic CRUD SQL operations that could be used are

- **Create (Insert):** To insert a new record into a table, you can use the INSERT statement

```json
{
  "operation": "sql",
  "sql": "INSERT INTO dev.dog (id, dog_name) VALUES (22, 'Simon')"
}
```

- **Read (Select):** To query data from the database, you can use the SELECT statement

```json
{
  "operation": "sql",
  "sql": "SELECT * FROM dev.dog WHERE id = 1"
}
```

- **Update:** To change the values of specified attributes in one or more rows in a database table, you can use the UPDATE statement

```json 
{
  "operation": "sql",
  "sql": "UPDATE dev.dog SET dog_name = 'penelope' WHERE id = 1"
}
```

- **Delete:** To remove one or more rows of data from a database table, you can use the DELETE statement

```json
{
  "operation": "sql",
  "sql": "DELETE FROM dev.dog WHERE id = 1"
}
```

