2025-07-23 18:22
Tags:  
# Rust

Rust is a low-level programming for developing fast and reliable software, it is a compiled statically-typed language with no garbage collection while applying strict rules to preserve better memory management.


## Installation

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

When your project is finally ready for release, you can use cargo build --release to compile it with optimizations. This command will create an executable in target/release instead of target/debug. The optimizations make your Rust code run faster, but turning them on lengthens the time it takes for your program to compile. This is why there are two different profiles: one for development, when you want to rebuild quickly and often, and another for building the final program you’ll give to a user that won’t be rebuilt repeatedly and that will run as fast as possible. If you’re benchmarking your code’s running time, be sure to run cargo build --release and benchmark with the executable in target/release.
## Basics



# References

https://doc.rust-lang.org/book/ch01-03-hello-cargo.html