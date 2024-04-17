# Lab 07 : 2FA simple bypass

## Overview:
- Level : PRACTITIONER
- This lab's two-factor authentication can be bypassed. You have already obtained a valid username and password, but do not have access to the user's 2FA verification code. To solve the lab, access Carlos's account page.

Your credentials: wiener:peter
Victim's credentials carlos:montoya

## Analysis:
- login as wiener : peter credetails for getting code use email client 
- observe the flow of authentication

## Solution:
- login with victim credential
- when ask for otp change the url from /login2 to /my-account
