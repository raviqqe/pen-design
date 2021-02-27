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
import "github.com/foo/bar"

baz = \() none {
  bar.Bar()
}
```

### Referencing

- A repository name + a module name
  - e.g. `github.com/pen-lang/foo/foo/bar` for a file named `bar.pen` in a `foo` directory in a repository of `github.com/pen-lang/foo`

### Qualification

```
import foo "github.com/pen-lang/foo/foo"

type baz {
  foo foo.Foo
}

blah = \() none {
  foo.Bar()
}
```
