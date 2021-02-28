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

## Arrays

```
[a]
```

## Streams

```
<<a>>
```

## Maps

- Keys are subtypes of `boolean | none | number | string`.

```
{a: b}
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
