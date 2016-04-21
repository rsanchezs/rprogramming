
# Listas

Las listas son un tipo especial de vector que pueden contener objetos de diferentes clases. Las listas son una estructura de datos muy importante y ampliamente utilizada, es por eso que tendríamos que estudiarlas y conocerlas profundamente. Las listas junto con un conjunto de funciones que trataremos más adelante constituyen una herramienta poderosa para el desarrollo de nuestro trabajo.

Las listas pueden ser creadas explícitamente con la función _list()_, la cual puede tomar un número arbitrario de argumentos.


```r
> x <- list(1, "a", TRUE, 1 + 4i)
> x
```

```
[[1]]
[1] 1

[[2]]
[1] "a"

[[3]]
[1] TRUE

[[4]]
[1] 1+4i
```

También podemos crear una lista vacía con una longitud preestablecida mediante la función _vector()_.


```r
> x <- vector("list", length = 5)
> x
```

```
[[1]]
NULL

[[2]]
NULL

[[3]]
NULL

[[4]]
NULL

[[5]]
NULL
```

