# Lab 02 : SQL injection vulnerability allowing login bypass

## Overview:
- Level : APPRENTICE
- SQL injection on login fuctionality
- End goal: login as administrator

## Analysis:
- login as admin:admin and capture request
- put ' in username or password and it give 500 internal server error

## Solution:
- payload : ' OR 1=1--


