# Package system

## Package configuration files

### Application

```json
{
  "application": {
    "name": "foo",
    "system": {
      "name": "github.com/ein-lang/os",
      "version": "main"
    }
  },
  "dependencies": {
    "github.com/foo/bar": { "version": "main" }
  }
}
```

### Library

```json
{
  "dependencies": {
    "github.com/foo/bar": { "version": "main" }
  }
}
```
