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

- Constants are always immutable, they don't have `mut` prefix and they must always be explicitly annotated with its used type. 

- Constants can be declared in any scope, including the global scope, which makes them useful for values that many parts of code need to know about.

- The last difference is that constants may be set only to a constant expression, not the result of a value that could only be computed at runtime.

# Shadowing

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