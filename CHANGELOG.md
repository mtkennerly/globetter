## v0.1.0 (2022-10-04)

* Initial release, forked from Glob v0.3.0 plus the latest additions on GitHub
  as of commit 91248c13bafe4520010503f8b4d1d9e037515268.
* Fixed:
  * `glob_with` did not respect the case sensitivity option for path segments without any wildcard characters.
    For example, the pattern `src/*.rs` would find `SRC/main.rs` even if you turned case sensitivity on.
    ([ticket](https://github.com/rust-lang/glob/issues/61))
