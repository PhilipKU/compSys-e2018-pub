# Exercises for 3/9-2018

Author: Michael Kirkedal Thomsen <kirkedal@acm.org>

These exercises are intended to give your a first quick feeling of C and prepare you for what comes in A0. Use the exercise classes to get help. Also you This is not part of the assignment.

For all of the below, you should use `make` to build your programs. To
parametrize `make` to build with all the necessary compiler flags, start by
writing down a `Makefile` containing the following:

```
CC=gcc
CFLAGS=-std=c11 -Wall -Werror -Wextra -pedantic -g
```

Now, to compile the programs below, just `make` them. For example:

```
$ make mynameis
```

* I will use "print" as a term for writing to stdout

## Printing in C
Write a C program `mynameis` that prints your name.

## Input arguments in C
Write a C program `repeatme`  that given a `string` as argument, prints the string twice on separate lines.

If the program gets a number of arguments that is different from 1 it should print "`Wrong number of arguments`".

## Input argument validation
Write a C program that `noAs` that given a `string` as argument, does either of the following. 

  * If the first character of the string is an the `char` `A` it prints "`No beginning A's are allowed`",
  * otherwise it prints the given string.

Reminder: Consider how `string`s are formatted in C. 

Note: reuse your argument validation from before. You can just as well learn it from the beginning. _Always sanitise your input._


## File printing
Write a C program `fileecho` that given a filename (formatted as a `string`) opens the file in read-only mode, reads its content and prints this.

## File check
Write a C program `fileexist` that given a filename (formatted as a `string`) checks if it can read the file and prints a reasonable status message.

## File content validation
Write a C program `noAshere` that given a filename (formatted as a `string`) opens the file in read-only mode, reads its content and checks if it contains any character `A`. If it contains an `A` print "`No A's are allowed`" otherwise print "`Ok`".



## Simple Caesar Cipher (bonus)
Write a C program `caesar` that is given a `string` as argument (we will treat this as a plain text) prints the string where all characters are replaced with the character with one higher `char` value.

The standard Caesar cipher (also called shift cipher), used for communicating secret messages in ancient times, shifts all letters _n_ places in the alphabet, where _n_ then is the secret key. For simplicity we have here fixed _n_ to 1 and do not use consider the alphabet a finite field.

If you are interested, you can read more at [https://learncryptography.com/classical-encryption/caesar-cipher](https://learncryptography.com/classical-encryption/caesar-cipher)

### Extras
You are welcome to extend this with

  * an extra argument that is read to an integer, such you can implement the full Caesar cipher,
  * a flag (e.g. argument "-enc" and "-dec"), such that you program can perform encryption and decryption,
  * reading plain text from a filename and writing it to a different filename,
  * ensure that you only use the letters of the ASCII table; ensure that the case of each letter is preserved.
