# Samplaí

This directory contains some installation instructions and basic examples of how to write procedures using Áireamhán.

# Installation

The language can be installed from PyPI, ```pip install aireamhan```. Once installed you can run the REPL or run procedures directly from files.

```
$ áireamhán [path/to/procedure.air]
```

# Features

The language supports ```int```, ```float```, ```complex```, ```str``` and Boolean types, where the Booles are defined as ```#tá``` and ```#níl```. Like Lisp it is fully parenthesised and uses Polish (prefix) Notation. Like Lisp it also makes use of conses (which are implemented as Python lists), and uses recursion and maps rather than loops. Unlike Python, Áireamhán provides support for tail recursive optimisation, an example of this can be seen in ```iolrán.air```. Below are the operators and procedures implemented.

| Operator                           | Definition                      |
|-------------------------------|-----------------------------------|
| níl, agus, <, >, =, <=, >=    | not, and, other logical operators |
| frmh(int/float)               | complex sqrt                      |
| dearbhluach(int/float)       | abs                               |
| uas(liosta)                   | max                               |
| íos(liosta)                   | min                               |
| cothrom_le?(x, x)             | equal to                          |
| ionann?(x, x)                 | identical to                      |
| fad(liosta)                   | length                            |
| cons(x, liosta)               | cons                              |
| liosta(x*)                    | create a list                     |
| liosta?(x)                    | is list?                          |
| folamh?(liosta)               | is list empty?                    |
| siombail?(x)                  | is symbol?                        |
| boole?(x)                     | is Boolean                        |
| cuir_le(f, x*)                | apply function f to args          |
| mapáil(f, liosta/cons)        | map function onto iterable        |
| scag(f, liosta/cons)          | filter iterable by Boolean f      |
| lódáil(fname)                 | load and execute file             |
| léigh(fname)                  | read file contents                |
| oscail_comhad_ionchuir(fname) | open file in read mode            |
| dún_comhad_ionchuir           | close read mode file              |
| oscail_comhad_aschur          | open output file                  |
| dún_comhad_aschur             | close output file                 |
| dac?                          | is EOF object                     |
| scríobh(x, [f])               | write x, to file if f is given    |
| sainigh                       | define variable value             |
| cuir!                         | set variable                      |
