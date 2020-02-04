# My Rust first contact

## Installation

Already having [asdf](https://github.com/asdf-vm/asdf) installed locally and running on other projects, I chose to install Rust with an [asdf plugin](https://github.com/code-lever/asdf-rust) built for it.

So, I created this repository with:

```bash
mkdir rustInit
cd rustInit
git init
```

After that, I created the traditional .tool-versions asdf file containing `rust 1.41.0` (latest stable Rust version available at the time) and then run:

```bash
asdf install
```

I've got the following output for this command:

```
info: downloading installer
info: profile set to 'default'
info: default host triple is x86_64-unknown-linux-gnu
info: syncing channel updates for '1.41.0-x86_64-unknown-linux-gnu'
info: latest update on 2020-01-30, rust version 1.41.0 (5e1a79984 2020-01-27)
info: downloading component 'cargo'
info: downloading component 'clippy'
info: downloading component 'rust-docs'
 12.0 MiB /  12.0 MiB (100 %)   4.1 MiB/s in  2s ETA:  0s
info: downloading component 'rust-std'
 17.5 MiB /  17.5 MiB (100 %)   4.5 MiB/s in  4s ETA:  0s
info: downloading component 'rustc'
 57.9 MiB /  57.9 MiB (100 %)   4.8 MiB/s in 12s ETA:  0s
info: downloading component 'rustfmt'
info: installing component 'cargo'
info: installing component 'clippy'
info: installing component 'rust-docs'
info: installing component 'rust-std'
info: installing component 'rustc'
 57.9 MiB /  57.9 MiB (100 %)  17.9 MiB/s in  3s ETA:  0s
info: installing component 'rustfmt'
info: default toolchain set to '1.41.0'

  1.41.0 installed - rustc 1.41.0 (5e1a79984 2020-01-27)


Rust is installed now. Great!

To get started you need Cargo's bin directory 
(/home/thales/.asdf/installs/rust/1.41.0/bin) in your PATH
environment variable.

To configure your current shell run 
source /home/thales/.asdf/installs/rust/1.41.0/env
```

After that, I had Rust running and compiling. Show!

## Hello world

Following [Rust's Getting Started guide](https://doc.rust-lang.org/book/ch01-02-hello-world.html), I created a program called main.rs with the tutorial's content. I ran:

```bash
rustc main.rs
./main
```

And then I got the following:

```
Hello, world!
```

Nice. I also played around with the message to see if there would be any issue with UTF-8 characters. There weren't any. 😊

I also added the executable file created to .gitignore. It seemed the right thing to do.

## Cargo project

In order to make this already created project a Cargo project ([following the Getting Started guide](https://doc.rust-lang.org/book/ch01-03-hello-cargo.html)), I ran `cargo new rustInit` and then the contents of the rustInit folder created with that to the project's root.

After running `cargo build`, I got an warning telling me to use snake case instead of came case I've been using so far. Good to know, Rust also prefers snake case. Renamed the project after learning that.

I also searched for a better .gitignore for a Cargo project, since the tutorial didn't mention anything about it.
