# Ex. No: 9 PL/SQL program using Cursor 
### DATE: 
### AIM: 
To create PL/SQL program to display the customer table 

### Steps:
1. Declare the variable  in Declare section.
2. Fetch the variable with datatype similar to data type in cursor 
3. Create a cursor to select all rows from customers table.
4. Display the result 
5. End the begin section.

### Program:
```
CREATE TABLE employd (
  empid NUMBER,
  empname VARCHAR(10),
  dept VARCHAR(10),
  salary NUMBER
);
```

```
INSERT INTO employd VALUES (1, 'Gojo', 'HR', 100000);
INSERT INTO employd VALUES (2, 'Yuji', 'Sales', 80000);
select * from employd;
```

```

DECLARE
   CURSOR employd_cursor IS
   SELECT empid,empname,dept,salary
   FROM employd;
   emp_id NUMBER;
   emp_name VARCHAR(50);
   emp_dept VARCHAR(50);
   emp_salary NUMBER;
BEGIN
  OPEN employd_cursor;

  LOOP
    FETCH employd_cursor INTO emp_id, emp_name, emp_dept, emp_salary;

    EXIT WHEN employd_cursor%NOTFOUND;

    DBMS_OUTPUT.PUT_LINE('Employee ID: ' || emp_id);
    DBMS_OUTPUT.PUT_LINE('Employee Name: ' || emp_name);
    DBMS_OUTPUT.PUT_LINE('Department: ' || emp_dept);
    DBMS_OUTPUT.PUT_LINE('Salary: ' || emp_salary);
  END LOOP;

  CLOSE employd_cursor;
END;
/
```

### Output:
![277101220-d08431a3-089d-449d-809c-785120d2b818](https://github.com/swathi22003343/DBMS/assets/120440439/1ff440b8-4a8b-421e-9010-db70cd30cde1)


### Result:
Thust the program was performed sucessfully.
