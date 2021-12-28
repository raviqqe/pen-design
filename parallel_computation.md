# Parallel computation

## Operations

### Spawn

- Semantics: `\() T -> \() T`
- Implemented as `\(\() any) \() any`

```pen
ctx ~ \() number { 42 }
```

### Map

- Semantics: `[T] -> [T]`
- Implemented as `\([any]) [any]`

```pen
ctx ~~ [number 42]
```

### Join

- Semantics: `[[T]] -> [T]`
- It represents the "race" operation too.

```pen
ctx ~> [[number] [number 42], [number 42]]
```
