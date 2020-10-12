# Type system

- Nominal typing
- No polymorphism
- Bidirectional type inference

## Types

### Primitives

```
boolean
number
string
```

#### Literals

```
false
true
-12.3
"string"
```

### Functions

```
(a, b) c
```

### Lists

```
[]a
```

#### Literals

```
[1, 2, 3]
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
enum maybePerson {
  some(person)
  none
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
foo(x boolean, y number) string {
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

#### Enum matching

```
if enum some(p) = x {
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
