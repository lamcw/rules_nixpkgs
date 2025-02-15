Rust Toolchain Example
======================

This is an example Rust project that uses `rules_rust`.

If the Nix package manager is present in the build environment, this example will use Nix to provide the Rust toolchain. Otherwise, it will use the toolchain provided by `rules_rust` and not rely on Nix at all.

# Usage

To run the example with Nix, issue the following command:
```
nix-shell --command 'bazel run --config=nix :hello'
```

To run the example without Nix, make sure you have Bazel installed, and issue the following command:
```
bazel run :hello
```
This non-Nix example will download a binary distribution of Rust's toolchain from the Internet.
