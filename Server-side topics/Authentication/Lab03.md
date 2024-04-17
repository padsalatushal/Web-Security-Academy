# Lab 03 : Username enumeration via response timing

## Overview:
- Level : PRACTITIONER
-  vulnerable to username enumeration using its response times

## Analysis:
- login with given credentails
wiener : peter
- they have ip protection 
- when we have correct credentails notice responce time
- now wiener as username and very long random password notice that responce time is increased
- this is probebly application first check username in backend if username is correct than it check password .
- X-Forwarded-For header is used to bypass ip protection

## Solution:
- on intruder select X-Forwarded-For value and username as parameter
- for password use random long password
- ran pitchfork
- filter out unique username via responce received 
- username : aix
- ran password bruteforce attack
- filter password via status code
- password : aaaaaa