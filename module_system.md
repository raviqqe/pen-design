# Module system

## Export

Capitalize names.

```
Foo = ...
```

## Import

```
import "github.com/foo/foo/Foo"

x = Foo.Foo
```

### Local modules

```
import "/Foo/Bar"
```

### Custom prefix

```
import Bar "github.com/foo/foo/Foo"

x = Bar.Foo
```

### Module reference

- A repository name + a file basename
  - e.g. `github.com/foo/bar/Baz` for a `Baz.pen` file in a `github.com/foo/bar` repository
