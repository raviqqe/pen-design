# Effect system

- Impure functions are injected only as arguments to functions.

## Effects

- I/O
  - File system
  - Network
  - Clock
- Parameters
  - Command-line arguments
  - Environment variables
- Parallelism / Concurrency
  - Parallel evaluation
  - Concurrent queues

## Main functions

```
lambda main(os Os) ! {
  ...
}
```

### OS type

```
record Os {
  arguments: []string
  environmentVariables: []string

  openFile: lambda(string, FileMode) !File
  readFile: lambda(File) !string
  writeFile: lambda(File, string) !
  ...
}
```
