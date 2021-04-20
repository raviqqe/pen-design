# Type system

- Nominal typing
- Restricted polymorphism
- Unidirectional type inference

## Primitives

```
boolean
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
<a>
```

## Maps

- Keys cannot be functions, `any` or any other types including them.

```
{a: b}
```

## Records

```
record person {
  name string
  age  number
}
```

## Variants

```
variant foo {
  bar(bar)
  baz
}
```

## Options

```
a?
```

## Any

- The top type

```
any
```

## Never

- The bottom type

```
never
```

## Error

```
record error {
  cause any
}
```
