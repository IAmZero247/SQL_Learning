# SQL Constraints
------------


1. Constraints are set of rules / business rules which will be defined at DDL statements.

2. Constraints enforce the database to allow only valid values into the Database tables.

3. Constraints ensure the user to fetch only valid/accurate data from the Database tables.

4. We can apply the Constraints at two levels

   1. <ins>Column level constraints</ins>
   
     Applying the constraints after defining the column immediately then those constraints are called as 
     "Column level constraints"

   2. <ins>Table level constraints</ins>
   
     Applying the constraints after defining all the columns in the table (or) at the end of the table are called as 
     "Table level constraints".


### Basically Oracle constraints are broadly divided into six types
------------
   1) Unique

   2) Not Null

   3) Check

   4) Default

   5) Primary Key
  
   6) Foreign Key (or) Referential Integrity
   
   
### 1. Unique Constraint    
------------


* This constraint does not allows us to enter duplicate values into column (or combination of columns)of an Database table.

* We can apply the unique constraint more than one column in the Same table(advantage)

* This constraint allows the user to enter the null values (disadvantage)

* All Basic Syntax CREATE/DISABLE/ENABLE/DELETE
```
Different ways to create constrait
##################################
Syntax-1a: Column Level constraint
========
	  CREATE TABLE table_name (
		...
		column_name data_type UNIQUE
		...
	  );

Syntax-1b
========
	CREATE TABLE table_name (
		...,
		UNIQUE(column_name)
	);

Syntax-2a: Defining the Unique Constraint by CONSTRAINT clause
========
CREATE TABLE table_name (
    ...
    column_name data_type CONSTRAINT <constraint_name> <contraint_type>;
    ...
);

Syntax-2b : Table level constraint
========
CREATE TABLE table_name (
    ...
    column_name data_type,
    ...,
    CONSTRAINT <constraint_name> UNIQUE(column_name)
);

Syntax-3 : Table level Unique Constraint for defining multiple columns as unique
========
CREATE TABLE table_name (
    ...
    column_name1 data_type,
    column_name2 data_type,
    ...,
    CONSTRAINT <constraint_name> UNIQUE(column_name1, column_name2)
);

Syntax-4 : Adding constraint after creation of table
####################################################
ALTER TABLE table_name ADD CONSTRAINT <constraint_name> UNIQUE(column_name1, column_name2);

Syntax : How to disable the constraint temporarily
##################################################
ALTER TABLE table_name DISABLE CONSTRAINT unique_constraint_name;

Syntax : How to enable the constraint back
##########################################
ALTER TABLE table_name ENABLE CONSTRAINT unique_constraint_name;

Syntax : Dropping the constraint
################################
ALTER TABLE table_name DROP CONSTRAINT unique_constraint_name;

```

### 2. NotNull Constraint    
------------
### 3. Check Constraint    
------------
### 4. Default Constraint    
------------
### 5. Primary Key Constraint    
------------
### ()Foreign Key Constraint    
------------
## LeetCode 
-----------




| Question                | Answer                 |
|-------------------------|------------------------:|
| <a href="https://leetcode.com/problems/employees-earning-more-than-their-managers/description/">Employees earn more than their managers</a> | <a href="https://github.com/mdh266/SQL-Practice/blob/master/leetcode/employees_managers.sql">Solution</a> |
| <a href="https://leetcode.com/problems/second-highest-salary/description/">Second highest salaries</a> | <a href="https://github.com/mdh266/SQL-Practice/blob/master/leetcode/SecondHighestSalary.sql">Solution</a> |
| <a href="https://leetcode.com/problems/customers-who-never-order/">Customers who never order</a> | <a href="https://github.com/mdh266/SQL-Practice/blob/master/leetcode/CustomersDontOrder.sql">Solution</a> | 
| <a href="https://leetcode.com/problems/duplicate-emails/description/">Duplicate Emails</a> | <a href="https://github.com/mdh266/SQL-Practice/blob/master/leetcode/DuplicateEmails.sql">Solution</a> |
|[Rising Temperatures](https://leetcode.com/problems/rising-temperature) | [Solution](https://github.com/mdh266/SQL-Practice/blob/master/leetcode/RisingTemperatures.sql) |
|[Department Top Three Salaries](https://leetcode.com/problems/department-top-three-salaries/submissions/) | [Solution](https://github.com/mdh266/SQL-Practice/blob/master/leetcode/Top3DeptSalaries.sql) |
|[N-th Highest Salary](https://leetcode.com/problems/nth-highest-salary/) | [Solution](https://github.com/mdh266/SQL-Practice/blob/master/leetcode/NthHighestSalary.sql)|
|[Department Highest Salary](https://leetcode.com/problems/department-highest-salary/) | [Solution](https://github.com/mdh266/SQL-Practice/blob/master/leetcode/DeptHighestSalary.sql) |
| [Rank Scores](https://leetcode.com/problems/rank-scores/) | [Solution](https://github.com/mdh266/SQL-Practice/blob/master/leetcode/RankScores.sql) |
| [Not Boring Movies](https://leetcode.com/problems/not-boring-movies/) | [Solution](https://github.com/mdh266/SQL-Practice/blob/master/leetcode/notboringmovies.sql)|
| [Exchange Seats](https://leetcode.com/problems/exchange-seats/) | [Solution](https://github.com/mdh266/SQL-Practice/blob/master/leetcode/exchange-seats.sql)|
| [Consecutive Numbers](https://leetcode.com/problems/consecutive-numbers/) | [Solution](https://github.com/mdh266/SQL-Practice/blob/master/leetcode/ConsecutiveNumbers.sql)|
| [Human Traffice Of Stadium](https://leetcode.com/problems/human-traffic-of-stadium/) | [Solution](https://github.com/mdh266/SQL-Practice/blob/master/leetcode/HumanTrafficStadium.sql) |




