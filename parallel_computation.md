# Parallel computation

## Parallel type

```
type Parallel {
  Map : \(number) Map
  Race : \(number) Race
  Split : \(number) Split
  ...
}
```

## `~` operator

```
xs ~ parallel.Map(concurrency)
```
