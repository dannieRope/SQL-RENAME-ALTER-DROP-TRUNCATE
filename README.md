# MANIPULATING CUSTOMERINFO TABLE
## RENAME, ALTER, DROP AND TRUNCATE 

```sql
--Connect to mysql_learner Database
USE mysql_learner;

--Retrieve all records from Customerinfo table
SELECT *
FROM Customerinfo;

---Change table name to customerinfo
EXEC sp_rename Customer, customerinfo;

=--Change firstName column to f_name and LastName to L_name
EXEC sp_rename 'customerinfo.firstname', 'f_name';

EXEC sp_rename 'customerinfo.lastname','l_name';

---Change column data type
ALTER TABLE Customerinfo
ALTER COLUMN  Email VARCHAR(255);

---add a new column called fullname

ALTER TABLE customerinfo
ADD Fullname  nVARCHAR(22);

---delete the new column fullname created
ALTER TABLE customerinfo
DROP COLUMN fullname ;

---delete all records in the customerinfo table
TRUNCATE Customerinfo; 

---delete the customerinfo table 
DROP TABLE Customerinfo;

```
