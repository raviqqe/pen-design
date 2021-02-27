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
main = \(os Os) none | error {
  ...
}
```

### OS type

```
type Os {
  arguments [string]
  environmentVariables [string]

  openFile \(string, FileMode) File | error
  readFile \(File) string | error
  writeFile \(File, string) none | error
  ...
}
```
