# Design decisions

## Single `number` type

### Pros

- Simple

### Cons

- Slow compared to integers
  - We can optimize it later using NaN boxing.
- Degraded type safety for integer values
  - If we use wrapped operations for them, it may even safer to use real numbers.

## Inductive definitions of low-level values

### Pros

- No cyclic reference
  - Reference counting can be used for GC.
