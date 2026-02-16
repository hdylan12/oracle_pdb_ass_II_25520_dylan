# Oracle Pluggable Database Management – Assignment II

## Student Information
- Name: Nsonera Hirwa Dylan
- Student ID: 25520
- Course: Database Development with PL/SQL (INSY 8311)
- Instructor: MANIRAGUHA Eric
- Oracle Version: Oracle Database 21c 
- Installation Type: Desktop Class (Single Instance)
- Tool Used: SQL*Plus (Command Prompt)

---

## Assignment Overview

- Creation of Pluggable Databases (PDBs)
- Opening and managing PDBs
- User creation inside a PDB
- Deletion of a PDB
- Usage of Oracle Enterprise Manager (OEM)

All tasks were executed individually using SQL*Plus.

---

# Task 1: Create a New Pluggable Database

## Step 1: Connect as SYSDBA, Verify Container, Create PDB

```sql
sqlplus / as sysdba

SHOW CON_NAME;
SHOW PDBS;

CREATE PLUGGABLE DATABASE dy_pdb_25520
ADMIN USER pdbadmin IDENTIFIED BY 5020
FILE_NAME_CONVERT=('pdbseed','dy_pdb_25520');
