# dylint-rules

Custom dylint lint rules shared across A Box of Scraps Rust projects.

## Rules

### [explicit_binding_types](explicit_binding_types/README.md)

Requires type annotations on simple `let` and `let mut` bindings whose initializer does not show the type.

### [file_length](file_length/README.md)

Warns when a physical Rust source file exceeds 600 lines.

### [tests_outside_src](tests_outside_src/README.md)

Requires test implementations outside each package's `src/` directory.

## License

Licensed under the [MIT License](LICENSE) by A Box of Scraps.
