
# Selección de elementos en una matriz

Para la selección de elementos en una matriz podemos utilizar la nomenclatura {% math %}(i, j){% endmath %}


```r
> x <- matrix(1:6, 2, 3)
> x
```

```
     [,1] [,2] [,3]
[1,]    1    3    5
[2,]    2    4    6
```

```r
> x[1, 2]
```

```
[1] 3
```

```r
> x[2, 1]
```

```
[1] 2
```

Podemos acceder a filas o columnas del siguiente modo.


```r
> ## Selecciona la primera fila
> x[1,]
```

```
[1] 1 3 5
```

```r
> ## Selecciona la segunda columna
> x[, 2]
```

```
[1] 3 4
```



