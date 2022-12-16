# Data Query Language [DQL] Commands
------------




* This command is used to retreive the data from the existing table.

* By using this command we can retrieve all the records in the table and also we can retrieve specific recoreds from the database table.
```
   Syntax:
   ========
       SELECT * FROM <table_name>;

       SELECT * FROM <table_name> WHERE <condition>;

   Example:
   ========
       SELECT * FROM emp;

       SELECT * FROM emp WHERE dept=10;

  >> In the above select command we are retrieving all the records from emp table

  >> * represent selecting all columns from emp table
```

  
##  Selection
  
* Retrieving the data from Database table completely or partially based on condition 

```   
   Example:
   ========
      SELECT * FROM emp;
 
      SELECT * FROM emp WHERE deptno=10;
```

##  Projection
 
* Retreiving the data from specific columns of an Database table known as "Projection"

* In projection we can't use * symbol in the select query.

```
   Example:
   ========
     SELECT empno,ename FROM emp;
 
     SELECT empno,ename,job FROM emp;

     SELECT empno,ename,job,sal FROM emp;

     SELECT empno FROM emp;

     SELECT empname FROM emp
```