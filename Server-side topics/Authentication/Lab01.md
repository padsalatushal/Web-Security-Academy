# Lab 01 : Username enumeration via different responses

## Overview:
- Level : APPRENTICE
- vulnerable to username enumeration and password brute-force attacks

## Analysis:
- goto login page when we login with test username and test password it gives error username  not found

## Solution:
- figure out username
- capture that request and run intruder attack as username as parameter
- filter by responce length and we got username adam
- bruteforce password for adam user


username : adam 
password : matrix
