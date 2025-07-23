2025-07-23 21:45
Tags: 

# Installation

- Install [[rustup]] cli tool managing rust versions and associated tools.
- Install a linker, could just be the C linker that comes with [[GCC]] or [[Clang]].
- Install [[cargo]] used for build the rust app and managing its dependancies.


## Create a project with cargo

``` bash
cargo new hello_cargo
$ cd hello_cargo
```

This initialised a [[Rust]] project, it also initialises it as a [[Git]] repo, [[Git]] files won’t be generated if you run cargo new within an existing [[Git]] repository; you can override this behaviour by using:

``` bash
cargo new --vcs=git
```

Cargo project has a config file _Cargo.toml_ which is a [[TOML]] file, it has 2 sections:

- `[package]` which specifies configurations for packages.
- `[dependencies]` which specifies the dependencies of the project

Build the project using `cargo build`, this command creates an executable file in _target/debug/hello_cargo_ rather than in your current directory. Because the default build is a debug build.

`cargo run`, this builds and runs in one command.

`cargo check`, this command quickly checks your code to make sure it compiles but doesn’t produce an executable.

`cargo build --release` is used when the project is finally ready for release, it compiles with optimizations and faster run.

If benchmarking, compile in release mode.

# References

https://doc.rust-lang.org/book/ch01-03-hello-cargo.html