Commands
========

Usually just expansions, although selective commands are actually macros of a sort. Until dynamic matching and dynamically allocated tables and all the other cool stuff is implemented, any commands will have to be hardcoded into the primary parsing functions.

Features
========
Some of the cool ones:

 - Less syntax
 - Improved wording
 - Statements are shorter
 - If you include a header, its library will automatically be linked when possible
 - If you include a library, all necessary headers will be included, and the library will be automatically linked when possible
 - Use of pointers (Referencing and Dereferencing) is automatic when possible, although you may still manually specify
 - Operator overloading is allowed with Arithmetic and Binary operations; Prioritization is as follows: `Bitwise (not, and, or, shift, etc.)` > `Arithmetic (BEDMAS, modulo (equal to mul/div), etc.)` > `Comparison (==, !=, >, <=, etc.)` > `Logical (not, and, or, xor, etc.)`
 - Extended logical and bitwise operators; new operators: bitwise (~&, ~|, ~^) and logical (!&&, !||, ^^, !^^)
 

Roadmap
=======

- [ ] libc
	- [ ] stdio
	- [ ] stdlib
	- [ ] assert
	- [ ] time

That's really all that I need at the moment, if you need anything yourself, implement it, or better still, help create an additional parser that will allow me to include additional `command-lists` of sorts.

---

Command List
============

i.e.: is on schedule to be implemented ASAP

|Library/Header			|C			|millic	|
|-----------------|----------------|-------|
|libc/stdio|`printf("formatted statement", var1, var2, etc);`|`print "formatted statement" var1 var2 etc`|
|libc/stdio|`scanf("formatted query", &numvar1, string);`|`scan "formatted query" numvar string`|
|libc/stdio|`puts("string");`|`echo "string"`|
|libc/stdio|`gets(string);`|`query string`|
|libc/stdio|`putchar("l");`|`write l`|
|libc/stdio|`c = getchar();`|`read c`|
|libc/stdlib|`buffer = (type*) malloc(sizeof(type) * vars);`|`allocate buffer vars type`|
|libc/stdlib|`buffer = (type*) calloc(vars, sizeof(type));`|`zerocate buffer vars type`|
|libc/stdlib|`buffer = (type*) realloc(buffer, vars * sizeof(type));`|`relocate buffer vars type`|
|libc/stdlib|`free(buffer);`|`delocate buffer`|
|libc/stdlib|`exit(status);`|`exit status`|
|libc/stdlib|`srand(time(NULL));`|`srand time(NULL)`|
|libc/stdlib|`var = rand();`|`random var`
|libc/stdlib|`var = rand() % 5`|`random` [newline] `buffer = result % 5`
|NA|`#include <sysheader.h>`|`header sysheader.h`|
|NA|`-lsyslib`|`lib syslib`|
|NA|`type function(type arg1, type arg2) { code; code; code; return var; }`|`function arg1 type:arg2 { code` [newline] `code` [newline] `code` [newline] `return var }`

Example Code
============

```
lib libc

main
```