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
  - e.g. `github.com/pen-lang/foo/foo/bar` for a file named `bar.pen` in a `foo` directory in a repository of `github.com/pen-lang/foo`

### Custom prefixes

```
import bar "github.com/foo/foo"

x = bar.Foo()
```
