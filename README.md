## Programming Language Parser
Parser for programming language based on syntax-directed translation scheme, implemented using Lex and Yacc.

The parser generates Java assembly code, which can then be translated to Java bytecode by [Jasmin](http://jasmin.sourceforge.net/) and run on Java Virtual Machine.

Assembly code is generated along with warning messages for semantic errors, if any. The parser terminates immediately when a syntax error is found.

## How to Run
Generate parser using Lex and Yacc.
```
$ make
```

Compile source code using parser.
```
$ ./parser code.p
```

Convert to Java bytecode using Jasmin.
```
$ java -jar jasmin-2.4/jasmin.jar code.j
```

Run the program.
```
$ java code
```

Remove temporary files.
```
$ make clean
$ rm code.j code.class
```

## Language Features
Declarations for global/local variables and constants

Arithmetic and boolean expressions

Assignments

Print statements

Read statements

Compound statements

If statements and for/while loops

Procedure declarations and invocations
