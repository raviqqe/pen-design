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
... |> f(x, y, _)
```

is equivalent to

```
f(x, y, ...)
```

## Functions

### Collections

```
delete : \(map, key) map
size : \(array) number
size : \(map) number
iterate : \(array) <element>
iterate : \(map) <key>
```

### Others

```
debug : \(any) none
error : \(any) error
```
