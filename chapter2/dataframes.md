
# Data frames

Los _data frames_ son utilizados en __R__ para almacenar datos de tipo tabla. Es un tipo de objeto muy importante en __R__ y utilizados ampliamente en modelado estadístico. El paquete _dplyr_ de Hadley Wickham posee un conjunto optimizado de funciones diseñadas para trabajar eficientemente con data frames.

Los data frames son representados como un tipo especial de lista donde cada elemento de la lista tiene que tener la misma longitud. Podemos considerar cada elemento de la lista como una columna y la longitud de cada elemento de la lista como el número de filas.

A diferencia de las matrices, los data frames pueden almacenar diferentes clases de objetos en cada columna. Recordemos que los matrices debían tener cada elemento de la misma clase (e.g. todos enteros o todos numericos).

Además del nombre de las columnas, que nos indica el nombre de las variables, los data frames tienen un atributo especial denominado _row.names_ que nos indica la información de cada fila en el data frame.

Los data frames normalmente son creados leyendo desde un conjunto de datos con las funcions _read.table()_ o _read.csv()_. Sin embargo, data frames pueden ser creados explícitamente con la función _data.frame()_ o pueden ser _"coerced"_ desde otro tipo de objetos como las listas.

Los data frames pueden ser convertidos a matrices con la función _data.matrix()_. 


```r
> x <- data.frame(foo = 1:4 , bar = c(T,T,F,F))
> x
```

```
  foo   bar
1   1  TRUE
2   2  TRUE
3   3 FALSE
4   4 FALSE
```

```r
> nrow(x)
```

```
[1] 4
```

```r
> ncol(x)
```

```
[1] 2
```

