## File system limitations

Understanding the limitations enables us to understand the development of modern databases.
Failure to realize that many shortcomings are not unique to file systems will result in them re-appearing in databases, even though db technology makes it easier to avoid them.

1.  Lengthy development times
- Even simple data-retrieval required extensive programming.

2. Long wait times for answers
- Because of problem no.1

3.  Complex system administration
- Each file requires it's own file management programs to be developed and maintained.

4. Lack of security, limited data share
- Sharing data introduces a lot of security risks. Security and data-sharing features are difficult to program and therefore often omitted from file systems.

5.  Extensive programming
- Any change to a file structure forces modifications to all the programs that are accessing that file.
    

## Data redundancy
When the same data are stored unnecessarily at different places. 
Sets the stage for data inconsistency and poor data security.
 
## Data inconsistency
When different and conflicting versions of the same data appear in different places.

## Field, record, file
**Field:** A character or group of characters. Used to define and store data.
**Record:** A logically connected set of one or more fields.
**File:** A collection of related records.

## DBMS
1. A collection of programs that manage the database structure and control access to the data stored in the database.
2. It is the intermediary between the user and the database.
3. Enables the data to be shared among many applications/users.
4. Integrates different views of the data into one data reposository.
5. Minimizes data inconsistency.

**Functions (not all)**
1. Data dictionary management
2. Security management
3. Backup and recovery management

## Query
A specific request for data manipulation.

## Meta-data
Data about data, through which the end-user data are integrated and managed.

## Data dictionary
-Contains definitions of the data elements and their relationships.