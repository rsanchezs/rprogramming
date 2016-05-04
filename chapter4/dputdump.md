
# Uso de dput() y dump()

Ver el video de esta sección:

{%youtube%}5mIPigbNDfk{%endyoutube%}

A continuación mostrarnos un ejemplo del uso de la función _dput()_ y _dget()_:


```r
> ##Crea un data frame
> y <- data.frame(a = 1, b = "a")
> ##Print 'dput' en la consola
> dput(y)
```

```
structure(list(a = 1, b = structure(1L, .Label = "a", class = "factor")), .Names = c("a", 
"b"), row.names = c(NA, -1L), class = "data.frame")
```

Obsérvese que la salida de _dput()_ es en la forma de código __R__ y muestra metadatos como la clase del objeto, el nombre de las filas, y el nombre de las columnas.

Podemos gravar en un archivo la información proporcionada por _dput()_:


```r
> ## Grava la salida de 'dput' a un archivo
> dput(y, file ="y.R")
> 
> ##Leemos los datos desde el archivo
> new.y <- dget("y.R")
> new.y
```

```
  a b
1 1 a
```

También podemos gravar múltiples objetos de una sola vez utilizando la función _dump()_. Pasaremos como argumento a la función un vector de caracteres con sus nombres.


```r
> x <- "foo"
> y <- data.frame(a = 1L, b = "a")
> 
> dump(c("x", "y"), file = "data.R")
> rm(x, y)
```
 La función inversa de _dump()_ es _source()_:
 
 
 

```r
> source(file = "data.R")
> str(y) ##con la función 'str' consultamos la estructura del objeto
```

```
'data.frame':	1 obs. of  2 variables:
 $ a: int 1
 $ b: Factor w/ 1 level "a": 1
```

```r
> x
```

```
[1] "foo"
```


