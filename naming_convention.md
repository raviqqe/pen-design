# Naming convention

- Acronyms are considered as single words.
  - `Cpu`
  - `Ast`

## Variables and types

- Lower or upper camel case
  - `fooBar`
  - `FooBar`
- Local names can be extra short [like in Go](https://github.com/golang/go/wiki/CodeReviewComments#variable-names).
  - `i` for `index`
  - `c` for `requestCount`

## Modules

- Snake case
  - `foo_bar`

## Module directories

- Lower case without signs
  - `foo_bar`
- Follow [Go's convention](https://blog.golang.org/package-names).

## Packages

- Kebab case
  - `github.com/foo-bar/baz-blah`
