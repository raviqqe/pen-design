# Syntax

## Statements

### Variable binding

```
foo = ...
```

### Type alias

```
type foo = ...
```

### Module import and export

- See [the module system](module_system.md).

## Expressions

### Primitives

```
false
true
none
-12.3
"string"
```

### Functions

#### Calls

```
f(x, y)
```

#### Abstraction

```
\(x boolean, y number) string {
  ...
}
```

### Lists

```
[1, 2, 3]
[x, ...xs]
```

### Maps

```
{"foo": "bar"}
{...xs, "foo": "bar"}
xs["foo"]
```

### User-defined types

```
x.name
person{name "foo", age 42}
person{...x, name "foo"}
```

### Error handling

#### `?` operator

- For `... | error` types

```
x?
```

### Conditionals

#### `if`

```
if x {
  ...
} else if y {
  ...
} else {
  ...
}
```

#### `switch`

##### Union and any types

```
switch x = y {
number:
  ...
string | none:
  ...
_:
  ...
}
```

##### List types

```
switch xs {
[]:
  ...
[y, ...ys]:
  ...
}
```
