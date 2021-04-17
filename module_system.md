# Module system

## Export

Capitalize names.

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

x = Foo.Bar
```

### Custom prefix

```
import Bar "github.com/foo/foo/Foo"

x = Bar.Foo
```

### Prefix shorthand

```
import "github.com/foo/foo/Foo"

x = Foo.Foo
```

is equivalent to

```
import "github.com/foo/foo/Foo"

x = Foo
```

### Module reference

- A repository name + a file basename
  - e.g. `github.com/foo/bar/Baz` for a `Baz.pen` file in a `github.com/foo/bar` repository
