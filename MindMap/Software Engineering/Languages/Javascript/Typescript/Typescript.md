- It's basically [[JavaScript]] with strict-typing added to it.
# Setup
- We need to install some packages:-
### `typescript` (The Compiler/Language)
- **What it is:** This is **the core package**. It's the **Typescript** language itself, which includes two key things:
    1. **The Compiler Tool (`tsc`)**: The program that trans-piles your `.ts` files into `.js` files.
    2. **The Language Service**: The "brains" that provides code analysis, error checking, and editor features like autocomplete and refactoring tools. This is what powers your IDE's **Typescript** intelligence.
### `ts-node` (The Direct Runner)
- **What it is:** A community package that lets you run **Typescript** files directly, without a separate compilation step. It does two things on the fly:
       1. **Trans-piles** your **Typescript** to [[Javascript]] (in memory).
       2. **Runs** the resulting [[Javascript]] using [[Node.js]].
# Configuration
- The typescript project is configured using `tsconfig.json` file.
- `compilerOptions` property has properties about the **Typescript** compiler.
- 