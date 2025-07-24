2025-07-24 15:26
Tags: 

- Variables are created immutable, meaning this code is invalid:
```rust
let x = 6;
x = 7;
```

- To make mutable variables, you have to prepend `mut` keyword, like this:
```rust
let 
```