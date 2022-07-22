## MySql Grants:

For MySql57 `Access denied for user 'root'@'localhost'` issue:
- run following before creating database. If database already created, drop database and create
after running this command.

```sql
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'password';
```
