# Oracle Accounts
------------
1) Database Administrator Account(DBA) Account i.e., sys(or)system 

2) We created some Database User using WebPage Approach  

3) We will create one Database user using CLI Approach -> john(mypassword)

```
 Step-1 : Creating the user using CLI Screen
  +++++++++++++++++++++++++++++++++++++++++++
     SQL> CREATE USER john IDENTIFIED BY mypassword;

      User created.

    NOTE:
    =====
     >>  Database Username : john and Database Password: mypassword


  Step-2 : Giving the Permissions to Newly Created User i.e.,john
  ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
     SQL> grant resource,connect to john;

     Grant succeeded.

    NOTE: After Creating the User make sure we need to give permissions for Creating Database Objects       
          (Table,Sequence,Index,view,Stored procedure,Stored Function etc.,)

 
  Step-3 : Connecting to Newly Created User Using CLI Approach
  ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
   SQL> connect
  
    Enter user-name: john
   
    Enter password:mypassword(Invisible)
   
    Connected.
```
### Note:
------------
* We can always create an new Database user account through DBA Account only.


* We can't create newly Database user account from another User account.

