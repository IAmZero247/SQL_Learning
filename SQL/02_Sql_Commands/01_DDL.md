# DDL - CREATE
------------
* To Create a Database Object of an Table we need to use DDL Command of "CREATE".

* After Creating the Database object of an Table in Database, as programmer we need to insert data into table then we need to 
  use DML command "INSERT".

* After Inserting the data into Database as programmer we need to validate the information by using DRL Command "SELECT"


------------

## Step-1: CREATE SYNTAX

* In order to create the Database table we will use DDL Command "create" and observe the syntax as below

* By using this DDL Command we can create any Database Object(Table,View,Sequences,Synonymns,Stored Procedure,Stored Functions)

* As of now we are going to create any Database table (Database Object)


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

* Write a Query for Creating Database Table of "bank_customers" information with following fields                    
                >  CustomerId     >>  only numbers
                >  CustomerName   >>  string
                >  Gender         >>  string
                >  Age            >>  only numbers
                >  location       >>  string


```
    SQL> CREATE TABLE bank_customers(
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
    INSERT INTO bank_customers(customer_id,customer_name,gender,age,location) VALUES(01,'Alice','Female',35,'Hyderabad');

    INSERT INTO bank_customers(customer_id,customer_name,gender,age,location) VALUES(02,'Jack','Male',35,'Banglore');

  
  Example
  =======
    INSERT INTO bank_customers VALUES(03,'Jennifer','Female',40,'Mumbai');

  Inject value via variable in programming -> INSERT INTO bank_customers VALUES(&customerId,&customername,&gender,&age,&location);
  
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
       SELECT * FROM bank_customers;
```



```
   Example
   =======
     SQL >>> CREATE TABLE club_users(username VARCHAR2(50),user_password VARCHAR2(100));
```

# DDL - ALTER
------------

* By using this DDL Command we can modify the structure of the Database Objects.

* As of Now By using this DDL Command we can modify the structure of the Database table.

* By using this command we can perform below things
    
        1. We can add the new column to the existing table.

        2. We can remove/drop the existing column from table.

        3. We can rename column names for existing columns in table.

        4. We can modify the datatypes for exisitng columns in table.
		
		
		
1. <ins> Adding new column into Exisiting Table(ALTER-ADD) : </ins> 
   
    * This command is used to add one column (or) more than one column to existing table 
	* We cannot add the new columns at required positions in the table.
    * Always newly added columns will be added at end of existing columns.
    ```
     Syntax
     ======
       ALTER TABLE <table_name> ADD(columnname1 column1datatype..... columnnamen columnndatatype);

     Example 
     =======
       SQL >> ALTER TABLE club_users ADD (gender CHAR(1),city_name VARCHAR2(50));
    ```
       
2.  <ins> We can drop the existing column from table(ALTER-DROP)</ins>
 
    * This command is used to remove the columns from the existing Database table.
    * By using this command either we can drop one column (or) more than one at atime.
	
    ```
    Syntax
    ======
      ALTER TABLE <table_name> DROP COLUMN <columname-1>; -- Removing only one column

      ALTER TABLE <table_name> DROP (columnname-1,columnname-2......columnname-n);

    Example
    =======
      SQL >>> ALTER TABLE bank_customers DROP COLUMN gender; -- Removing the one column 
  
      SQL >>> ALTER TABLE bank_customers DROP(gender,age);   -- Removing the multiple columns
	  
    ``` 
	
3. <ins>We can rename column names for existing columns in table(ALTER-RENAME)</ins>
    
    * This command is used to change the column names from old column name to new column name.

    * By using this command we can't rename columns name for more than one columns at a time.
	
	```
     Syntax
     =======
       ALTER TABLE <table_name> RENAME COLUMN <old_column_name> TO <new_column_name>;

     Example
     =======
      SQL>>ALTER TABLE bank_customers RENAME COLUMN customer_name TO customer_full_name;
	``` 
	

4. <ins>We can modify the datatypes for exisitng columns in table(ALTER-MODIFY)</ins>
 
   * By using this command we can increase/decrease the size of the datatype of database columns and we can change the datatype from old datatype to new datatype.
   
   ```
   Syntax
   ======
      ALTER TABLE <table_name> MODIFY column_name datatype(size);

      ALTER TABLE <table_name> MODIFY(column_name-1 datatype(size)...........column_name-n datatype(size));
   Example
   ========
    SQL >>>> ALTER TABLE bank_customers MODIFY customer_name varchar2(100);

    SQL >>>> ALTER TABLE bank_customers MODIFY(customer_id number(6), customer_name varchar2(140));
   ``` 	


# DDL - TRUNCATE
------------  
* This command is used to delete the records permanently from the exisiting table.
* CREATE,ALTER,RENAME,DROP are concentrating on struture of Database object but where as TRUNCATE concentrates on data.

```
   Syntax:
   =======
       TRUNCATE TABLE <table_name>;

   Example 
   =======
       TRUNCATE TABLE bank_customers;

   OUTPUT
   ======
       Table BANK_CUSTOMERS truncated.   
```

# DDL - RENAME
------------ 
* This command is used to change the table name from old table name to new table name
```
    Syntax
    ======
        RENAME  <old_table_name> TO <new_table_name>
		
		ALTER TABLE <old_table_name> TO <new_table_name>;

    Example 1
    =========
    SQL >>>  RENAME bank_customers TO sbi_customers;

    OUTPUT
    ======
    Table renamed.
		
	Example 2
    =========
	SQL >>> ALTER TABLE sbi_customers rename to axis_customers;
	
	OUTPUT
    ======
    Table SBI_CUSTOMERS altered.
	
```


# DDL - DROP
------------ 

* This command is used to remove the table structure from Database objects
 
```    
    Syntax
    ======
      DROP TABLE <table_name>;

    Example
    =======
      DROP TABLE axis_customers;

    OUTPUT
    =======
      Table AXIS_CUSTOMERS dropped.

* What ever the tables we got dropped in oracle database those table are available in ORACLE RECYCLE BIN.

* To retreive the oracle recycle bin then we need to use the below command 
```  
     SQL >>> SELECT * FROM RECYLEBIN;
```	 
	 
* We can restore the dropped table back to Oracle database by using flashback command

```
    Syntax:
    =======
        FLASHBACK TABLE <table_name> TO BEFORE DROP;

    Example
    =======
        FLASHBACK TABLE axis_customers TO BEFORE DROP;
```
>>> To See all the tables in the database(select * from tab;)
	   