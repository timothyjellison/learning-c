# MySQL Katas

In *The Clean Coder* Uncle Bob recommends deliberate practice to master basic skills and keep them sharp. Running through these katas once every few days should keep you feeling comfortable performing basic CRUD operations in MySQL.

## Katas
1. List all databases
2. Create a new database
3. Create a new table in the new database with fields firstname, lastname, and age
4. List all the tables in the new database
5. Add two rows, one for yourself and one for a friend
6. Query the table for the firstname of anyone who under 30 years old
7. Add a column isProgrammer that only holds values true/false
8. Update your two rows so one has isProgrammer true and the other has isProgrammer false
9. Delete one of the rows from your table
10. Delete the new database

## Tips

1. Remember that to you can stretch your commands across multiple lines by pressing <kbd>Enter</kbd>. The command won't execute until you add a semicolon <kbd>;</kbd>
2. Run through these same katas using a variety of tools: definitely in the mysql console but also try them in a client like [MySQL Workbench](https://www.mysql.com/products/workbench/) or [Sequel Pro](https://www.sequelpro.com/) and through client library like [mysql for Node](https://www.npmjs.com/package/mysql) or [MySQL Connector for Python](https://dev.mysql.com/doc/connector-python/en/).
3. These are very basic operations but they're the most powerful. 80% of your usecases are covered by 20% of the functionality.

## Solutions

### List all databases
```sql
SHOW DATABASES;
```

### Create a new database
```sql
CREATE DATABASE mydatabasename;
```

### Use a database
```sql
USE mydatabasename;
```

### Create a new table
```sql
CREATE TABLE mytablename
(
firstname VARCHAR(20),
lastname VARCHAR(20),
age SMALLINT
);
```

### Show all the tables
```sql
SHOW TABLES;
```

### Insert a row
```sql
INSERT INTO mytablename (firstname, lastname, age, isProgrammer)
VALUES ('Grace', 'Hopper', 43, true);
```

### Conditional query
```sql
SELECT firstname
FROM mytablename
WHERE age < 30;
```

### Add a column
```sql
ALTER TABLE mytablename
ADD COLUMN isProgrammer BOOLEAN
AFTER age;
```

### Update column in a specific row
```sql
UPDATE mytablename
SET isProgrammer = TRUE
WHERE firstname = 'Grace';
```

### Delete a row
```sql
DELETE FROM mytablename
WHERE isProgrammer <> TRUE;
```

### Delete the new database
```sql
DROP DATABASE mydatabasename;
```

## Happy Coding!
You can find me over at [timothyellison.com](https://www.timothyellison.com/)
