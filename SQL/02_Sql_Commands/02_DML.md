# DML
------------

## INSERT SYNTAX - Adding new data to sample Table 

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
    INSERT INTO abc_customers VALUES(03,'Jennifer','Female',40,'Mumbai');

  Inject value via variable in programming -> INSERT INTO abc_customers VALUES(&customerId,&customername,&gender,&age,&location);
  
 ``` 
 
## UPDATE SYNTAX - How to Modify the data in Database Table
 
 
* By using update statement we can change the existing column value based on some conditions.

* Condition means whether you want to update columns values for all records (or) particular record.

* If you omit (or) ignore the condition in the update statement then will performs update for all records of columns values.

```
 Syntax For Updating all rows in the Database table
 ===================================================
   UPDATE <table_name> SET <modifyingcolumn1>=<modifyingcolumn1value>.......<modifyingcolumnn>=<modifyingcolumnnvalue>


   Example : Write SQL Query to update the location as "Delhi" for all customers in abc_customers table

   SQL >>>> UPDATE abc_customers SET location='Delhi';

   Result  :::  3 rows updated.

 Syntax For Updating Particular rows in the Database table
 ===================================================
   UPDATE <table_name> SET <modifyingcolumn1>=<modifyingcolumn1value>.......<modifyingcolumnn>=<modifyingcolumnnvalue>

                       where <conditions>

   Example : Write SQL Query to update the location as "Pune" for particular customers in abc_customers table whose customer_id is 1 

   SQL >>> UPDATE abc_customers SET location='Pune' where customer_id = 1;


   Example : Write SQL Query to update the location as "Pune" for particular customers in abc_customers table whose customername is Jennifer

   SQL >>> UPDATE abc_customers SET location='Pune' where customer_name='Jennifer';

   Result::::: 1 row updated.


   Example : Write SQL Query to update the location as "Chennai" and age "40" for particular customer in abc_customers table whose customername is Jennifer

   SQL >>> UPDATE abc_customers SET location='Chennai',age=40 where customer_name='Jennifer';

   Result::::: 1 row updated.


   SQL >>> UPDATE abc_customers SET location='Guntur',age=40 where customer_name='Alice' and gender='Female';

   Result::::: 1 row updated.

  NOTE:
  =====
  * As of now in our table we have only one customer record whose customer name as "Jennifer" that is reason we are getting only one row updated in the above update SQL Statements

  * If we are having more than one customer whose customer names having "Jennifer" then will get respective rows matched got updated.

  * In the Realtime always recommended to perform the update statement based on the customer_id because customer_id will be unique number for every customer

  * we used two predefined keywords in update statement i.e., SET and WHERE 

        "SET" is used for defining the modifying columns in Database table

        "WHERE" is used specifying the condition to update the particular row (or) rows in database table

```		


## DELETE SYNTAX - How to Remove the Unwanted records from Database Table
 

* By using delete command we can remove unwanted records from Database table.

* If you specifying the where condition in delete statement then will delete particular records based on condition specified.

* If you omit (or) ignore the condition in delete statement then will delete all rows from database table.

```

 Syntax:
 ======
 DELETE FROM <table_name>;

 Ex: DELETE FROM abc_customers;  >>>> It will delete all rows from database table because we don't have any where filtering                                           condition in sql statement.

  
 Syntax:
 =======
 DELETE FROM <table_name> where <Conditions>;

 Ex:  DELETE FROM abc_customers where customer_id=1; 
	  >>> Deleting record from Table whose customer_id as 1

      DELETE FROM abc_customers where customer_name='Jack'; 
	  >>> Deleting record from Table whose customer_name as Jack

      DELETE FROM abc_customers where gender='Male';
	  >>> Deleting customers from table whose gender as "Male"

      DELETE FROM abc_customers where gender='Male' and age >=35;
	  >>>Deleting customers from table whose gender as "Male" and age should be greater than 35.

```
 