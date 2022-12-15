# DDL - CREATE
------------
* To Create a Database Object of an Table we need to use DDL Command of "CREATE".

* After Creating the Database object of an Table in Database, as programmer we need to insert data into table then we need to 
  use DML command "INSERT".

* After Inserting the data into Database as programmer we need to validate the information by using DRL Command "SELECT"


------------

## Step-1: CREATE SYNTAX

* In order to create the Database table we will use DDL Command "create" and observe the syntax as below

```
 CREATE TABLE <table_name>(
                            <column_name_1> <DATATYPE>,
                            <column_name_2> <DATATYPE>,
                            ...........................
                            ...........................
                            ...........................
                            <column_name_n> <DATATYPE>,
          
                          );
						  
						  
  NOTE: Naming Conventions need to be follow for any name in Oracle Database
      ==========================================================================
      1) Every name in Database must begins with "Alphabet".

      2) We need to follow the mentioned charset i.e.,a-z,A-Z,0-9,@,$,#,_

      3) Names are not Case Sensitive.
 
      4) Predefined keywords are not allowed.

      5) Blank Spaces are also not allowed in the names.						  
```

* Write a Query for Creating Database Table of "abc_customers" information with following fields                    
                >  CustomerId     >>  only numbers
                >  CustomerName   >>  string
                >  Gender         >>  string
                >  Age            >>  only numbers
                >  location       >>  string


```
    SQL> CREATE TABLE abc_customers(
                                   customer_id NUMBER,
                                   customer_name VARCHAR(50),
                                   gender VARCHAR(15),
                                   age NUMBER,
                                   location VARCHAR(50)
                                  );

      OUTPUT
      ======
      Table Created
```

## Step-2: INSERT SYNTAX

* Inserting the data into Database table by using DML Command "INSERT"

```
  Syntax For Insert Command 
  ==========================   
  1) INSERT INTO <table_name>(column_name_1,column_name_2.................column_name_n) VALUES(value1,value2,.....valuen);
  
  2) INSERT INTO <table_name> VALUES(value1,value2,value3,value4..................valuen);

  Example
  =======
    INSERT INTO abc_customers(customer_id,customer_name,gender,age,location) VALUES(01,'Alice','Female',35,'Hyderabad');

    INSERT INTO abc_customers(customer_id,customer_name,gender,age,location) VALUES(02,'Jack','Male',35,'Banglore');

  
  Example
  =======
    INSERT INTO abc_customers VALUES(03,'Rajesh','Male',40,'Mumbai');

  Inject value via variable in programming -> INSERT INTO abc_customers VALUES(&customerId,&customername,&gender,&age,&location);
  
 ``` 
 
 
 
## Step-3: SELECT SYNTAX
======
 * Just Validating the Information by selecting data from Database Table using DRL Command "SELECT"

```
    Syntax for Select Command
    =========================
       SELECT * FROM <table_name>;   >> Retrieves all the information from given table

   Example 
   =======
      SELECT * FROM abc_customers;
```