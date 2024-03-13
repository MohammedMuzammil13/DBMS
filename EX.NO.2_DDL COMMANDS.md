# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb

### SQL QUERY:
```
create database studentdb
```

### OUTPUT:

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
CREATE TABLE student (
    RegisterNumber INT PRIMARY KEY,
    Name VARCHAR(50),
    Age INT,
    Address VARCHAR(100),
    PhoneNumber VARCHAR(15)
);

INSERT INTO student (RegisterNumber, Name, Age, Address, PhoneNumber)
VALUES (1, 'John Doe', 20, '123 Main St, Cityville', '123-456-7890'), (2, 'Jane Smith', 22, '456 Elm St, Townsville', '987-654-3210');
```
### OUTPUT:
![Screenshot 2024-03-13 112011](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/628c2d3e-2cb0-423f-854f-36024b94a826)


### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
ALTER TABLE student ADD department VARCHAR(50);
```


### OUTPUT:
![Screenshot 2024-03-13 112131](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/6542f7be-fc89-4da1-b89a-1808c240f7c0)


### 4) Rename the student table to mystudent

### SQL QUERY: 
```
ALTER TABLE student RENAME TO mystudent;
```

### OUTPUT:
![Screenshot 2024-03-13 112131](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/4f43e292-7187-453c-b6d7-c89ec18b6a0e)


### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
TRUNCATE TABLE mystudent;
```
### OUTPUT:
![Screenshot 2024-03-13 112619](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/ba8ffaea-7c33-46b6-8ae7-5b1d763e10b8)

### 4) Drop the mystudent table
 
### SQL QUERY: 
```
DROP TABLE mystudent;
```

### OUTPUT:
![Screenshot 2024-03-13 112737](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/e7f7beea-03c2-43b6-8559-9e44c3fe4c04)



## Result:
         Thus the basic DDL commands in SQL are executed. 


