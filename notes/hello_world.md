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
