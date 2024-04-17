# Lab 08 : 2FA broken logic

## Overview:
- Level : PRACTITIONER
- This lab's two-factor authentication is vulnerable due to its flawed logic. To solve the lab, access Carlos's account page.

Your credentials: wiener:peter
Victim's username: carlos

## Analysis:
- login as wiener : peter credetails for getting code use email client 
- observe the flow of authentication

## Solution:
- get /login2 request is use for generating mfa code
- sent that get /login2 request to repeter and in cookie section change the value from wiener to carlos and send that request. now the mfa code for carlos user is generted.
- go back to login page and login with wiener user
- submit any random invalid mfa code 
- now send new post /login2 to intruder
- change the value from wiener to carlos in cookie section and select mfa code value as parameter
- ran bruteforce account
- filter out valid mfa code request via 302 request 
- on that request right click and then open in browser