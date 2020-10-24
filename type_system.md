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

#### Literals

```
[1, 2, 3]
[...xs, x]
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
  source: any
}
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
if true {
  ...
} else if false {
  ...
} else {
  ...
}
```

### Switch statement

- For union and any types

```
switch x {
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

### Type alias

```
type foo = bar
```
