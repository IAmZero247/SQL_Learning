# SQL Commands / SQL Statements / SQL Queries
------------
* Basically Statement represents preforming the particular task (or) Statement is group of predefined words
   
   Example : SELECT * FROM emp;

* Every Statement must be terminated by Semicolon.

* The Statement which we are Passed to Database Software System, such statements is called as "SQL Statements".

* Basically SQL Commands/SQL Statements are Categorized as below

   1) <ins>Data Definition Language(DDL) Commands (or) DDL Statements </ins> 

      >> Deals with Creating/Modifying/Dropping Structure of Database Objects.

      >> DDL Commands are  "CREATE,ALTER,DROP,TRUNCATE,RENAME,FLASHBACK,PURGE"
	  
	  >> All DDL Commands are by default "AUTO COMMIT";

   2) <ins>Data Manipulation Lanaguage(DML) Commands (or) DML Statements</ins>
      
       >> Deals with Data of an Database objects

       >> DML Commands are "INSERT, UPDATE, DELETE"  
       
       >> All DML Commands are not by default "AUTO COMMIT"	  

       >> NOTE
  
			* When we are talking about update and delete commands we used "where" clause which can be used to specify the condition for sql statements

			* If we are not using where clause in update statment (or) delete statement means it will perform update operation and delete operation on all rows of the database table.
	   

   3) <ins>Data Control Language(DCL) Commands (or) DCL Statements</ins>
       
       >> Deals with giving the Permission (or) Revoking the permisssion of an users
 
       >> DCL Commands are used By "DBA Persons"

       >> DCL Commands are "GRANT,REVOKE"       

   4) <ins>Date Retrevial Language(DRL) / Data Query Language (DQL) Commands (or) DRL/DQL Statements</ins>

       >> Deals with Retreving the data from Database objects

       >> DRL Commands are "SELECT"

   5) <ins>Transaction Control Language(TCL) Commands (or) TCL Statements</ins>

       >> Deals with Transaction Management
  
       >> TCL Commands are "COMMIT, ROLLBACK, SAVEPOINT"
	   
NOTE
====
Database Objects in Oracle : Tables,Views,Sequences,indexes,Stored Procedures,Stored Functions etc.,	   