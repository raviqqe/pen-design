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

#### Literals

```
false
true
none
-12.3
"string"
```

### Functions

```
\(a, b) c
```

### Lists

- Generic
- Lazy

```
[a]
```

#### Operations

```
[1, 2, 3]
[x, ...xs]
```

### Maps

- Keys are number or string types.

```
{a: b}
```

#### Operations

```
{"foo": "bar"}
{...xs, "foo": "bar"}
xs["foo"]
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

#### Operations

```
p.name
person{name "foo", age 42}
person{...p, name "bar"}
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

#### `?` operator

- For `... | error` types

```
x?
```

## Expressions

### Lambda

```
\(x boolean, y number) string {
  "hello"
}
```

### `if` `else`

```
if x {
  ...
} else if y {
  ...
} else {
  ...
}
```

### `switch`

#### Union and any types

```
switch x = y {
  number {
    ...
  }
  string | none {
    ...
  }
  _ {
    ...
  }
}
```

#### List types

```
switch xs {
  [] {
    ...
  }
  [y, ...ys] {
    ...
  }
}
```

## Statements

### Variable binding

```
foo = ...
```

### Type alias

```
type foo = bar
```
