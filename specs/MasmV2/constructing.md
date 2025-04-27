# constructing interpreters and or compilers

Micro-Assembly primarily has 3 fully spec compliant interpreter's plus one of them being a bytecode compiler. but your not here for this are you?

in order to construct a interpreter you can follow these:

1. find a spec.
    there's multiple specs availabe, v1 and v2 (current as of apr 25, 2025) are the currently existing
    ones we have.

2. choose a language.
    you have multiple languages to choose from, Csharp, c++, c, ect.
    find a language that suites your needs, then have fun.

3. implement the spec.
    with your language and spec chosen, go ahead and open the spec and implement functions that act on said spec:
        mov, takes 2 registers or a register then value and moves it into the dest by order of 
        "mov dest src"