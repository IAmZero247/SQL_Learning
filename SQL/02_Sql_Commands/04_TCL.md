# Transaction Control Language [TCL] Commands
------------




* We have three TCL Commands 

	* COMMIT    >>> Saving the information permanently in the database

	* ROLLBACK  >>> Undo Operation

	* SAVEPOINT >>> It is used to save a set of transactions under a name



## Transaction And Session
Transaction
===========
* Transaction: Any Operation which we can perform on the database by using DML Commands i.e.,insert,update,delete on the Database then 
  it is known as "Transaction"

* Session: It can be defined certain amount of time (or) interval given to user to perform some activities.
	1. During the Login to Logoff of an user what ever operation done by the user i.e.,Transactions
	2. Basically sessions can be terminated in two ways
		* Normal Termination   >>> exit (or) quit   >>> Always save the data (or) Transactions successful
		* Abnormal Termination >>> Directly switching off the CPU, Directly Hit PowerOff Button etc., >>> Doesn't saves the data (or) transactions unsuccessful



## COMMIT

* This command is used to save the transactions explictly from the moment of the user login to database to till execute this command.

```
Syntax:
=======
   COMMIT;
```


## ROLLBACK

* This command is used to discard all the transactions done on Database table before performing commit operation

```
Syntax:
=======
   ROLLBACK;
```

## Example Scenario on Commit and Rollback


```
    User  >>>> Logged into DB   >>>> Insert(10),Update(10),delete(15) >>>> By Default this operations will not saved


    If we want to save all these operations permanently to the database table >>>> COMMIT(SAVE)

 
    If we don't want to save all these operations into Database >>>> ROLLBACK (UNDO)
```


## SAVEPOINT

* This command is used to save a set of transactions under a name.

```
 Syntax:
 =======
    SAVEPOINT <save_point_name>;
```


## Example Scenario on Commit , Rollback and Savepoint

```
   user >>>>> Logged into DB >>>> Insert(2)   >>>> Added One Savepoint      >>>> SAVEPOINT  insertSavePoint

                             >>>> Update(2)   >>>> Added one More SavePoint >>>>> SAVEPOINT updateSavePoint

   User >>>>> I can do "ROLLBACK" Operation >> Insert(2),Update(2) will be discarded from Database.

   User >>>>> I can do "COMMIT" Operation   >> Insert(2),Update(2) will be saved into Database permanently

   User >>>>> I can do "ROLLBACK" to particular "Savepoint" 
 
        SQL>>> ROLLBACK TO updateSavePoint >>>> Only Update(2) will be discarded

        SQL>>> ROLLBACK TO insertSavePoint >>>> Only Insert(2) will be discarded

        SQL>>> COMMIT;   >>>> Nothing will be saved
```