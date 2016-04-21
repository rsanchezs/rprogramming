
# Evaluación

Cuando un expresión correcta es introducida en la consola, esta es evaluada y el resultado de la expresión es devuelto. El resultado puede ser _auto-printed_:


```r
> x <- 5 ## No se imprime en pantalla
> x ## por auto-printing se imprime en pantalla
```

```
[1] 5
```

```r
> print(x) ## impresión explícita
```

```
[1] 5
```

En [1] se muestra que _x_ es un vector y que su primer elemento es _5_.

Tipicamente con un trabajo interactivo, nosotros no imprimeros los objetos de forma explícita ya que es mucho más cómodo sólo escribir el nombre del objeto y presionar la tecla __Enter__. Sin embargo, cuándo escribamos scripts, funciones o programas muchos más largos, nos veremos con la necesidad de imprimir objetos y es entonce cuándo utilizaremos el modo explícito, ya que el modo ímplicito no trabaja en esas circunstáncias.

Cuándo un vector __R__ es mostrado en la consola obsérvese que el índice del vector es mostrado en []. Por ejemplo:


```r
> x <- 10:30
> x
```

```
 [1] 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30
```

Los números entre corchetes no forman parte del vector en sí mismo, sino que se trata únicamente de información para la impresión por pantalla.

En __R__ es de vital importáncia entender la diferéncia que existe en el objeto __R__ y la manera en que estos objetos son mostrados en la consola. Normalmente, la información en la consola puede tener información adicional para hacerla más agradable al usuario.

> __Nota:__ El operador __:__ es utilizado para crear secuencias de enteros.
