
# Nombres

Los objetos en __R__ pueden tener nombres, lo que es útil para la escritura de código legible y objetos auto-descriptivos. A continuación se muestra un ejemplo de asignación de nombres a un vector de enteros.


```r
> x <- 1:3
> names(x)
```

```
NULL
```

```r
> names(x) <- c("España", "Honduras", "El Salvador")
> x
```

```
    España    Honduras El Salvador 
          1           2           3 
```

```r
> names(x)
```

```
[1] "España"     "Honduras"    "El Salvador"
```

