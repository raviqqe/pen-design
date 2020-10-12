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
enum error {
  error(any)
}
```

### Functions

```
func(a, b) c
```

### Lists

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

#### Implementation

```
enum option<a> {
  some(a)
  none(none)
}
```

### Results

```
!person
```

#### Implementation

```
enum result<a> {
  ok(a)
  error(error)
}
```

## Statements

### Function definition

```
func foo(x bool, y number) string {
  return "hello"
}
```

### Variable definitions

```
foo = 42
```

## Expressions

### If expressions

```
if true {
  ...
} else if false {
  ...
} else {
  ...
}
```

#### Enum type matching

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

#### Any type matching

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

### For loop

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
