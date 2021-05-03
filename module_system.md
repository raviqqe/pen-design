# Module system

## Export

Capitalize names.

```
Foo = ...
```

## Import

```
import foo.Foo

x = Foo.Foo
```

### Local modules

```
import .Foo.Bar
```

### Custom prefix

```
import foo.Foo as Bar

x = Bar.Foo
```

### Module reference

- A package name and a module path
  - e.g. `foo.Bar.Baz` for a `Baz.pen` file in a `Bar` directory in a `foo` package
