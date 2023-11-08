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
sql
create table employee(
emp_id numeric,
emp_name varchar(10),
addr varchar(40)
);
```

### OUTPUT:
![276302151-56bbda44-a582-42e3-9738-5b1d035dd675](https://github.com/swathi22003343/DBMS/assets/120440439/81e5572b-98be-4bb4-a617-ce87fb3723b0)

### Q2) Insert three rows into emploee table 


### QUERY:
```
sql
insert into employee values(1,'Luffy','EastBlue');
insert into employee values(2,'Shanks','GodValley');
insert into employee values(3,'Grap','MarinFord');
```
### OUTPUT:
![276302974-db081e71-759d-44df-b847-75294a2e2a34](https://github.com/swathi22003343/DBMS/assets/120440439/24436907-9c10-4628-b2e8-cb12a7ae19b5)

### Q3) Start the transaction and create a save point s1.

### QUERY:

sql

savepoint A;
### OUTPUT:
![276303398-d491985f-d652-4510-baba-69bda39920c4](https://github.com/swathi22003343/DBMS/assets/120440439/27d47f3f-0178-49f7-9194-bac6110ce891)

### Q4) Perform insertion into employee table.

### QUERY:
```
sql
insert into employee(4,'Robin','EniesLobby');
```
### OUTPUT:

![276303961-b9d81949-f840-4fb4-8427-6c5efb79da74](https://github.com/swathi22003343/DBMS/assets/120440439/02142cce-f02b-4aad-80b9-7cf174de6f99)

### Q6)	Display the employee table and create a save point s2 .


### QUERY:
```
sql
select * from employee;
savepoint s2;
```

### OUTPUT:

![276304509-bc86bb69-d7ad-4193-aeda-050214882984](https://github.com/swathi22003343/DBMS/assets/120440439/47b85b21-24d6-4598-8b8f-27a7c2d4f9c0)

### Q7)	Perform updation on any one of the row.


### QUERY:
```
sql
update employee set emp_name='Nico Robin' where emp_id=4;
```

### OUTPUT:

![276305358-2e9e6855-56ea-40f4-ba36-56f8eafd68ee](https://github.com/swathi22003343/DBMS/assets/120440439/d5fa8de9-ca15-46ab-b801-ad1d92366039)

### Q8) Display the employee table and rollback to  save point s2 


### QUERY:
```
sql
select * from employee;
rollback to s2;
```

### OUTPUT:

![276305855-b66b2852-7cbc-49e6-a059-579485f3ff49](https://github.com/swathi22003343/DBMS/assets/120440439/8950d77b-82a2-4c83-b09a-a0b1f65a1730)

### Q9) Display the employee table and commit the changes; 


### QUERY:
```
sql
select * from employee;
commit;
```
### OUTPUT:

![276306207-7dd55645-f515-4c5b-9174-1b3a9bc24e30](https://github.com/swathi22003343/DBMS/assets/120440439/b7b8a10e-3b39-493c-b39f-7818e5398536)

### Q10) Rollback to save point s1;


### QUERY:
```
sql
rollback to A;
```

### OUTPUT:
![276306832-441afff5-9f95-418b-ad8b-c2b5cfbf810d](https://github.com/swathi22003343/DBMS/assets/120440439/663cb052-6530-431d-a70c-0827e62a7a28)


### Q11)	Create a new user and grant access to any one database with "insert and update"


### QUERY:
```
CREATE USER new_user;
GRANT INSERT, UPDATE ON database_name TO new_user;
```

### OUTPUT:
![281134636-3c3761a5-28c0-4c83-a203-89e0087e6676](https://github.com/swathi22003343/DBMS/assets/120440439/ff811fa5-bbe0-4321-931f-7f53abfbe4e1)

![281134796-fd08ac3a-d1a5-4a16-af6a-f3bc5ff24629](https://github.com/swathi22003343/DBMS/assets/120440439/9e21d8cf-5593-45c1-a33e-a2bad26704aa)

### Q12) Check the user access and display the result 


### QUERY:
SHOW GRANTS FOR new_user;

### OUTPUT:
![281134999-2fbd5d94-7610-4828-a072-c84372c06442](https://github.com/swathi22003343/DBMS/assets/120440439/1627821e-46b1-47df-a7c4-194ffe7a66a6)

### Q13) Revoke the privillages.

### QUERY:
```
SHOW GRANTS FOR new_user;
REVOKE INSERT, UPDATE ON database_name FROM new_user;
SHOW GRANTS FOR new_user;
```

### OUTPUT:

![281136125-bd4b2b58-817e-42ea-b84d-a59af0382c11](https://github.com/swathi22003343/DBMS/assets/120440439/a245c387-a9ec-46c2-a35a-b1de593f3a8a)

## RESULT :
Thus the basic TCL and DCL commands are executed.
