2025-07-24 15:45
Tags: 

- Every value in Rust is of a certain _data type_, which tells Rust what kind of data is being specified so it knows how to work with that data.

```rust
let x: i32 = 6; // x is a 32-bit signed integer
```

# Scaler Types

- A _scalar_ type represents a single value. Rust has four primary scalar types: integers, floating-point numbers, Booleans, and characters.

## Integers

- Integers in rust are represented by `i#` or `u#`, where `i` stands for [[signed integers]], and `u` stands for [[unsigned integers]], and `#` is the a number representing the length of the variable in bits, it can be 8, 16, 32, 64 or 128.

- There's also `isize` and `usize`, whose sizes depend on the architecture of the running machine, 32-bit or 64-bit.

- [[Integer]] literals can have type suffixes to designate the type of the integer, such as `12u8`.

- [[Integer]] literals can have visual separators to make reading easier, such as:-
	- `1_000_000` (one million).
	- `0xff` (, `0o77`, `0b1111_0000`, `b'A'`