# CS100 rshell Assignment 4
==========================

Authors
-------------
Thomas Lee
tlee066@ucr.edu

Kimberly Wu
kwu017@ucr.edu 

Repository
--------------
https://github.com/tlee066/Rshell

Summary
--------------
***rshell*** is a command shell program, created to have the ability to implement BASH commands. rshell
prints a command prompt (ex. $) then reads user input on one line. 

Commands syntax:
```
executable [ argumentList ] [ connector cmd ]
```
Available Connectors:
```
&&, ||, ;
```
Comments are supported in ***rshell***.
Anything after the # symbol will be considered a comment.

Connector Descriptions
---------
; (semicolon) - if a command is followed by ;, the next command is always executed.

&& (and) - if a command is followed by &&, the next command is executed only if the first succeeds.

|| (or) - if a command is followed by ||, the next command is executed only if the first fails.

Test Scripts
----------
Our version of ***rshell*** comes with multiple testing scripts designed to display proper functionality
of our program. To run any of the scrips, navigate to the tests directory and enter:
```
./<scriptname>
```
Scripts include:
```
append_redirect_test.sh		#tests appending redirection
input_redirect_test.sh		#tests input redirection
output_redirect_test.sh		#tests output redirection
pipe_test.sh				#tests piping

```
To run rshell
---------
Open the terminal and run these commands:
```
1. git clone https://github.com/tlee066/Rshell.git
2. cd Rshell
3. git checkout assn4
4. make
5. ./bin/rshell
```
Known Bugs
--------
1. Does not handle quotations. (ex. echo "Hello world" should print hello world, but instead rshell prints the entire string including quotations "hello world".)
2. As of now multiple precedence operators (parentheses) work, when they shouldn't. (ex. ((ls)) should not work, but our program treats them as balanced operators and executes normally.)
3. Piping test script has a few errors when run, but running the exact same test cases with normal program execution does not yield any errors.

