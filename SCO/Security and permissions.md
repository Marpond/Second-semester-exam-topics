## Authentication/Authorization
The Database Engine’s security system includes two different security subsystems:
1. Windows security
	- Operating system level security
2. Database Engine security
	- System level security, defines an SQL Server login

**1. Windows authentication**
Specifies security at the operating system level, in other words logging in can be done with a Windows account.

**2. SQL Server authentication**
Created within the system and is associated with a password, mostly used for backward compatibility.
Some logins are identical to the existing user accounts.

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
When several users need to perform similar activities in a particular database (and there is no corresponding Windows group), we can add a database role, which specifies a group of database users that can access the same objects of the database.

Members of a database role can be any of the following:
- Windows groups and user accounts
- Logins
- Other roles

The security architecture in the Database Engine includes several “system” roles that
have special implicit permissions. There are two types of predefined roles (in addition
to user-defined roles):
- Fixed server roles
- Fixed database roles

Beside these two, the following sections also describe the following types of roles:
- Application roles
- User-defined server roles
- User-defined database roles

## The “sa” login account
System administrator is a special login provided for backward compatibility. By default, it is assigned to the sysadmin fixed server role and cannot be changed. The sa login is the login to which was granted all possible permissions for system administration tasks.

## Permissions GRANT, REVOKE, DENY
The **GRANT** statement grants permissions to securables.
```sql
USE sample;
GRANT CREATE TABLE, CREATE PROCEDURE
	TO peter, mary;
```
The **DENY** statement prevents users from performing actions. This means that the
statement removes existing permissions from user accounts or prevents users from
gaining permissions through their group/role membership that might be granted in the
future.
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