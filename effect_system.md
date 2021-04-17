# Effect system

- Side effects are injected only as arguments to functions.

## Effects

- I/O
  - File system
  - Network
  - Clock
  - Random
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
  Arguments [string]
  EnvironmentVariables [string]

  OpenFile \(string, FileMode) File | error
  ReadFile \(File) string | error
  WriteFile \(File, string) none | error
  ...
}
```
