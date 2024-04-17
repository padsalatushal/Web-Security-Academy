# Lab 02 : Username enumeration via subtly different responses

## Overview:
- Level : PRACTITIONER
- vulnerable to username enumeration and password brute-force attacks

## Analysis:
- goto login page when we login with test username and test password it gives error Invalid username or password.

## Solution:
- figure out username
- capture that request and run intruder attack as username as parameter
- on intruder result on filter option search by 'Invalid username or password.' and select negative search it will give request that doesn't contain 'Invalid username or password.' in responce.
- got username app01
- now ran intruder attack same but for password parameter
- filter out password via status code 


username : app01
password : tigger
