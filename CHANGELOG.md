## Unreleased

* Initial release.
* Fixed:
  * `glob_with` did not respect the case sensitivity option for path segments without any wildcard characters.
    For example, the pattern `src/*.rs` would find `SRC/main.rs` even if you turned case sensitivity on.
    ([ticket](https://github.com/rust-lang/glob/issues/61))
