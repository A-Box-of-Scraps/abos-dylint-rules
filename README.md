# dylint-rules

Custom dylint lint rules shared across A Box of Scraps Rust projects.

## Installation

Install Dylint and its linker:

```sh
cargo install cargo-dylint dylint-link --locked
```

Add the following to your project's workspace-root `Cargo.toml`:

```toml
[[workspace.metadata.dylint.libraries]]
git = "https://github.com/A-Box-of-Scraps/abos-dylint-rules"
rev = "<rev-hash>"
pattern = "explicit_binding_types" # "file_length"; "tests_outside_src";
```

Replace `<rev-hash>` with the full commit hash you want to use. Pinning a revision keeps the rules reproducible.

To enable all three rules, replace `pattern` with:

```toml
pattern = ["explicit_binding_types", "file_length", "tests_outside_src"]
```

Run the configured rules from your project:

```sh
cargo dylint --all
```

## Rules

### [explicit_binding_types](explicit_binding_types/README.md)

Requires type annotations on simple `let` and `let mut` bindings whose initializer does not show the type.

### [file_length](file_length/README.md)

Warns when a physical Rust source file exceeds 600 lines.

### [tests_outside_src](tests_outside_src/README.md)

Requires test implementations outside each package's `src/` directory.

## License

Licensed under the [MIT License](LICENSE) by A Box of Scraps.
