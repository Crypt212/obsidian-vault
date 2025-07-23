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

This initialised a [[Rust]] project, it also initialises it as a [[Git]] repo, Git [[files]] won’t be generated if you run cargo new within an existing [[Git]] repository; you can override this behavior by using:

``` bash
cargo new --vcs=git
```

Cargo project has a config file _Cargo.toml_, it has 2 sections:
- [package] 
## Basics

#

# References

