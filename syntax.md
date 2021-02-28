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

### Record type definitions

See [Type system](type_system.md#records).

### Module import and export

See [Module system](module_system.md).

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

### Arrays

```
[1, 2, 3]
[x, ...xs]
xs[42] # element | error
```

### Maps

```
{"foo": "bar"}
{...xs, "foo": "bar"}
xs["foo"] # value | error
```

### Records

```
x.name
person{name: "foo", age: 42}
person{...x, name: "foo"}
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
switch x = ... {
number:
  ...
string | none:
  ...
_:
  ...
}
```

##### Stream types

```
switch xs {
[]:
  ...
[y, ...ys]:
  ...
}
```
