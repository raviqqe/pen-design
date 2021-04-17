# Parallel computation

## Parallel type

```
type Parallel {
  Map : \(number) MapContext
  Race : \(number) RaceContext
  Split : \(number) SplitContext
}
```

## `~` operator

```
xs ~ parallel.Map(concurrency)
```
