# Type system

- Nominal typing
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

### Arrays

```
[a]
```

#### Operations

```
[1, 2, 3]
[...xs, x]
xs[0]
```

### Maps

- Keys are number or string types.

```
{a: b}
```

#### Operations

```
{"foo": "bar"}
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
person{name: "foo", age: 42}
person{...p, name: "bar"}
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

- For union and any types

```
switch x = y {
number:
  ...
string:
  ...
_:
  ...
}
```

## Statements

### Variable definition

- Variables of the same names in functions are overwritten.

```
foo = ...
```

### Type alias

```
type foo = bar
```
