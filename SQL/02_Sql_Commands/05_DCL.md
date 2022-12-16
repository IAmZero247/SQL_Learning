# Data Control Language [DCL] Commands
------------


* This commands are used by DBA for granting permissions to users and Revoking the permission from users.

* We have two DCL Commands i.e., grant, revoke

    GRANT >>>> providing the permissions
 
    REVOKE >>>> Takingout the permissions



## To Create User 
```
Syntax:
=======
CREATE USER <uname> IDENTIFIED BY <password>;

Example:
========
CREATE USER karthik IDENTIFIED BY mypassword;

Output:
=======
User KARTHIK created.
```

## Granting the permissions to karthik user for creating,insert,updating,deleting
```
Syntax:
=======
GRANT RESOURCE,CONNECT TO <uname>;

Example:
========
GRANT RESOURCE,CONNECT TO karthik;

Output:
=======
Grant succeeded.
```


## Removing the permissions to karthik user for creating,insert,updating,deleting

```
Syntax:
=======
REVOKE RESOURCE FROM <uname>;

Example:
========
REVOKE RESOURCE FROM karthik;

Output:
=======
Revoke succeeded.
```


## To view all the users in the Database

```
SQL >>>> SELECT * FROM ALL_USERS;
```
## To view all the details about Database users

```
SQL >>>> SELECT * FROM DBA_USERS;
```

## To View all the tables in Particular Account

```
SQL >>>> SELECT * FROM TAB;
```

## To Know the username Of Connected Account

```
SQL  >>>> SHOW USER
```
## To Change the Password of an User Account

```
SQL >>>> ALTER USER karthik IDENTIFIED BY mynewpassword;
```
## How to lock an User Account

```
SQL >>>> ALTER USER karthik ACCOUNT LOCK;   >>>> Locking the account
```

## How to unlock the User Account

```
SQL >>>> ALTER USER karthik ACCOUNT UNLOCK;  >>>> Unlocking the account
```

## How to drop the user

```
SQL >>> DROP USER <uname> CASCADE

    >>> DROP USER karthik CASCADE;
```

*  If the user account is empty then we no need to define cascade and if the user account is non-empty then we need to use 
  cascade.


