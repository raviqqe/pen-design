# Type system

- Nominal typing
- Subtyping
  - No covariance or contravariance
- Restricted polymorphism
- Unidirectional type inference

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

```
[a]
```

## Records

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

## Unions

```
foo | bar
```

## Any

The top type

```
any
```

## Error

```
type error {
  cause any
}
```
