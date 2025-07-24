2025-07-24 15:45
Tags: 

- Every value in Rust is of a certain _data type_, which tells Rust what kind of data is being specified so it knows how to work with that data.

```rust
let x: i32 = 6; // x is a 32-bit signed integer
```

# Scaler Types

- A _scalar_ type represents a single value. Rust has four primary scalar types: [[Integers]], [[Floating-point Numbers]], [[Booleans]], and [[Characters]].

## [[Integers]]

- [[Integers]] in rust are represented by `i#` or `u#`, where `i` stands for [[signed integers]], and `u` stands for [[unsigned integers]], and `#` is the a number representing the length of the variable in bits, it can be 8, 16, 32, 64 or 128.

- There's also `isize` and `usize`, whose sizes depend on the architecture of the running machine, 32-bit or 64-bit.

- [[Integer]] literals can have type suffixes to designate the type of the integer, such as `12u8`.

- [[Integer]] literals can have visual separators to make reading easier, such as:-
	- `1_000_000` (one million)
	- `0xff` (255 in [[Hex]])
	- `0o77` (63 in [[Octal]])
	- `0b1111_0000` (240 in [[Binary]])
	- `b'A'` ([[Integer]] value of letter 'A' in [[ASCII]])

## [[Floating-point Numbers]]

- In Rust, there is `f32` and `f64`.

### [Numeric Operations](https://doc.rust-lang.org/book/ch03-02-data-types.html#numeric-operations)

```rust
fn main() {
    // addition
    let sum = 5 + 10;

    // subtraction
    let difference = 95.5 - 4.3;

    // multiplication
    let product = 4 * 30;

    // division
    let quotient = 56.7 / 32.2;
    let truncated = -5 / 3; // Results in -1

    // remainder
    let remainder = 43 % 5;
}
```

## [[Booleans]]

- [[Booleans]] are represented using `bool`, they are one byte in size.

## [[Characters]]

- [[Rust]]’s `char` type is the language’s most primitive alphabetic type.

- `char` values are put in single-quotes, unlike string values, which are put in double-quotes.

- [[Rust]]’s `char` type is four bytes in size and represents a Unicode Scalar Value, which means it can represent a lot more than just ASCII. Accented letters; Chinese, Japanese, and Korean characters; emoji; and zero-width spaces are all valid `char` values in [[Rust]].


# Compound Types

- _Compound types_ can group multiple values into one type. Rust has two primitive compound types: [[Tuples]] and [[Arrays]].

## Tuples

- A tuple is a way to group a number of values ta