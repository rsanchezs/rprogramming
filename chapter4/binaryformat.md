
# Formatos binarios

El complemento al formato textual es el binario, el cual es necesario en ocasiones por eficiencia, o porque no existe manera de representación en formato textual. También, con datos numéricos, podemos perder precisión cuando los convertimos a un formato textual, es entonces cuando es apropiado utilizar el formato binario.

Las funciones para convertir un objeto __R__ en formato binario son _save()_, _save.image()_ y _serialize()_.


```r
> a <- data.frame(x = rnorm(100), y = runif(100))
> b <- c(3, 4.4, 1/3)
> 
> ##Guardamos a y b en un archivo
> save(a, b, file = "mydata.rda")
> 
> ##Cargamos a y b en el espacio de trabajo
> 
> load("mydata.rda")
```

Si tenemos muchos objetos que queremos guardar en un archivo, podemos guardar todos los objetos del espacio de trabajo con la función _save.image()_:


```r
> ##Guardamos todos los objetos del espacio de trabajo en un archico
> save.image(file = "mydata.RData")
> 
> ##Cargamos todos los objetos del archivo
> load(file = "mydata.RData")
```

Obsérvese que hemos utilizado la extensión _.rda_ con la función _save()_ y la extensión _.RData_ cuando hemos utilizado la función _save.image()_. Esto sólo es una preferencia personal y podemos utilizar cualquier extensión que queramos.Sin embargo, recomiendo el uso de dichas extensiones porque son utilizadas por otros programas.

Por último, la función _serialize()_ se utiliza para convertir objetos __R__ en un formato binario que puede ser transmitido a través de una conexión. Esta podría ser un archivo, pero también podrá ser una conexión de red.

Cuando serializamos un objeto __R__, el resultado será un vector codificado en formato hexadecimal.


```r
> x <- list(1, 2, 3)
> serialize(x, NULL)
```

```
 [1] 58 0a 00 00 00 02 00 03 03 00 00 02 03 00 00 00 00 13 00 00 00 03 00
[24] 00 00 0e 00 00 00 01 3f f0 00 00 00 00 00 00 00 00 00 0e 00 00 00 01
[47] 40 00 00 00 00 00 00 00 00 00 00 0e 00 00 00 01 40 08 00 00 00 00 00
[70] 00
```

Si lo deseas puedes gravar el resultado en un archivo, sin embargo recomiendo utilizar los métodos anteriores (ej. _save_()).

El beneficio de _serialize()_ es que es el único modo de representar un objeto __R__ en un formato exportable, sin perder precisión ni metadatos.
