# Parallel computation

## Parallel type

```
Parallel.Parallel
```

## `~` operator

### Map

```
xs ~ Parallel.Map(prl, concurrency) # <...>
```

### Race

```
xs ~ Parallel.Race(prl, concurrency) # <...>
```

### Split

> WIP

```
xs ~ Parallel.Split(prl, concurrency) # <<...>>
```
