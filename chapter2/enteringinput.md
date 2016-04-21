
#Primeros pasos con R

##Introducción de datos

En el _prompt_ de __R__ escribiremos las expresiones. El símbolo __<-__ és el operador de asignación.


```r
> x <- 1
> print(x)
```

```
[1] 1
```

```r
> x
```

```
[1] 1
```

```r
> msg <- "hello"
> print(msg)
```

```
[1] "hello"
```

La gramática del lenguaje determina si una expresión es completa o no.Por ejemplo:

```
x <-     ## Expresión incompleta
```

El carácter __#__ indica que es un comentario. Cualquier cosa escrita a la derecha del mismo será ignorado. Este és el único tipo de comentario en __R__. A diferéncia de otros lenguajes __R__ no soporta los comentarios multilínia y por bloques.
