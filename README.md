# Sql server 2017

In this project have a container about sql server 2017 for developer.

## Before you beginner

Need to create a file called `.env`, your template is the fiel `.env.modelo`. Replace variables in the document.

* `%APP_NAME%`: Name about the container
* `%APP_DB_SA_PASS%`: Password of **sa** user
* `%APP_DB_PORT%`: Port mapping in your host
* `%APP_MEMORY_MAX_LIMIT%`: Limit the memory used in container (Em mb)

## Developer

> The password must have at least 8 characters, 1 of which must be uppercase/lowercase and a special character.

Follow the steps below to create login, user and database to use in the project

```sql
CREATE LOGIN <user> WITH password='<password>';
CREATE USER <user> FROM LOGIN <user>;
CREATE DATABASE <base_name>;

use <base_name>;
CREATE USER <user> FOR LOGIN <user>;
EXEC sp_addrolemember 'db_owner', '<user>';
```
