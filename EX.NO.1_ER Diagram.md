# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE 06-03-24
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![image (2)](https://github.com/DrUmaRaniV/DBMS/assets/119291664/d60bcaf9-241f-4919-9759-bf4f8c765122)



### Relational model
![image (3)](https://github.com/DrUmaRaniV/DBMS/assets/119291664/2b350748-15be-4d15-96a1-a05838514b25)



### SQL DDL Schema 
CREATE TABLE College
(
  CName INT NOT NULL,
  COffice INT NOT NULL,
  CPhone INT NOT NULL,
  PRIMARY KEY (CName)
);

CREATE TABLE Instructor
(
  Id INT NOT NULL,
  Name INT NOT NULL,
  Phone INT NOT NULL,
  PRIMARY KEY (Id),
  UNIQUE (Phone)
);

CREATE TABLE Department
(
  DName INT NOT NULL,
  DCode INT NOT NULL,
  PRIMARY KEY (DName),
  UNIQUE (DCode)
);

CREATE TABLE Student
(
  Name INT NOT NULL,
  Id INT NOT NULL,
  Phone INT NOT NULL,
  Address INT NOT NULL,
  PRIMARY KEY (Id),
  UNIQUE (Phone)
);

CREATE TABLE Section
(
  Sem INT NOT NULL,
  SecID INT NOT NULL,
  SecNo INT NOT NULL,
  Year INT NOT NULL,
  PRIMARY KEY (SecID)
);

CREATE TABLE Course
(
  CCode INT NOT NULL,
  Credits INT NOT NULL,
  CoName INT NOT NULL,
  PRIMARY KEY (CCode),
  UNIQUE (CoName)
);

## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
