## Creating a view
```sql
CREATE VIEW view_name [(column[ ,...n ])]
	[WITH <view_attribute>[ ,...n ]]
	AS select_statement
	[WITH CHECK OPTION]
	[;]
<view_attribute> ::= {
[ENCRYPTION]
[ SCHEMABINDING]
[VIEW_METADATA]
}
```

A view can be used for the following purposes
- To focus, simplify and customize the perception each user has of the database
- As a security mechanism by allowing users to access data through the view, without granting the users permissions to directly access the underlying base tables.

## Altering and removing views

## WITH CHECK OPTION
The option WITH CHECK OPTION is used to restrict the insertion of only such rows that satisfy the conditions of the query. If this option is used, the Database Engine tests every inserted row to ensure that the conditions in the WHERE clause are evaluated to TRUE.

## INSERT, UPDATE, DELETE on views