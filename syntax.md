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
xs[42] # ... | error
```

### Streams

```
<<>>
<<x, ...xs>>
```

### Maps

```
{"foo": "bar"}
{...xs, "foo": "bar"}
xs["foo"] # ... | error
```

### Records

```
x.name
person{name: "foo", age: 42}
person{...x, name: "foo"}
```

### Error handling

- For `... | error` types

```
x?
```

### Conditionals

#### Booleans

```
if x {
  ...
} else if y {
  ...
} else {
  ...
}
```

#### Unions and `any`

```
x = ...

if x as number {
  ...
} else if string | none {
  ...
} else {
  ...
}
```

#### Streams

```
if <<x, ...xs>> = xs {
  ...
} else {
  ...
}
```
