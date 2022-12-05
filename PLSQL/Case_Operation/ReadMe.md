# Case Operations

## Case Expresion And Case Statement


1. ## Case Expression

1. Syntax 
```
somevar := CASE [expression | condition]
	WHEN condition1 return result1
	WHEN condition2 return result2
    WHEN condition3 return result3
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
  v_salary_increase:=CASE
                      WHEN v_job_code   = 'SA_MAN' THEN 0.2
                      WHEN v_department = 'IT' AND v_job_code = 'IT_PROG' THEN 0.3
                     ELSE 0
                     END;
  dbms_output.put_line('Your salary increase is : '|| v_salary_increase);
END;
/************************************************************/
 
```

2. ## Case Statement

