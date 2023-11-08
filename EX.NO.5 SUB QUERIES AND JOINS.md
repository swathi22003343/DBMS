# EX.NO.5 SubQueries, Views and Joins 
### DATE
## AIM
### To use SubQueries, Views and Joins in SQL 
## Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values
```sql
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

## Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:

![270762717-1848b392-372d-4111-af2d-25daf5458864](https://github.com/swathi22003343/DBMS/assets/120440439/473a352c-c9ed-4ac0-b98a-7f68e5805ab9)

### OUTPUT:
![270762784-ee7dd795-bf87-4dff-aca9-b80307477ddd](https://github.com/swathi22003343/DBMS/assets/120440439/4ad87e5e-e181-4be1-8738-213d742047ed)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:

![270763155-2c78d720-f077-4843-bbbd-cefb0e36afcf](https://github.com/swathi22003343/DBMS/assets/120440439/37ce8bb0-82fd-496d-a71a-6d407ebea29b)

### OUTPUT:
![270763212-0ca9e7dc-c9b6-45c6-b7a0-bf123d815295](https://github.com/swathi22003343/DBMS/assets/120440439/6a945b24-18a2-43e9-81d3-5fc0b3ee23da)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:

![270764132-ea1201a0-53bc-436b-b815-3889759afcff](https://github.com/swathi22003343/DBMS/assets/120440439/00fa1527-edd6-4868-aacd-cbb4cd10466b)

### OUTPUT:

![270764187-7376ae95-bab6-4739-abd7-bdc5e8a727dd](https://github.com/swathi22003343/DBMS/assets/120440439/40341649-aa67-4012-a9ab-c066997f7b68)

### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![270764614-4c3e781f-8787-461d-b2ee-162f5222abd9](https://github.com/swathi22003343/DBMS/assets/120440439/e66a7e59-ddd7-46af-8aa1-6affe1c5e9dd)


### OUTPUT:
![270764656-753d1db9-8955-4b97-b850-43622886968b](https://github.com/swathi22003343/DBMS/assets/120440439/01b3a206-8f6f-4877-817e-4e87770b2579)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:

![270765070-3551ed65-3cb5-4846-b817-48436b507530](https://github.com/swathi22003343/DBMS/assets/120440439/112a06f8-4ec1-4f5d-a147-0bd78be996af)

### OUTPUT:
![270765159-026712b5-02b2-40d6-a757-cec5bc08890d](https://github.com/swathi22003343/DBMS/assets/120440439/61915164-9ef3-4e53-87f1-3a9074c21cd2)

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
![270767939-d83bbdcd-83a3-427e-bd2b-e799958b055d](https://github.com/swathi22003343/DBMS/assets/120440439/4b1a99c8-33c6-42e1-a582-8971997b3855)


### OUTPUT:
![270767871-6941b531-33ed-41dc-b6f4-9e8bcc0dd113](https://github.com/swathi22003343/DBMS/assets/120440439/3c347cc8-c9b9-451a-92ca-b6b7b1913e7e)

## Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:

![270771248-20c63405-1555-444c-8d92-daee8ad9f52d](https://github.com/swathi22003343/DBMS/assets/120440439/a3e40602-0c75-4fb4-8d5e-496f90a65c24)

### OUTPUT:
![270771306-4bf9b80e-b31d-486e-87b5-5462e60e6e2f](https://github.com/swathi22003343/DBMS/assets/120440439/3014fec8-92b9-46cd-a8a6-2eacebbb8248)

### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:

![270772008-6b4b7f1a-e1fa-41eb-abfc-d544b005a00e](https://github.com/swathi22003343/DBMS/assets/120440439/8041d1df-a7cb-41b2-81e9-0ad9cb846e28)

### OUTPUT:
![270772054-031553d8-640c-4306-9f12-cd4a6c6a68ed](https://github.com/swathi22003343/DBMS/assets/120440439/01927913-50cc-4b12-aef6-2f81817a8449)

### Q9) Perform Natural join on both tables

### QUERY:
![270772360-a9609769-7404-4c74-909b-53d5610ea79a](https://github.com/swathi22003343/DBMS/assets/120440439/3c7b88df-d6dd-44ed-9c30-6598719d3de8)


### OUTPUT:
![270859730-099c0b7d-7822-4459-8025-92adc824dda8](https://github.com/swathi22003343/DBMS/assets/120440439/79c3b6f0-9807-4db7-919f-0cc2c2b9e6f6)

### Q10) Perform Left and right join on both tables

### QUERY:
![270849330-7915ee92-d1e0-4528-be68-4bbe6fd7a11c](https://github.com/swathi22003343/DBMS/assets/120440439/3e06e144-4b08-4bf7-83db-ff3c423f1660)

![270860423-dcc24099-0fdd-404b-b81d-ea86de5cc8f9](https://github.com/swathi22003343/DBMS/assets/120440439/4a7ce9ad-2ad1-4614-9c97-3854706ac641)

### OUTPUT:
![270860061-bfa8a83b-9e86-4924-895c-05fbe6346506](https://github.com/swathi22003343/DBMS/assets/120440439/24083455-8511-4b77-bd6b-33207b16935d)
![270860293-7fe7c05b-ca77-4da2-9ab9-38a5f50a4879](https://github.com/swathi22003343/DBMS/assets/120440439/20047a88-32b1-4c45-8f85-eee7116c497b)

### RESULT 
Thus the basics of subqueries,views,joins are performed in SQL.
