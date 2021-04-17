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
import "github.com/foo/foo/Foo"

x = Foo.Foo
```

### Prefix omission

Prefixes can be omitted if their names are the same as exported names.

```
import "github.com/foo/foo/Foo"

x = Foo
```

### Referencing

- A repository name + a file basename
  - e.g. `github.com/foo/bar/Baz` for a `Baz.pen` file in a `github.com/foo/bar` repository

### Custom prefixes

```
import Bar "github.com/foo/foo/Foo"

x = Bar.Foo
```
