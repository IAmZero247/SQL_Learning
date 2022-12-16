# Data Control Language [DCL]
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


## Removong the permissions to karthik user for creating,insert,updating,deleting

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
SQL >>>> select * from all_users;
```
## To view all the details about Database users

```
SQL >>>> select * from dba_users;
```

## To View all the tables in Particular Account

```
SQL >>>> select * from tab;
```

## To Know the username Of Connected Account

```
SQL  >>>> show user
```
## To Change the Password of an User Account

```
SQL >>>> alter user karthik identified by mynewpassword;
```
## How to lock an User Account

```
SQL >>>> alter user karthik account lock;   >>>>> Locking the account
```

## How to unlock the User Account

```
SQL >>>> alter user karthik account unlock;  >>>> Unlocking the account
```

## How to drop the user

```
SQL >>> drop user <username> cascade

    >>> drop user karthik cascade;
```

*  If the user account is empty then we no need to define cascade and if the user account is non-empty then we need to use 
  cascade.


