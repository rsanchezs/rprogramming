
# Coerción explícita

El mecanismo de _coercion_ puede ser hecho de forma explícita con la función _as.*_ si es posible.


```r
> x <- 0:6
> class(x)
```

```
[1] "integer"
```

```r
> as.numeric(x)
```

```
[1] 0 1 2 3 4 5 6
```

```r
> as.logical(x)
```

```
[1] FALSE  TRUE  TRUE  TRUE  TRUE  TRUE  TRUE
```

```r
> as.character(x)
```

```
[1] "0" "1" "2" "3" "4" "5" "6"
```

En ocasiones esto no es posible y __R__ nos devolverá un objeto __NAs__.


```r
> x <- c("a","b", "c")
> as.numeric(x)
```

```
Warning: NAs introduced by coercion
```

```
[1] NA NA NA
```

```r
> as.logical(x)
```

```
[1] NA NA NA
```

```r
> as.complex(x)
```

```
Warning: NAs introduced by coercion
```

```
[1] NA NA NA
```
Cuándo esto suceda __R__ nos avisará con un mensaje de tipo _warning_.
