# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE:
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## Data Control Language (DCL) commands
* Data control language (DCL) is used to access the stored data.
* It is mainly used for revoke and to grant the user the required access to a database.
## List of DCL commands: 
1. GRANT : It is used to insert data into a table.
2. REVOKE: It is used to update existing data within a table.
## Transaction control language(TCL) commands
1. COMMIT : COMMIT command in SQL is used to save all the transaction-related changes permanently to the disk
2. START TRANSACTION : to start the transaction
3. ROLLBACK : undo the transaction upto savepoint 
4. SAVEPOINT : create a savepoint to save the different parts of the same transaction using different names

### Q1) Create a table employee with employee id ,name and Address

### QUERY:
```
CREATE TABLE employee (
    employee_id INT PRIMARY KEY,
    name VARCHAR(40),
    address VARCHAR(40)
);
```
### OUTPUT:
![Screenshot 2024-03-20 105918](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/ada15580-75ab-4dda-9f50-87fae59d59b2)



### Q2) Insert three rows into emploee table 


### QUERY:
```
INSERT INTO employee (employee_id, name, address) VALUES (1, 'Muzammil', 'Chennai');
INSERT INTO employee (employee_id, name, address) VALUES (2, 'Prem', 'Salem');
INSERT INTO employee (employee_id, name, address) VALUES (3, 'Stanley', 'Chennai');
```




### OUTPUT:
![Screenshot 2024-03-20 110206](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/e489e0fe-3bc3-475f-8489-48f1188d0748)


### Q3) Start the transaction and create a save point s1.

### QUERY:


### OUTPUT:

### Q4) Perform insertion into employee table.

### QUERY:


### OUTPUT:


### Q6)	Display the employee table and create a save point s2 .


### QUERY:


### OUTPUT:


### Q7)	Perform updation on any one of the row.


### QUERY:


### OUTPUT:


### Q8) Display the employee table and rollback to  save point s2 


### QUERY:


### OUTPUT:


### Q9) Display the employee table and commit the changes; 


### QUERY:


### OUTPUT:


### Q10) Rollback to save point s1;


### QUERY:


### OUTPUT:


### Q11)	Create a new user and grant access to any one database with "insert and update"


### QUERY:


### OUTPUT:


### Q12) Check the user access and display the result 


### QUERY:


### OUTPUT:

### Q13) Revoke the privillages.

### QUERY:


### OUTPUT:


## RESULT :
Thus the basic TCL and DCL commands are executed.
