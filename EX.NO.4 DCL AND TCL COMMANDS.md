# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE: 27/03/24
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
```
exec savepoint s1;
```

### OUTPUT:
![Screenshot 2024-03-20 111724](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/a144b6b7-9cba-4601-a3a3-82ad94ee92bc)


### Q4) Perform insertion into employee table.

### QUERY:
```
INSERT INTO employee (employee_id, name, address) VALUES (1, 'Muzammil', 'Chennai');
INSERT INTO employee (employee_id, name, address) VALUES (2, 'Prem', 'Salem');
INSERT INTO employee (employee_id, name, address) VALUES (3, 'Stanley', 'Chennai');
```


### OUTPUT:
![Screenshot 2024-03-20 110206](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/e489e0fe-3bc3-475f-8489-48f1188d0748)


### Q6)	Display the employee table and create a save point s2 .


### QUERY:
```
select * from employee;
exec savepoint s2;
```
### OUTPUT:
![Screenshot 2024-03-20 112048](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/5a661cbf-326e-483d-8156-6a213faa8ee4)

### Q7)	Perform updation on any one of the row.


### QUERY:
```
UPDATE employee
SET address = 'Bangalore'
WHERE employee_id = 3;
```
### OUTPUT:
![Screenshot 2024-03-20 112313](https://github.com/MohammedMuzammil13/DBMS/assets/119291664/fbf895bc-8d95-4d41-9e08-c8aeb31c9ae3)

### Q8) Display the employee table and rollback to  save point s2 


### QUERY:
```python
sql
select * from employee;
rollback to s2;
```

### OUTPUT:
![image](https://github.com/Lakshmipriya2005/DBMS/assets/115525361/b66b2852-7cbc-49e6-a059-579485f3ff49)


### Q9) Display the employee table and commit the changes; 


### QUERY:
```python
sql
select * from employee;
commit;
```

### OUTPUT:
![image](https://github.com/Lakshmipriya2005/DBMS/assets/115525361/7dd55645-f515-4c5b-9174-1b3a9bc24e30)


### Q10) Rollback to save point s1;

### QUERY:
```python
sql
rollback to A;
```

### OUTPUT:
![image](https://github.com/Lakshmipriya2005/DBMS/assets/115525361/441afff5-9f95-418b-ad8b-c2b5cfbf810d)


### Q11)	Create a new user and grant access to any one database with "insert and update"


### QUERY:
```sql
CREATE USER new_user;
GRANT INSERT, UPDATE ON database_name TO new_user;
```

### OUTPUT:
![image](https://github.com/Yuvaraj878/DBMS/assets/118622554/3c3761a5-28c0-4c83-a203-89e0087e6676)

![image](https://github.com/Yuvaraj878/DBMS/assets/118622554/fd08ac3a-d1a5-4a16-af6a-f3bc5ff24629)


### Q12) Check the user access and display the result 


### QUERY:
```sql
SHOW GRANTS FOR new_user;
```

### OUTPUT:
![image](https://github.com/Yuvaraj878/DBMS/assets/118622554/2fbd5d94-7610-4828-a072-c84372c06442)


### Q13) Revoke the privillages.

### QUERY:
```sql
SHOW GRANTS FOR new_user;
REVOKE INSERT, UPDATE ON database_name FROM new_user;
SHOW GRANTS FOR new_user;
```

### OUTPUT:
![image](https://github.com/Yuvaraj878/DBMS/assets/118622554/bd4b2b58-817e-42ea-b84d-a59af0382c11)

## RESULT :
Thus the basic TCL and DCL commands are executed.
