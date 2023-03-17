---
{"dg-publish":true,"permalink":"/notes/c-compilation-process/","tags":[null]}
---



# [[Notes/C++\|C++]] Compilation Process

[[Notes/C++\|C++]] is a powerful and versatile [[Notes/Programming\|programming]] language that can be used for various purposes, such as system [[Notes/Programming\|programming]], game development, web development, and more. However, before a [[Notes/C++\|C++]] program can run on a computer, it has to go through several steps of transformation from human-readable code to machine-executable code. This process is called compilation and it involves three main stages: preprocessing, compilation, and linking.

## Preprocessing

The first stage of compilation is preprocessing. In this stage, the preprocessor takes a [[Notes/C++\|C++]] source code file and deals with the preprocessor directives, such as `#include`, `#define`, `#ifdef`, etc. The preprocessor directives are instructions for the preprocessor to modify the source code before passing it to the [[Notes/Compiler\|compiler]]. For example, the `#include` directive tells the preprocessor to insert the contents of another file at the specified location. The `#define` directive tells the preprocessor to replace a certain identifier with a given value or expression throughout the source code. The `#ifdef` directive tells the preprocessor to conditionally include or exclude some parts of the code depending on whether a certain macro is defined or not.

The output of this stage is a "pure" [[Notes/C++\|C++]] file without preprocessor directives. This file is also called a [[Notes/Translation Unit in C++\|translation unit]] because it contains all the information needed by the [[Notes/Compiler\|compiler]] to translate one source file into an object file.

## Compilation

The second stage of compilation is compilation itself. In this stage, the [[Notes/Compiler\|compiler]] takes each [[Notes/Translation Unit in C++\|translation unit]] and converts it into an object file. An object file is a binary file that contains machine code instructions for one [[Notes/Translation Unit in C++\|translation unit]] along with some additional information, such as symbols (names of variables and functions), relocation entries (addresses that need to be adjusted when linking), and debugging information (source code location and variable values).

The [[Notes/Compiler\|compiler]] performs several tasks during this stage, such as lexical analysis (breaking down the source code into tokens), syntax analysis (checking if the tokens follow the rules of [[Notes/C++\|C++]] grammar), semantic analysis (checking if the tokens make sense in terms of types, scopes, declarations, etc.), optimization (improving the performance or size of the generated code), and code generation (producing machine code instructions).

The output of this stage is one object file per [[Notes/Translation Unit in C++\|translation unit]]. These object files are not yet executable because they may contain unresolved references to symbols defined in other translation units or external libraries.

## Linking

The third and final stage of compilation is linking. In this stage, the linker takes all
the object files produced by the [[Notes/Compiler\|compiler]] and combines them into one executable file or library. The linker also resolves all the unresolved references by matching them with their definitions in other object files or external libraries.

The linker performs several tasks during this stage, such as symbol resolution (finding definitions for undefined symbols),
relocation (adjusting addresses according to their final locations), and library inclusion (adding external libraries required by the program).

The output of this stage is an executable file or library that can run on
a computer.

## Conclusion

In summary, the [[Notes/C++\|C++]] compilation process consists of three stages: preprocessing, compilation, and linking.
Each stage transforms the source code into a different form until it becomes a machine-executable code.
Understanding how the compilation process works can help you write better [[Notes/C++\|C++]] programs, debug errors, and optimize performance.

