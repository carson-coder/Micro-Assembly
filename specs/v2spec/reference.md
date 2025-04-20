## Reference

This document provides a quick reference for the Micro-Assembly v2 specification. For detailed explanations and examples, please refer to the main documentation files.

### Syntax Conventions

*   **Case Sensitivity:** Instructions are case-insensitive (`MOV` is the same as `mov`). Register names and labels are case-sensitive (`R1` is different from `r1`).
*   **Arguments:** Arguments are separated by spaces, not commas (e.g., `MOV RAX RBX`).
*   **Memory Addresses:** Memory addresses are typically prefixed with a dollar sign (`$`), e.g., `IN $1000`, `DB $1 "String"`.
*   **Labels:** Labels defined with `LBL` are referenced using a hashtag (`#`) prefix in jump instructions (e.g., `JMP #loop`).
*   **External Calls:** Function calls to external code (like MNI) do not use a dollar sign (`$`) prefix, just the namespace and function name (e.g., `MNI Math.sin`).
*   **Immediate Values:** Immediate values (constants) are not prefixed with a dollar sign (`$`), e.g., `MOV RAX 5`.
*   **Strings:** Strings are enclosed in double quotes (`"`), e.g., `DB "Hello, World!"`.
*   **Comments:** (From the start till the end, e.g., `meow ; hello world` - )
*   **Numeric Values:** All numeric values are treated as 64-bit integers unless specified otherwise.

### Registers

*   **General Purpose:** `RAX`, `RBX`, `RCX`, `RDX`, `RSI`, `RDI`
*   **Stack Pointers:** `RBP` (Base Pointer), `RSP` (Stack Pointer)
*   **Instruction Pointer:** `RIP`
*   **Numbered General Purpose:** `R0` through `R15`

*Note:* Be careful when manipulating `RSP` and `RBP`. Always balance `PUSH` and `POP` operations.

### Instruction Set Overview

Micro-Assembly v2 includes instructions for:

*   **Data Movement:** `MOV`, `MOVADDR`, `MOVTO`
*   **Arithmetic:** `ADD`, `SUB`, `MUL`, `DIV`, `INC`
*   **Bitwise Logic:** `AND`, `OR`, `XOR`, `NOT`, `SHL`, `SHR`
*   **Flow Control:** `JMP`, `CMP`, `JE`, `JNE`, `JL`, `JG`, `JLE`, `JGE`, `CALL`, `RET` (*RET is implied by CALL but not explicitly listed*)
*   **Stack Operations:** `PUSH`, `POP`, `ENTER`, `LEAVE`
*   **I/O:** `IN`, `OUT`, `COUT`
*   **Memory/String Operations:** `DB`, `COPY`, `FILL`, `CMP_MEM`
*   **Program Control:** `HLT`, `EXIT`
*   **Command Line Arguments:** `ARGC`, `GETARG`
*   **Labels:** `LBL`

For a detailed description of each instruction, see the [v2 Instruction Set Documentation](v2instructions.md).

### Micro Native Interface (MNI)

MNI allows Micro-Assembly code to interact with native host functions (e.g., Java via JMASM, Python via PyMasm).

*   **Syntax:** `MNI <Namespace>.<Function> [Arguments...]`
*   **Available Functionality (Examples):**
    *   Math (`Math.sin`, `Math.sqrt`, `Math.random`)
    *   Memory Management (`Memory.allocate`, `Memory.free`)
    *   Advanced String Operations (`StringOperations.toUpper`, `StringOperations.parseInt`)
    *   Data Structures (`DataStructures.createList`, `DataStructures.createMap`)
    *   Network Operations (`Network.httpGet`, `Network.openSocket`)
    *   File System (`FileSystem.open`, `FileSystem.read`, `FileSystem.delete`)
    *   System Operations (`System.exec`, `System.sleep`, `System.getEnv`)
    *   Debugging (`Debug.breakpoint`, `Debug.dumpRegisters`)

For a comprehensive list of MNI functions, refer to the MNI section in the [v2 Instruction Set Documentation](v2instructions.md).