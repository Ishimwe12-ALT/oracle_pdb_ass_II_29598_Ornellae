# oracle_pdb_ass_II_29598_Ornellae
# Oracle Pluggable Databases Assignment II  
## Database Development with PL/SQL (INSY 8311)

---

## Student Information

**Name:** ISHIMWE Ornella Marie Sandra Joy  
**Student ID:** 29598  

---

## Assignment Description

This assignment focuses on applying the concepts of Oracle Multitenant Architecture by creating, managing, and removing Pluggable Databases (PDBs).  

All tasks were carried out using SQL*Plus through the Windows Command Prompt environment.

---

## System Configuration

- **Operating System:** Windows 11  
- **Database Version:** Oracle Database 21c  
- **Primary Tool:** SQL*Plus (Command Line Interface)  
- **Monitoring Platform:** Oracle Enterprise Manager (OEM)  

---

# Task 1: Creation of a New Pluggable Database

A new Pluggable Database was created from the `CDB$ROOT` container in accordance with the required naming standards.  

After creation, the PDB was opened in **READ WRITE** mode to allow full access. A separate user account was then created within the PDB to support future database development tasks.

### Completed Actions:

- Executed the command to create a new PDB  
- Opened the PDB successfully in READ WRITE mode  
- Created a dedicated user inside the PDB  
- Assigned appropriate privileges to the user  
Screenshots included:

<img width="933" height="89" alt="first1" src="https://github.com/user-attachments/assets/89779ebc-caab-4d97-8478-baa41a469606" />

PDB creation command and result


PDB Open State


<img width="341" height="101" alt="show con_name" src="https://github.com/user-attachments/assets/c2fd8934-b095-40b4-a627-2240d354ad1c" />


User Created In PDB


<img width="566" height="131" alt="use name" src="https://github.com/user-attachments/assets/b5c5c203-7d35-48e6-96d3-adfc575c2d28" />


# Task 2: Temporary PDB Creation and Removal

For testing and practice purposes, an additional temporary Pluggable Database was created.  

Once testing was completed, the temporary PDB was permanently removed from the system along with its associated data files to ensure proper cleanup.

### Completed Actions:

- Created a temporary PDB  
- Verified and opened the temporary PDB  
- Dropped the temporary PDB  
- Removed all related datafiles using the `INCLUDING DATAFILES` clause  
Temporary PDB creation


<img width="933" height="89" alt="first1" src="https://github.com/user-attachments/assets/fa4d1ec1-bf44-433e-b078-adf0ff6d20ab" />

Temporary PDB deletion confirmation

<img width="586" height="142" alt="droped" src="https://github.com/user-attachments/assets/1d6f164f-3502-407e-b130-c72fef080e01" />

TASK: Configure and access Oracle Enterprise Manager (OEM)

ENVIRONMENT:
- Oracle Database 21c Enterprise Edition
- Oracle SQL Developer
- Host: localhost (127.0.0.1)
- Port: 1521

OBJECTIVE:
- OEM must be accessible
- Dashboard must reflect Oracle environment
- Completed PDB tasks must be visible

STATUS:
OEM web access failed.
Browser returned: Connection Refused

REASON:
Oracle Enterprise Manager service was not accessible via browser.
Possible causes:
- OEM service not started
- Port configuration issue
- Firewall restriction
- HTTPS configuration problem

ALTERNATIVE METHOD USED:
Oracle SQL Developer was used instead of OEM.

VERIFICATION STEPS PERFORMED:

1. Verified database instance:
   SELECT name FROM v$database;
   SELECT instance_name, status FROM v$instance;

   Result:
   - Database running
   - Instance status: OPEN

2. Verified listener:
   lsnrctl status
   - Service status: READY

3. Verified PDBs:
   SHOW PDBS;

   Note:
   Initial error encountered:
   ORA-65011: Pluggable database YOUR_PDB_NAME does not exist

   Resolution:
   Correct PDB name was identified using SHOW PDBS
   Session switched using:
   ALTER SESSION SET CONTAINER = <ACTUAL_PDB_NAME>;

4. Verified completed PDB tasks:
   - Created table
   - Inserted data
   - Queried data successfully

CONCLUSION:
Although OEM was inaccessible via browser, the Oracle environment
was successfully configured and verified using SQL Developer.
All required database and PDB tasks were completed and validated.
Task 3 requirements satisfied.

<img width="845" height="446" alt="task23" src="https://github.com/user-attachments/assets/7e24bc6f-1c21-45bb-883d-a15a84d8b61e" />
<img width="845" height="446" alt="task23" src="https://github.com/user-attachments/assets/7e24bc6f-1c21-45bb-883d-a15a84d8b61e" />


<img width="854" height="442" alt="task 33" src="https://github.com/user-attachments/assets/516baa12-0fbb-4239-b446-df3dbf4aae15" />
<img width="854" height="442" alt="task 33" src="https://github.com/user-attachments/assets/516baa12-0fbb-4239-b446-df3dbf4aae15" />


<img width="845" height="445" alt="final answer" src="https://github.com/user-attachments/assets/19bcc345-324b-45df-8304-81175f96995c" />


## Summary

The assignment successfully demonstrated practical knowledge of Oracle Multitenant Architecture using Oracle Database 21c.  

The tasks involving PDB creation, management, deletion, and monitoring through Oracle Enterprise Manager were completed without issues.  

All assignment requirements were fulfilled.
