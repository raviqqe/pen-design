# Parallel computation

## Requirements

It can represent the following kinds of parallel computation.

- Map
- Race
- Join
- Split
  - Might not be necessary with sophisticated runtime

## Operations

### Spawn

- Semantics: `\() T -> \() T`
- Implemented as `\(\() any) \() any`

```pen
f = go \() number { 42 }
```

### Join

- Semantics: `[[T]] -> [T]`
- Implemented as `\([[any]]) [any]`

```pen
xs = go [[number] [number 42], [number 42]]
```
