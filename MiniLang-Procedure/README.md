# MiniLang – Procedures

Extension of the MiniLang interpreter that introduces **procedure support with call-by-value semantics**, enabling structured and reusable code.

Base project:
[MiniLang](https://github.com/BalaciSofia/MiniLang)

## Added Features

* Shared **ProcTable** for storing procedures
* Support for defining procedures with parameters
* `call fname(exp1, ..., expn)` – invokes a procedure
* Automatic `return` handling
* Stack of **Symbol Tables** for proper variable scoping

Implements **call-by-value procedures** using a stack of symbol tables to handle local scope and restore the caller’s context after execution.

