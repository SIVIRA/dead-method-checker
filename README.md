# dead-method-checker

Find unused methods in Go structs.

## Installation

```bash
go install github.com/SIVIRA/dead-method-checker@latest
```

## Usage

**Important**: Run this command from the top directory of your target project (where `go.mod` is located).

```bash
dead-method-checker --pkg <package-path> --struct <struct-name>
```

### Options

- `--pkg` (required): Path of the package to check for unused methods
- `--struct` (required): Name of the struct to check for unused methods
- `--ignore`: Methods to ignore check (comma-separated)
- `--fail`: Exit with non-zero status if unused methods are found

### Examples

Check for unused methods in a struct:

```bash
dead-method-checker --pkg github.com/example/mypackage --struct MyStruct
```

Ignore specific methods:

```bash
dead-method-checker --pkg github.com/example/mypackage --struct MyStruct --ignore String,GoString
```

Exit with error code if unused methods are found:

```bash
dead-method-checker --pkg github.com/example/mypackage --struct MyStruct --fail
```
