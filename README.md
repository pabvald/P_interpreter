## Extension of the the interprerter created by Dušan Kolář.


## Original README by  Dušan Kolář.
This is a small DEMO intepreter exploiting flex and bison compilers.
See end of read.me for versions used, even if other versions could be
used as well.

This software was created by Dušan Kolář solely for edicational purposes.
Absolutely no warranty.

It can be used under GPL 3.0 license


List of of files:
-  **astree.c**   - abstract syntax tree creation and interpretation
-  astree.h   - header file for abstract syntax tree module
-  inter01.l  - lex analyzer specification for flex
-  inter01.y  - syntax parser specification for bison
-  _mk        - simple shell script to build the parser
-  README.md    - this file
-  stduse.c   - a small library of overrided standardly used functions
-  stduse.h   - header file for this library
-  symtab.c   - simple symbol table based on binary tree
-  symtab.h   - header file for this symbol table implementation
-  token.h    - definitions of tags and standard macros to use the attributes

Language parsed:
A very simple line oriented language, supported feattures:
empty line - no action
print expression - prints expression value to standard output
print string - prints string enclosed in double quoutes
print string expression - prints string and directly behind it value of the expression
let variable = expression - assigns value of the expression to the variable
read variable - reads floating point value from standard input, which stores to variable
read string variable - prints string to standard output and reads floating point value to variable

It is case insensitive language.

Expression supports floating point numbers only (integer is treated as a floating
point). Expression can contain variables, floating point constants, brackets,
standard binary operators for addition, subtraction, multiplication, division.
Also power operator (^) is included, it is right associative, though. Next,
C like operators for comparison of values (<, <=, ==, >=, >, !=), operators
for logical and (&&) and logical or (!!). As unary operators, unary plus, minus
and logical negation (!) can be used. Finally, C-like ternary operator can be used
( ? : ). Moreover, functions for sinus (sin), cosinus (cos), and tangets (tan)
are included.

---------------------------
Used versions of compiler compilers:

flex 2.6.4

bison (GNU Bison) 3.0.4
Written by Robert Corbett and Richard Stallman.
Copyright (C) 2015 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

