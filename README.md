# Elisp-wasm
compiler for elisp into wasm (web assembly)
* Why?
Why not just have an API to emacs running on a back-end?
* To-do
    Lexical analysis: The first stage of the compiler is to convert the source code, written in elisp, into a stream of tokens. This is done using a lexical analyzer, also known as a lexer or scanner. The lexer reads the source code and breaks it up into individual tokens, such as keywords, identifiers, and operators.

    Syntax analysis: The next stage is to take the stream of tokens produced by the lexer and use them to create an abstract syntax tree (AST). This is done using a parser, which analyzes the structure of the code and creates a tree-like representation of the program.

    Semantic analysis: The AST is then passed to the semantic analysis stage, where the compiler checks for errors and verifies that the program is semantically correct. This includes checking that variables are declared before they are used, that functions are called with the correct number and types of arguments, and that the program follows the rules of the elisp language.

    Code generation: Once the program has been verified to be semantically correct, the compiler generates the target code, in this case wasm. This typically involves mapping the elisp code to the corresponding wasm instructions, and creating a binary file that can be executed by a wasm runtime.

    Optimization: The final stage is to optimize the generated code for better performance. This can include techniques like constant folding, instruction scheduling, and register allocation.

* Challenges
    Homoiconicity: Elisp is a homoiconic language, meaning that code and data have the same representation. This makes it difficult to distinguish between the two when translating to wasm, which has a more rigid distinction between code and data.

    Garbage collection: Elisp uses a garbage collector to automatically manage memory, while wasm requires manual memory management. This would require the compiler to insert appropriate wasm instructions to handle memory management.

    Dynamic nature of elisp: Elisp is a dynamic language, which means that types are not declared and can change at runtime. This would make it difficult for the compiler to generate efficient wasm code, as it would have to handle type checking and casting at runtime.

    Elisp runtime environment : Elisp code is executed in a runtime environment provided by an Elisp interpreter, which provides a number of built-in functions and data structures that are not available in a wasm runtime. This would require the compiler to provide equivalents for these in wasm or provide a way to access them.

    Limited support for elisp in wasm: Currently, there is limited support for elisp in wasm, and it may not be possible to use existing tools or libraries to assist in building the compiler. This would require the development of a new toolchain specifically for the task.
