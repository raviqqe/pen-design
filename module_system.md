# Module system

## Export

- Capitalize names.

```
Foo = ...
```

```
type Foo {
  Bar number
  ...
}
```

## Import

```
import "github.com/foo/foo"

x = foo.Foo
```

### Referencing

- A repository name + a module name
  - e.g. `github.com/foo/bar/baz` for a `baz` directory in a `github.com/foo/bar` repository

### Custom prefixes

```
import bar "github.com/foo/foo"

x = bar.Foo()
```
