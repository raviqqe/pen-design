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
func main(os Os) ! {
  ...
}
```

### OS type

```
struct Os {
  arguments: []string,
  environmentVariables: []string,

  openFile: func(string, FileMode) !File
  readFile: func(File) !string
  writeFile: func(File, string) !
  ...
}
```
