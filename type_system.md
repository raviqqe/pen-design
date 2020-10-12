# Type system

- Nominal typing
- No polymorphism
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

### Any

- The top type

```
any
```

### Error

```
record error {
  source: any
}
```

### Functions

```
func(a, b) c
```

### Arrays

```
[]a
```

#### Literals

```
[1, 2, 3]
[x, ...xs]
```

### Record types

- Elements are private outside modules.

```
record person {
  name string
  age  number
}
```

#### Operations

```
p.name
person{name: "foo", age: 42}
person{...p, name: "bar"}
```

### Union types

```
union foo {
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

## Expressions

### Lambda expression

```
lambda(x boolean, y number) string {
  return "hello"
}
```

## Statements

### Variable definition

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

#### Union matching

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
