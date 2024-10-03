# Database-Creation-Deletion-OEM
### Create a New Pluggable Database (PDB) 'plsql_class2024db' AND 'pa_to_delete_pdb'

```sql
 CREATE PLUGGABLE DATABASE plsql_class2024db
  2  ADMIN USER PA_plsqlauca IDENTIFIED BY 1234
  3  FILE_NAME_CONVERT = ('C:\ORACLE\ORADATA\ORCL\PDBSEED\',
  4                       'C:\ORACLE\ORADATA\ORCL\newpdb\');
```
## This command creates a new PDB, plsql_class2024db.
Admin User: PA_plsqlauca is the administrative user created for this PDB, with the password oracle.
![SQL ASSIGNMENT 1](https://github.com/user-attachments/assets/33a641ea-3b43-489c-9aed-47247c5985a6)
## Testing database connection
![pa](https://github.com/user-attachments/assets/ecf30a5c-7e68-4ce2-ad98-72993f1ebc13)

```sql
CREATE PLUGGABLE DATABASE PA_TO_DELETE_PDB
  2  ADMIN USER PA_plsqlauca IDENTIFIED BY 1234
  3  FILE_NAME_CONVERT=('C:\USERS\ORADATA\ORCL\PDBSEED\',
  4                     'C:\USERS\ORADATA\ORCL\PDBSEED\newpdb1\');
```
![SQL ASSIGNMENT 2](https://github.com/user-attachments/assets/6dc75794-fefc-4b0c-84b9-7074db572708)

```sql
ALTER PLUGGABLE DATABASE FA_TO_DELETE_PDB UNPLUG INTO 'C:\USERS\ORADATA\ORCL PDB_DEMO.XML';
DROP PLUGGABLE DATABASE FA_TO_DELETE_PDB INCLUDING DATAFILES;
```
![SQL ASSIGNMENT 3](https://github.com/user-attachments/assets/7c34683a-603a-4082-89d9-2fcb94bd1c22)
## CREATE USER
```sql
CREATE USER pacience IDENTIFIED BY 1234;
GRANT ALL PRIVILEGES TO pacience;
```
```sql
BEGIN
  2  DBMS_XDB_CONFIG.SETHTTPPORT(8080);
  3  DBMS_XDB_CONFIG.SETHTTPSPORT(5500);
  4  END;
  5  /
```
```sql
SELECT DBMS_XDB_CONFIG.GETHTTPPORT() AS HTTP_PORT,
  2         DBMS_XDB_CONFIG.GETHTTPSPORT() AS HTTPS_PORT
  3  FROM DUAL;
```
![SQL ASSIGNMENT 4](https://github.com/user-attachments/assets/4fbdcaa2-6290-49b2-9a2f-1c2b3125fdca)
