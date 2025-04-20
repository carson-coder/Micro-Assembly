
# Micro-Assembly

This repository serves as the central hub for the specification, documentation, and examples related to the Micro-Assembly language.


Here you can find:
*   Documentation
*   Language specifications (including different versions)
*   Examples and usage guides (potentially)

## Specification

The current development focuses on the **v2 Specification**. Please note that this specification is currently a **work in progress**, and details may change.

*   **Instruction Set:** Find the detailed list of instructions, registers, addressing modes, and Micro Native Interface (MNI) functions in the [v2 Instruction Set Documentation](specs/v2spec/v2instructions.md).
*   **General Notes:** Read about syntax conventions and development philosophy in the [v2 Spec Notes](specs/v2spec/notes.md).


## Key Features (v2 Spec) of the current spec

*   Standard arithmetic, logic, and flow control instructions.
*   Stack operations (PUSH, POP, ENTER, LEAVE).
*   I/O operations (IN, OUT, COUT).
*   Memory manipulation (DB, COPY, FILL).
*   Bitwise operations (AND, OR, XOR, NOT, SHL, SHR).
*   Extended memory addressing (MOVADDR, MOVTO).
*   **Micro Native Interface (MNI):** Allows interaction with native code (e.g., Java via JMASM, Python via PyMasm) for extended functionality like:
    *   Math operations
    *   Memory management
    *   Advanced string operations
    *   Data structures (Lists, Maps)
    *   Network operations
    *   File system access
    *   System calls
    *   Debugging tools

## License

This project is licensed under the GNU Affero General Public License v3.0. See the [LICENSE](LICENSE) file for full details.


Please refer to the specific directories within this repository, such as [`docs/`](docs/) and [`specs/`](specs/), for detailed information. The content and structure may evolve over time.