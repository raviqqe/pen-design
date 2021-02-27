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
  - e.g. `github.com/foo/foo/bar` for a `bar` directory in a `github.com/pen-lang/foo` repository

### Custom prefixes

```
import bar "github.com/foo/foo"

x = bar.Foo()
```
