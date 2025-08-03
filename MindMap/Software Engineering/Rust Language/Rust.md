2025-07-24 12:13
Tags: 

Rust is a low-level programming for developing fast and reliable software, it is a compiled statically-typed language with no garbage collection while applying strict rules to preserve better memory management.

# Installation

- Install [[rustup]] CLI tool managing rust versions and associated tools.
- Install a linker, could just be the C linker that comes with [[GCC]] or [[Clang]].
- Install [[cargo]] used for build the rust app and managing its dependencies.

# Basics

## Variables and Mutability

### Immutable

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
### Constant

- Constants are always immutable, they don't have `mut` prefix and they must always be explicitly annotated with its used type. 

- Constants can be declared in any scope, including the global scope, which makes them useful for values that many parts of code need to know about.

- The last difference is that constants may be set only to a constant expression, not the result of a value that could only be computed at runtime.

### Shadowing

- The process of re-declaring the variable with the same name, it can change the type of the variable too:-
```rust
let x = 6; // this is now 6 
let x = x + 6; // this is now 12
let x = "ahmed"; // this now "ahmed"
```

- The shadowing lasts until the end of its scope, for example:-
```rust
let x = 6;
println!("{}", x); // 6
{
	let x = "ahmed";
	println!("{}", x); // "ahmed"
}
println!("{}", x); // 5
```

#### Differences between shadowing and mutability

- Shadowing is different from marking a variable as `mut` because we’ll get a compile-time error if we accidentally try to reassign to this variable without using the `let` keyword. By using `let`, we can perform a few transformations on a value but have the variable be immutable after those transformations have been completed.

- The other difference between `mut` and shadowing is that because we’re effectively creating a new variable when we use the `let` keyword again, we can change the type of the value but reuse the same name.



## Data Types

- Every value in Rust is of a certain _data type_, which tells Rust what kind of data is being specified so it knows how to work with that data.

```rust
let x: i32 = 6; // x is a 32-bit signed integer
```

### Scaler Types

- A _scalar_ type represents a single value. Rust has four primary scalar types: [[Integers]], [[Floating-point Numbers]], [[Booleans]], and [[Characters]].

### Compound Types

- _Compound types_ can group multiple values into one type. Rust has two primitive compound types: [[Tuples]] and [[MindMap/Software Engineering/Rust Language/Arrays|Arrays]].
## 
# References

https://doc.rust-lang.org/book/ch01-03-hello-cargo.html