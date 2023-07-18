
## Conventions

* When naming a file, always use the snake_case convention. For e.g. - `hello_world.rs` instead of `helloworld.rs`
* It’s good style to place the opening curly bracket on the same line as the function declaration, adding one space in between.
* Rust's style is to indent with four spaces, not a tab.
* In order to adhere to the standard convention, `rustfmt` tool can be used.

## Chapter 1 - Getting Started

#### Anatomy of a Rust program

* Basic anatomy of a rust program:

```rust
fn main() {
	println!("Hello, world!");
}
```

* These lines define a function named `main`. It is a special function because it is the entry point of the program, i.e., it is the always the first code that runs in every executable Rust program.
* `println!()` calls a Rust macro. If it had called a function instead, it would be entered as `println()` (without the `!`). The `println!()` macro prints the input string to _stdout_.
* Rust is an _ahead-of-time compiled_ language, meaning you can compile a program and give the executable to someone else, and they can run it even without having Rust installed.

#### Cargo

* Cargo is Rust's build system and package manager.
* In order to create a new Rust project using Cargo, `cargo new --bin ${project_name}` command can be used.
* Basic anatomy of a `Cargo.toml` file:

```toml
[package]
name = "hello_cargo"
version = "0.1.0"
edition = "2021"

# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]
```

* The three lines under the `[package]` determine the project configuration.
* The `[dependencies]` section is used to list and manage any dependencies that are being used in the Rust project. 
* `cargo build`  command is used to build the project and create an executable. The default configuration is *debug*.
* `cargo run`  command not only builds the project, but also runs the executable.
* `cargo check`  command quickly checks the code to make sure it compiles but doesn’t produce an executable.
* Cargo rebuilds the project only when the source code is modified. Otherwise, it just runs the executable.
* When building the project for release, `cargo build --release`  command can be used.

## Chapter 2 - Programming a Guessing Game

```rust

```
* By default, Rust has a set of items defined in the standard library that it brings into the scope of every program. This set is called the _prelude_
* In Rust, variables are _immutable_ by default. Therefore, in order to make the variable mutable, the  `mut`  keyword is used.
* The  `use`  keyword is used to bring a module into scope in Rust.
* & is used to create a reference in Rust.
* The  `read_line`  function takes the user input and appends it to the given string buffer without overwriting it. The string buffer has to mutable so that it's content can be changed.
* The  `expect`  method is defined in the Result enum and is invoked when the instance of the Result type is an  `Err`  value. It will cause the program to crash and display the message that is passed as an argument.