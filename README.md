# Database-Creation-Deletion-OEM
### Create a New Pluggable Database (PDB) 'plsql_class2024db' AND 'he_to_delete_pdb'

```sql
 CREATE PLUGGABLE DATABASE plsql_class2024db
  2  ADMIN USER he_plsqlauca IDENTIFIED BY oracle
  3  FILE_NAME_CONVERT = ('C:\ORACLE\ORADATA\ORCL\PDBSEED\',
  4                       'C:\ORACLE\ORADATA\ORCL\newpdb\');
```
