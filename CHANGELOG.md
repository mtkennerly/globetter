## v0.1.1 (2022-10-07)

* Avoided `canonicalize` call during case-insensitive matching on Windows/Mac.
  If you want the returned path to match the real capitalization on theses OSes,
  turn on case-sensitive matching or canonicalize it separately.
  ([ticket](https://github.com/rust-lang/glob/issues/61))
* Avoided unnecessary system calls to determine whether a path is a directory.
  ([ticket](https://github.com/rust-lang/glob/issues/79))

## v0.1.0 (2022-10-04)

* Initial release, forked from Glob v0.3.0 plus the latest additions on GitHub
  as of commit 91248c13bafe4520010503f8b4d1d9e037515268.
* Fixed:
  * `glob_with` did not respect the case sensitivity option for path segments without any wildcard characters.
    For example, the pattern `src/*.rs` would find `SRC/main.rs` even if you turned case sensitivity on.
    ([ticket](https://github.com/rust-lang/glob/issues/61))
