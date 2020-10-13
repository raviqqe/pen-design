# Module system

## Export

- Capitalize the first letters.

```
record Foo {
  ...
}
```

```
union Foo {
  Bar
  ...
}
```

```
Foo = ...
```

## Import

```
import "github.com/pen-lang/foo/foo"

lambda bar() {
  Foo()
}
```

### Referencing

- A repository name + a module name
  - e.g. `github.com/pen-lang/foo/foo/bar` for a file named `bar.pen` in a `foo` directory in a repository of `github.com/pen-lang/foo`

### Qualification

```
import foo "github.com/pen-lang/foo/foo"

record baz {
  foo: foo.Foo
}

lambda blah() {
  foo.Bar()
}
```
