# Oracle Datatypes
------------

## INSERT SYNTAX - Adding new data to sample Table 

*  Datatype >>> It is used to define the type of the value to be holded in the database column

## Basically Oracle classified the datatypes in the below categories 


### <ins>1) number</ins>
  
* These datatypes allows use to define the numeric/Number values into Database column such as integers(whole numbers) (or)  decimal numbers(fractional numbers).

      1. Whole numbers:: 10,20,50,60,70,58,,958 etc.,

      2. Decimal numbers:: 10.25,25.36.69.58.47.1232 etc.,

* i) <ins>number(size)</ins>
      
    1. This datatype allows us to define only integers (or) whole numbers either postive (or) negative numbers such as

         studentrollno,employeeno,customerbillno etc.,

    2. Here size represents the number of digits 
    ```
       Example
       ======= 
         studentNo NUMBER(4)
		 >>>> 9999
    ``` 
* ii)  <ins>number(precision,scale)</ins>
    
    1. This datatype allows us to define decimal values(or) fractional values such as student average marks,employee    
         salary,Bill Amount of an Customer,Interest Rates in Bank etc.,

    2. Here Precision means no of digits including decimal values where as scale means no of decimal values.
   
    ```   
	   Example
       ========
          employeesalary NUMBER(6,2);   >>>> 9999.99

          billAmount NUMBER(8,3)  >>>> 12345.678  
    ```
###   <ins>2) Alphabets </ins>

* This datatype further divided into below types
 
*  i) <ins>char(size)</ins> : 
     
    1. This datatype allows us to define character values  such as employee names,student names etc.,

    2. The maximium length of datatype is 1-2000 characters.

    3. It always allocates the memory in a static fashion.

    ```
        Example:
        ========
          studentName CHAR(25);

          Name of Student :: Jennifer   
    ```
* ii) <ins>varchar(size) / varchar2(size)</ins>
     
    1. This datatype allows us to define character values such as employee names,student names,customer names etc.,

    2. The maximium length of this datatype is 1-4000 characters.

    3. It always allocates the memory in Dynamic fashion.

    ```
	 Example
        ========
           studentName varchar(30);

           Name of Student :: Alice
    ```    
       
	4. NOTE : Difference between varchar (Vs) varchar2 datatype ?
        
        1.  varchar is developed by SQL 
       
        2.  varchar2 is developed by Oracle Corporation       

###   <ins>3) Date</ins>
  =======
1. This datatype allows us to defind date values in the Database column such as DateofJoining,HireDate,BirthDate,PurchasedDate,DateofBooking etc.,

2. The default format of Date in Oracle Database is "DD-MON-YY"  >>> 12-FEB-13
 
###   <ins>4) Timestamp</ins>
 
1. This dataype allows us to defined both Date and time values into Database Column

2. The default format of timestamp in oralce Database is "DD-MON-YY HH:MM:SS"  >>> 12-Feb-13 18:20:35

###   <ins>5) Miscellaneous</ins> 

1.  Clob  >>> Character Large Object  >> Which is extension of Varchar datatype >> 1 GB -TO- 4GB

2.  Blob  >>> Binary Large Object >> Which can be used for storing files,audios,videos etc.,>>>> 1 GB -TO- 4GB

3.  BFile >>> Binary File >> Which can be used for externdal data such as external files,binary files etc.,> 1 GB -TO- 4GB

` 