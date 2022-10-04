Globetter
=========

This is a minimal fork of the [Glob crate](https://crates.io/crates/glob).
As of 2022-10-04, its last release was 2019-03-07, and there are some outstanding defects.
This fork is intended as a drop-in replacement for bug fixes,
detailed in the [changelog](CHANGELOG.md) and [releases page](https://github.com/mtkennerly/globetter/releases).

Support for matching file paths against Unix shell style patterns.

[![Build Status](https://dev.azure.com/rust-lang/glob/_apis/build/status/rust-lang-nursery.glob?branchName=master)](https://dev.azure.com/rust-lang/glob/_build/latest?definitionId=20&branchName=master)

[Documentation](https://docs.rs/glob)

## Usage

To use `globetter`, add it to your project by running `cargo add globetter`.

## Examples

Print all jpg files in /media/ and all of its subdirectories.

```rust
use globetter::glob;

for entry in glob("/media/**/*.jpg").expect("Failed to read glob pattern") {
    match entry {
        Ok(path) => println!("{:?}", path.display()),
        Err(e) => println!("{:?}", e),
    }
}
```
