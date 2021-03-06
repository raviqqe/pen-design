# Design decisions

## Single `number` type

### Pros

- Simple

### Cons

- Slower than integers
  - We can optimize it later using NaN boxing.
- Less type-safe for integers
  - If we use wrapped operations for them, it may even safer to use real numbers.

## Inductive definitions of low-level values

### Pros

- No cyclic reference
  - Reference counting can be used for GC.
