# Elisp-wasm
compiler for elisp into wasm (web assembly)
* Why?
Why not just have an API to emacs running on a back-end?
To-do
    Lexical analysis: The first stage of the compiler is to convert the source code, written in elisp, into a stream of tokens. This is done using a lexical analyzer, also known as a lexer or scanner. The lexer reads the source code and breaks it up into individual tokens, such as keywords, identifiers, and operators.

    Syntax analysis: The next stage is to take the stream of tokens produced by the lexer and use them to create an abstract syntax tree (AST). This is done using a parser, which analyzes the structure of the code and creates a tree-like representation of the program.

    Semantic analysis: The AST is then passed to the semantic analysis stage, where the compiler checks for errors and verifies that the program is semantically correct. This includes checking that variables are declared before they are used, that functions are called with the correct number and types of arguments, and that the program follows the rules of the elisp language.

    Code generation: Once the program has been verified to be semantically correct, the compiler generates the target code, in this case wasm. This typically involves mapping the elisp code to the corresponding wasm instructions, and creating a binary file that can be executed by a wasm runtime.

    Optimization: The final stage is to optimize the generated code for better performance. This can include techniques like constant folding, instruction scheduling, and register allocation.
