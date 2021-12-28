# Parallel computation

## Functions

```
Map \(Parallel) Map
Race \(Parallel) Race
Split \(Parallel) Split
Join \(Parallel) Join
```

## Operations

### `\() T -> \() T`

```pen
ctx ~ \() number { 42 }
```

### `[T] -> [T]`

- `Map`
- `Race`
  - Equivalent to `Split` and `Join`

```pen
ctx ~~ [number 42]
```

### `[T] -> [[T]]`

- `Split`

```pen
ctx ~< [number 42]
```

### `[[T]] -> [T]`

- `Join`

```pen
ctx ~> [number 42]
```
