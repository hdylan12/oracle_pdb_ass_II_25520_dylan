# Oracle Pluggable Database – Assignment II

---

## Student Information

- **Name:** Nsonera Hirwa Dylan  
- **Student ID:** 25520  
- **Course:** Database Development with PL/SQL (INSY 8311)  
- **Instructor:** MANIRAGUHA Eric  
- **Oracle Version:** Oracle Database 21c  
- **Installation Type:** Desktop Class (Single Instance)  
- **Tool Used:** SQL*Plus (Command Prompt)  

---

## Assignment Overview

This assignment demonstrates:

- Creation of Pluggable Databases (PDBs)  
- Opening and managing PDBs  
- Creating a user inside a PDB  
- Deleting a PDB  
- Using Oracle Enterprise Manager (OEM)  

All tasks were executed individually using SQL*Plus.

---

# Task 1: Create a New Pluggable Database

## Step 1: Connect as SYSDBA

```sql
sqlplus / as sysdba
```

## Step 2: Verify Current Container

```sql
SHOW CON_NAME;
SHOW PDBS;
```

## Step 3: Create Required PDB

```sql
CREATE PLUGGABLE DATABASE dy_pdb_25520
ADMIN USER pdbadmin IDENTIFIED BY 5020
FILE_NAME_CONVERT=('pdbseed','dy_pdb_25520');
```

  **Screenshot:**  
[View PDB Creation](screenshots/1_pdb_creation.png)

## Step 4: Open the PDB

```sql
ALTER PLUGGABLE DATABASE dy_pdb_25520 OPEN;
```

## Step 5: Verify Open Mode

```sql
SHOW PDBS;
```

## Step 6: Switch to the New PDB

```sql
ALTER SESSION SET CONTAINER = dy_pdb_25520;
SHOW CON_NAME;
```

## Step 7: Create User Inside the PDB

```sql
CREATE USER dylan_plsqlauca_25520 IDENTIFIED BY password5020;
GRANT CONNECT, RESOURCE TO dylan_plsqlauca_25520;
```

  **Screenshot:**  
[View User Creation](screenshots/1_user_creation.png)

---

# Task 2: Create and Delete Temporary PDB

## Step 1: Switch Back to Root Container

```sql
ALTER SESSION SET CONTAINER = CDB$ROOT;
```

## Step 2: Create Temporary PDB

```sql
CREATE PLUGGABLE DATABASE dy_to_delete_pdb_25520
ADMIN USER tempadmin IDENTIFIED BY password5020
FILE_NAME_CONVERT=('pdbseed','dy_to_delete_pdb_25520');
```

  **Screenshot:**  
[View Temporary PDB Created](screenshots/2_temp_pdb_created.png)

## Step 3: Open and Verify

```sql
ALTER PLUGGABLE DATABASE dy_to_delete_pdb_25520 OPEN;
SHOW PDBS;
```

## Step 4: Close and Drop the Temporary PDB

```sql
ALTER PLUGGABLE DATABASE dy_to_delete_pdb_25520 CLOSE IMMEDIATE;
DROP PLUGGABLE DATABASE dy_to_delete_pdb_25520 INCLUDING DATAFILES;
SHOW PDBS;
```

  **Screenshot:**  
[View Temporary PDB Deleted](screenshots/2_temp_pdb_deleted.png)

---

# Task 3: Oracle Enterprise Manager (OEM)

Oracle Enterprise Manager Database Express (OEM) was accessed through the browser to monitor the Oracle environment and confirm pluggable database operations.

Access URL:

```
https://localhost:5500/em
```

  **Screenshot:**  
[View OEM Dashboard](screenshots/3_oem_dashboard.png)

---

# Challenges Faced

- SQL Developer JDK compatibility issue  

No errors were encountered during PDB creation or deletion.

---

# Issues Encountered

None

---

# PDB Created

```
dy_pdb_25520
```

---

# Academic Integrity Statement

I confirm that this assignment was completed independently.  
All commands were executed and documented by myself without copying from classmates or external repositories.

---

# Repository Link

https://github.com/hdylan12/oracle_pdb_ass_II_25520_dylan
