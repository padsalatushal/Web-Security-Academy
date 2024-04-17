# Lab 04 : Broken brute-force protection, IP block

## Overview:
- Level : PRACTITIONER
- This lab is vulnerable due to a logic flaw in its password brute-force protection. To solve the lab, brute-force the victim's password, then log in and access their account page.
- Your credentials: wiener:peter
- Victim's username: carlos

## Analysis:
- login with given credentails
wiener : peter
- they have ip protection 


## Solution:
- inorder to perform bruteforce attack and bypass ip blocking
- every 3 incorrect request our ip is blocked 
- to bypass ip blocking login with our correct credential
- select username and password as paratmeter for pitchfork attack 
- username list should be like  
    wiener
    carlos 
    wiener
    carlos 
    and so on

- password list should be like 
    peter
    123456
    peter
    password
    peter
    12345678
    peter
    qwerty
    peter
    123456789
    peter
    12345
    peter
    1234
    peter
    111111