# Type system

- Nominal typing
- No polymorphism
- Bidirectional type inference

## Types

### Primitives

```
bool
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

### Any

- The top type

```
any
```

### Error

```
struct error {
  source: any
}
```

### Functions

```
func(a, b) c
```

### Arrays

- Lazy?

```
[]a
```

#### Literals

```
[1, 2, 3]
[x, ...xs]
```

### Struct types

- Elements are private outside modules.

```
struct person {
  name string
  age  number
}
```

#### Operations

```
p.name
person{ name: "foo", age: 42 }
person{ ...p, name: "bar" }
```

### Unions

```
enum foo {
  foo(bar)
  baz
}
```

### Options

```
?person
```

### Results

```
!person
```

## Statements

### Function definition

```
func foo(x bool, y number) string {
  return "hello"
}
```

### Variable definitions

- Variables of the same names in functions are overwritten.

```
foo = 42
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

#### Enum matching

```
switch x {
case foo(x)
  ...
case bar(x)
  ...
default
  ...
}
```

#### Type matching

- For any, option and result types

```
switch type x {
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
for true {
  ...
}
```

#### Iterative

```
for x in xs {
  ...
}
```
