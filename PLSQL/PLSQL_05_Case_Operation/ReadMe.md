# Case Operations

## Case Expression And Case Statement


1. ## Case Expression - Used to assign value to some variable

	1. Syntax 
	```
	somevar := CASE [expression | condition]
		WHEN condition1 THEN result1
		WHEN condition2 THEN result2
		WHEN condition3 THEN result3
		.............
		.............
		ELSE resultdft
	END;	
		
	``` 
	2. [expression | condition] , condition1 , condition2 etc should be of same type
	3. somevar , result1, result2 , resultdft should be of same type.
	4. Example 
	```
	/****************** Simple Case Expression ******************/
	DECLARE
	  v_job_code        VARCHAR2(10) := 'SA_MAN';
	  v_salary_increase NUMBER;
	BEGIN
	  v_salary_increase :=  CASE v_job_code 
			WHEN 'SA_MAN' THEN 0.2
			WHEN 'SA_REP' THEN 0.3
			ELSE 0
			END;
	  dbms_output.put_line('Your salary increase is : '|| v_salary_increase);
	END;
	/************************************************************/
	 
	/****************** Searched Case Expression ****************/
	DECLARE
	  v_job_code        VARCHAR2(10) := 'IT_PROG';
	  v_department      VARCHAR2(10) := 'IT';
	  v_salary_increase NUMBER;
	BEGIN
	  v_salary_increase :=  CASE
						  WHEN v_job_code   = 'SA_MAN' THEN 0.2
						  WHEN v_department = 'IT' AND v_job_code = 'IT_PROG' THEN 0.3
						 ELSE 0
						 END;
	  dbms_output.put_line('Your salary increase is : '|| v_salary_increase);
	END;
	/************************************************************/
 
    ```

2. ## Case Statement

1. Syntax 
	```
	CASE 
		WHEN condition-a THEN 
		     statementa1;
			 statementa2;
			 statementa3;
			 ...
		WHEN condition-b THEN 
		     statementb1;
			 statementb2;
			 statementb3;
			 ...
		WHEN condition-c THEN 
		     statementc1;
			 ...
		.............
		.............
		ELSE 
		statement-def1;
		statement-def2;
		statement-def3;
		...
	END CASE;	
		
	``` 
 2. Example 
	```
	DECLARE
	  v_job_code        VARCHAR2(10) := 'IT_PROG';
	  v_department      VARCHAR2(10) := 'IT';
	  v_salary_increase NUMBER;
	BEGIN
	  CASE
		WHEN v_job_code = 'SA_MAN' THEN
		  v_salary_increase := 0.2;
		  dbms_output.put_line('The salary increase for a Sales Manager is: '|| v_salary_increase);
		WHEN v_department = 'IT' AND v_job_code = 'IT_PROG' THEN
		  v_salary_increase := 0.2;
		  dbms_output.put_line('The salary increase for a Sales Manager is: '|| v_salary_increase);
		ELSE
		  v_salary_increase := 0;
		  dbms_output.put_line('The salary increase for this job code is: '|| v_salary_increase);
	  END CASE;
	END;
	```

