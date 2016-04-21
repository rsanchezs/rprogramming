
# Matrices

Las matrices son vectores con un atributo denominado _dimension_. Este atributo que nos proporciona la dimensión de la matriz es en sí mismo un vector de tipo entero de longitud _2_ (numero de filas, numero de columnas).


```r
> m <- matrix(nrow = 2, ncol = 3)
> m
```

```
     [,1] [,2] [,3]
[1,]   NA   NA   NA
[2,]   NA   NA   NA
```

```r
> dim(m)
```

```
[1] 2 3
```

```r
> attributes(m)
```

```
$dim
[1] 2 3
```

Las matrices se contruyen _"column-wise", esto quiere decir que lo hacen verticalmente, es decir empezando de la esquina superior izquierda y descendiendo hacia abajo por las columnas.


```r
> m <- matrix(1:6, nrow = 2, ncol = 3)
> m
```

```
     [,1] [,2] [,3]
[1,]    1    3    5
[2,]    2    4    6
```

También podemos crear matrices a partir de vectores pasándole el atributo _dimension_.


```r
> m <- 1:10
> m
```

```
 [1]  1  2  3  4  5  6  7  8  9 10
```

```r
> dim(m) <- c(2, 5)
> m
```

```
     [,1] [,2] [,3] [,4] [,5]
[1,]    1    3    5    7    9
[2,]    2    4    6    8   10
```

Las matrices pueden ser creadas rellenando los elementos por columnas ("_column-binding_") o por filas ("_row-binding_") con las funciones _cbind()_ y _rbind()_ respectivamente.


```r
> x <- 1:3
> y <- 10:12
> cbind(x, y)
```

```
     x  y
[1,] 1 10
[2,] 2 11
[3,] 3 12
```

```r
> rbind(x,y)
```

```
  [,1] [,2] [,3]
x    1    2    3
y   10   11   12
```

