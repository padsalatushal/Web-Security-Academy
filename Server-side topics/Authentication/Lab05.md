# Lab 05 : Username enumeration via account lock

## Overview:
- Level : PRACTITIONER
- This lab is vulnerable to username enumeration. It uses account locking, but this contains a logic flaw. To solve the lab, enumerate a valid username, brute-force this user's password, then access their account page.

## Analysis:
- account lock 


## Solution:
- capture login request
- ran cluster bomb attack in intruder 
- select username and password as parameter
- password as null value
- filter out username via responce length 
- username : att
- again ran sniper intruder attack as att as username and passwordd as parameter
- filter out password via responce length
- password : love