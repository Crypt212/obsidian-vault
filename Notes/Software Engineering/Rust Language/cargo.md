2025-07-23 19:20
Tags: 

# cargo

Cargo is a tool to build [[Rust]] apps and manage its dependancies.

## Create a project with cargo

```bash
cargo new hello_cargo
$ cd hello_cargo
```

This initialised a [[Rust]] project, it also initialises it as a [[Git]] repo, Git [[files]] won’t be generated if you run cargo new within an existing [[Git]] repository; you can override this behavior by using:
``` bash
cargo new --vcs=git
```