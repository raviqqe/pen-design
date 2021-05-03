# Module system

## Export

Capitalize names.

```
Foo = ...
```

## Import

```
import Foo.Foo

x = Foo.Foo
```

### Local modules

```
import .Foo.Bar
```

### Custom prefix

```
import Foo.Foo as Bar

x = Bar.Foo
```

### Module reference

- A package name and a module path
  - e.g. `Foo.Bar.Baz` for a `Baz.pen` file in a `Bar` directory in a `Foo` package
