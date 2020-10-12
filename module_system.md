# Module system

## Exporting variables and types

```
record Foo {
  ...
}
```

```
enum Foo {
  Bar
  ...
}
```

```
func Foo() {
  ...
}
```

## Importing modules

```
import "github.com/pen-lang/foo/foo"

func bar() {
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

func blah() {
  foo.Bar()
}
```
