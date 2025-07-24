2025-07-24 15:45
Tags: 

- Every value in Rust is of a certain _data type_, which tells Rust what kind of data is being specified so it knows how to work with that data.

```rust
let x: i32 = 6; // x is a 32-bit signed integer
```

# Scaler Types

- A _scalar_ type represents a single value. Rust has four primary scalar types: integers, floating-point numbers, Booleans, and characters.

## Integers

- Integers in rust are represented by `i#` or `u#`, where `i` stands for [[signed integers]], and `u` stands for [[unsigned integers]], and `#` is the a number representing the length of the variable in bits, it can 

| 8-bit   | `i8`    | `u8`    |
| ------- | ------- | ------- |
| 16-bit  | `i16`   | `u16`   |
| 32-bit  | `i32`   | `u32`   |
| 64-bit  | `i64`   | `u64`   |
| 128-bit | `i128`  | `u128`  |
| arch    | `isize` | `usize` |
