
# Mezclando objetos

Existen ocasiones en las que nos encontramos diferentes clases de objetos __R__ mezclados. Algunas veces esto sucede por accidente pero también puede darse el caso de que haya sido intencionadamente. Obsérvese detenidamente el siguiente código:


```r
> y <- c(1.7, "a")  ## character
> y
```

```
[1] "1.7" "a"  
```

```r
> class(y)
```

```
[1] "character"
```

```r
> y <- c(TRUE, 2)   ## numeric
> print(y)
```

```
[1] 1 2
```

```r
> class(y)
```

```
[1] "numeric"
```

```r
> y <- c("a", TRUE) ## Character
> print(y)
```

```
[1] "a"    "TRUE"
```

```r
> class(y)
```

```
[1] "character"
```

En todos los casos anteriores hemos mezclados objetos de diferentes clases en un vector. No obstante, recordemos que la única regla en los vectores es que no podemos mezclas objetos de diferentes clases. Cuando esto sucede, se pone en marcha la _coercio_ para que cada elemento del vector seán de la misma clase.

En el ejemplo presentado hemos visto el efecto conocido como _coercion_ implícita. Con este mecanismo R intenta encontrar un manera de representar todos los objetos de una forma razonable.
