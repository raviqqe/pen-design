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
Arguments \(Os) [string]
EnvironmentVariables \(Os) [string]

OpenFile \(Os, string, FileMode) File | error
ReadFile \(Os, File) string | error
WriteFile \(Os, File, string) none | error

...
```
