# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE
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

![280923349-e875b722-4f09-4e9b-8da7-4e7097b9017a](https://github.com/swathi22003343/DBMS/assets/120440439/1a8a4727-76c9-43e7-bbeb-f64c4f7630aa)

### Relational model

![280923365-09bdd43d-f3af-4bc7-b366-ce6ccac30954](https://github.com/swathi22003343/DBMS/assets/120440439/b4f9e045-2b31-40ce-b44c-c59919e6f2f9)

### SQL DDL Schema 
```
CREATE TABLE BANK
(
  CODE INT NOT NULL,
  NAME INT NOT NULL,
  ADDRESS INT NOT NULL,
  PRIMARY KEY (CODE)
);

CREATE TABLE BANK_BRANCH
(
  ADDRESS INT NOT NULL,
  BRANCH_NO INT NOT NULL,
  PRIMARY KEY (BRANCH_NO)
);

CREATE TABLE ACCOUNTS
(
  ACCT_NO INT NOT NULL,
  BALANCE INT NOT NULL,
  TYPE INT NOT NULL,
  PRIMARY KEY (ACCT_NO)
);

CREATE TABLE LOAN
(
  LOAN_NO INT NOT NULL,
  AMOUNT INT NOT NULL,
  TYPE INT NOT NULL,
  PRIMARY KEY (LOAN_NO)
);

CREATE TABLE CUSTOMER
(
  SSN INT NOT NULL,
  NAME INT NOT NULL,
  ADDRESS INT NOT NULL,
  PHONE INT NOT NULL,
  PRIMARY KEY (SSN)
);
```
## RESULT 

Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.

