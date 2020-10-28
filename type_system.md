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

### Streams

```
<a>
```

#### Operations

```
<>
x << func() <a> {
  return ...
}
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

### Lambda expression

```
\(x boolean, y number) string {
  return "hello"
}
```

## Statements

### Variable definition

- Variables of the same names in functions are overwritten.

```
foo = ...
```

### If statement

```
if x {
  ...
} else if y {
  ...
} else {
  ...
}
```

### Switch statement

- For union and any types

```
switch x = y {
case number
  ...
case string
  ...
default
  ...
}
```

### For statement

#### Conditional

```
for x {
  ...
}
```

#### Iterative

```
for x in xs {
  ...
}
```

#### Local exit

```
continue
break
```

### Type alias

```
type foo = bar
```
