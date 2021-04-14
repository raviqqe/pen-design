# Built-ins

## Operators

### Arithmetic

```
1 + 1
1 - 1
1 * 1
1 / 1
```

### Comparison

```
1 == 1
1 /= 1
1 < 1
1 > 1
1 <= 1
1 >= 1
```

### Boolean

```
true & true
true | true
not(true)
```

### Pipe

```
... |> f(x, y)
```

is equivalent to:

```
f(x, y, ...)
```

## Functions

### Collections

- Collections include strings, arrays and maps.
- Key types depend on collection types.
  - Number for strings and arrays
  - Non-function type for maps

```
delete : \(collection, key) map
size : \(collection) number
```

### Maps

```
include : \(map, key) boolean
```

### Others

```
debug : \(any) none
error : \(any) error
```
