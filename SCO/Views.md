## Creating a view
```sql
CREATE VIEW view SELECT ... FROM ... WHERE ...
```
A view can be used for the following purposes
- To focus, simplify and customize the perception each user has of the database
- As a security mechanism by allowing users to access data through the view, without granting the users permissions to directly access the underlying base tables.

## Altering and removing views
```sql
ALTER VIEW view AS
     SELECT ...
     FROM ...
     WHERE ...
```
```sql
DROP VIEW view
```
## WITH CHECK OPTION
The option WITH CHECK OPTION is used to restrict the insertion of only such rows that satisfy the conditions of the query. If this option is used, the Database Engine tests every inserted row to ensure that the conditions in the WHERE clause are evaluated to TRUE.

## INSERT, UPDATE, DELETE on views
```sql
INSERT INTO view(fields) VALUES(...)
```
```sql
UPDATE view SET ... WHERE ...
```
```sql
DELETE FROM view WHERE ...
```
## Permissions
```sql
GRANT permission ON view TO user
```