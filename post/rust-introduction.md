---
title: A quick introduction to Rust
author: Tristan Lukens
date: June 2 2022
tags: [introduction, rust, programming]
---

Rust is fantastic.

Even though you need to initialise a project first (that is, if you want to things the correct way).

## Prerequisites

I think familiarity with the \*nix terminal would be mandatory.

## Installing Rust

Most people use a tool called `rustup` for managing their Rust installations. I'm not going to paste the command for installation right here; that's available [here](https://www.rust-lang.org/tools/install), which is the official Rust website and their official installation page.

If you use Windows, first of all, for the love of God, please move to Linux, and second of all, there's steps for that on the web page I linked.

It's a bad habit to just run a command which you can't verify isn't malicious, which is why I'm linking to the official web page instead of blatantly letting you copy an installation command you don't know.

This command will guide you through the installation.

## Initialising a new project

1. go to the dir you want the project to live in
2. run `cargo init hello`
3. run `cd hello`
4. open the project in your text editor. I'll walk through it

## The project

The project structure looks like this upon initialisation.

```
hello
├── .gitignore
├── Cargo.toml
└── src
    └── main.rs
```

`.gitignore` ignores some files in git. If you know what git is, fantastic. If not, don't worry. It's explained quite well [here](https://docs.github.com/en/get-started/quickstart/set-up-git), the GitHub docs.

`Cargo.toml` is like the `go.mod` (go), `package.json` (js) or `Gemfile` (ruby) of Rust; it is the place where you put your dependencies and other metadata about your project. When you build your project, a `Cargo.lock` file will be generated, which is a file where the exact versions of your dependencies live. Cargo is Rusts package manager.

The `src/` folder is where the code of your project lives. This is what's compiled.

`main.rs` is the entry point of your program. By default, its contents are the following.

```rust
fn main() {
    println!("Hello, world!");
}
```

This uses a main function, which is used as an entry point to your program. It uses the `println!` macro to print `Hello, world!` to the console.

## Some basic `cargo` subcommands

### `cargo run`

Performs checks, compiles the program (everything in `src/`) and runs the program.

### `cargo build`

Builds the program into a `target/` folder.

### `cargo check`

Check if the program is valid to be compiled. This is faster than generating the executable with it.

## Extra: single files

You **can** use only a single file and compile it to a binary with `rustc`. Here's a set of commands that'd do that.

```
mkdir foo
cd foo/
touch main.rs
echo 'fn main() { println!("Hello, world!"); }' >> main.rs
rustc main.rs
./main
```

First create a directory, go into it, create `main.rs` (this file could have any name), then echo the regular main function that prints "Hello, world!" into the file, compile it and run the binary.

---

🦀
