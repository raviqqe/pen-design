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

```
size : \(string | array | map) number
```

### Maps

```
delete : \(map, string) map
include : \(map, string) boolean
```

### Others

```
debug : \(any) none
error : \(any) error
```
