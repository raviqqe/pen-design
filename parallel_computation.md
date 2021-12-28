# Parallel computation

## Operations

### Spawn

- `\() T -> \() T`

```pen
ctx ~ \() number { 42 }
```

### Map

- `[T] -> [T]`

```pen
ctx ~~ [number 42]
```

### Split

- `[T] -> [[T]]`

```pen
ctx ~< [number 42]
```

### Join

- `[[T]] -> [T]`

```pen
ctx ~> [[number] [number 42], [number 42]]
```
