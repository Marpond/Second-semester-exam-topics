## Authentication/Authorization
The Database Engine’s security system includes two different security subsystems:
1. Windows security
	- Operating system level security
2. Database Engine security
	- System level security, defines an SQL Server login

1. **Windows authentication**
OS level security, logging in can be done with a Windows account.

2. **SQL Server authentication**
Created within the system and is associated with a password, mostly used for backward compatibility.

**Database Engine authentication modes**
1. Windows mode (trusted mode)
2. Mixed mode

## CREATE LOGIN
```sql
create login login_name with password = 'password' go
```

## CREATE USER
```sql
create user user_name for login login_name
```

## ROLES
When several users need to perform similar activities in a database, we can add a database role, which specifies a group of database users that can access the same objects of the database.

Members of a database role can be:
- Windows groups and user accounts
- Logins
- Other roles

The security architecture in the Database Engine includes several “system” roles that have special implicit permissions:

**Fixed server roles**
Defined at the server level and exist outside of databases.
- sysadmin
- dbcreator

**Fixed database roles**
Defined at the database level and therefore exist in each database.
- db_owner
- db_ddladmin

Beside these two, there are also:

1. **Application roles**
 Allows application to take responsibility of authenticating instead of the database system.
 
2. **User-defined server roles**
3. **User-defined database roles**

## The “sa” login account
System administrator is a special login provided for backward compatibility. By default, it is assigned to the sysadmin fixed server role and cannot be changed. The sa login is the login to which was granted all possible permissions for system administration tasks.

## Permissions GRANT, REVOKE, DENY
The **GRANT** statement grants permissions to securables.
```sql
USE sample;
GRANT CREATE TABLE, CREATE PROCEDURE
	TO peter, mary;
```

The **DENY** statement prevents users from performing actions. This means that the statement removes existing permissions from user accounts or prevents users from gaining permissions through their group/role membership that might be granted in the future.
```sql
USE sample;
DENY CREATE TABLE, CREATE PROCEDURE
	TO peter, mary;
```

The **REVOKE** statement removes one or more previously granted or denied
permissions.
```sql
USE sample;
REVOKE CREATE TABLE, CREATE PROCEDURE
	TO peter, mary;
```