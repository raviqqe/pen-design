# Type system

- Nominal typing
- Subtyping
- Restricted polymorphism
- Bidirectional type inference

## Types

### Primitives

```
boolean
none
number
string
```

### Functions

```
\(a, b) c
```

### Lists

- Lazy

```
[a]
```

### Maps

- Keys are number or string types.

```
{a: b}
```

### User-defined types

```
type person {
  name string
  age  number
}
```

#### Without fields

```
type foo
```

### Union types

```
foo | bar
```

### Any

- The top type

```
any
```

### Error

```
type error {
  source any
}
```
