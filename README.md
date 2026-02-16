# oracle_pdb_ass_II_25520_dylan

# Oracle Pluggable Database Management – Assignment II

## Student Information
- Name: Nsonera Hirwa Dylan
- Student ID: 25520
- Course: Database Development with PL/SQL (INSY 8311)
- Instructor: Eric Maniraguha
- Oracle Version: Oracle Database 21c Enterprise Edition
- Installation Type: Desktop Class (Single Instance)

---

## Assignment Overview

Demonstration of practical understanding of Oracle Architecture, mainly creation and deletion of Pluggable Databases (PDBs), user management within PDBs and usage of Oracle Enterprise Manager (OEM).

All tasks were executed individually using SQL*Plus (Command Prompt).

---

# Task 1: Create a New Pluggable Database

### PDB Name Created:
dy_pdb_25520

### Steps Performed:
1. Created pluggable database using CREATE PLUGGABLE DATABASE command.
2. Opened the PDB in READ WRITE mode.
3. Switched session to the PDB.
4. Created user:
   dylan_plsqlauca_25520
5. Granted CONNECT and RESOURCE roles.

### Result:
- PDB successfully created and opened.
- User successfully created inside the PDB.

Screenshots available in `/screenshots` folder.

---

# Task 2: Create and Delete Temporary PDB

### Temporary PDB Name:
dy_to_delete_pdb_25520

### Steps Performed:
1. Created temporary PDB.
2. Verified existence using SHOW PDBS.
3. Closed the PDB.
4. Dropped the PDB including datafiles.
5. Verified deletion successfully.

### Result:
- Temporary PDB successfully created and deleted.

Screenshots available in `/screenshots` folder.

---

# Task 3: Oracle Enterprise Manager (OEM)

- Accessed OEM via: https://localhost:5500/em
- Logged in as SYS (SYSDBA).
- Verified environment and PDB visibility.

Screenshot available in `/screenshots` folder.

---

# Challenges Faced

- Initial JDK compatibility issue with SQL Developer.
- Resolved by installing JDK 17 and configuring environment variables correctly.

No database configuration errors were encountered during PDB creation.

---

# Issues Encountered
No

---

