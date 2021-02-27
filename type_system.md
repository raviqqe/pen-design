# Type system

- Nominal typing
- Subtyping
  - No covariance or contravariance
- Restricted polymorphism
- Bidirectional type inference

## Primitives

```
boolean
none
number
string
```

## Functions

```
\(a, b) c
```

## Lists

- Lazy

```
[a]
```

## Maps

- Keys are number or string types.

```
{a: b}
```

## Record types

```
type person {
  name string
  age  number
}
```

### Without fields

```
type foo
```

## Union types

```
foo | bar
```

## Any

- The top type

```
any
```

## Error

```
type error {
  source any
}
```
