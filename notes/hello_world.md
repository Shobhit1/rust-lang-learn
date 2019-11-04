# Rust

## Introduction to Rust

### Hello World

This is how you write hello world in Rust

```rust
fn main() {
    println!("Hello, world!");
}
```

Compiling and running the program

```bash
rustc main.rs
./main
```

### Anatomy of hello world

```rust
fn main() {

}
```

This is an example of `main` function. The main function is special: : it is always the first code that runs in every executable Rust program.

The `println!` in the above function is called `Rust macro`. If it was a function, it would not have `!` at the end of it.
We would just call `println` to call a function. Using a `!` means that you’re calling a macro instead of a normal function.

We end the line with a semicolon`;`.

> Rust is an ahead-of-time compiled language, meaning you can compile a program and give the executable to someone else, and they can run it even without having Rust installed.

Just compiling with `rustc` is fine for simple programs, but as your project grows, you’ll want to manage all the options and make it easy to share your code.

## Cargo tool

Cargo is Rust’s build system and package manager. This is similar to `package.json` from `nodejs` source codes.
Helps with building your code, downloading the libraries your code depends on and building those libraries.

use `cargo init` to initialize cargo in already existing directory

or `cargo new hello_world` to generate directory `hello_world` which will be auto initialized with following:
`cargo.toml`: TOML file that is based on [toml-lang](https://github.com/toml-lang/toml)
`src/main.rs`: a hello world rust program

`cargo build`: Command that tells cargo to build project. Builds a executable file in `target/debug/`.
`cargo run`: Run the generated executable. Can also run this file using `./target/debug/hello_world`.

`cargo run`also knows when you changed file, where it will compile the files before running; otherwise just runs the previously generated executable.

`Cargo.lock`: This is a lock file similar to `yarn.lock`. This file keeps track of the exact versions of dependencies in your project. Cargo manages its contents for you.

`cargo check`: This command quickly checks your code to make sure it compiles but doesn’t produce an executable
