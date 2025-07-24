2025-07-24 15:26
Tags: 

# Immutable

- Variables are created immutable, meaning this code is invalid:
```rust
let x = 6;
x = 7;
```

- To make mutable variables, you have to prepend `mut` keyword, like this:
```rust
let mut x = 6;
x = 8;
```

- Immutability's is important when you need to make a variable in the some point of the code that is going to hold a value that you want to make sure that it won't change afterwards.
# Constant

- Constants 