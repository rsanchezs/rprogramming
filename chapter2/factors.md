
# Factores

Los factores son utilizados para representar categorías y pueden estar ordenadas o desordenadas. Podemos pensar en los factores como un vector de enteros en el que cada entero representa una etiqueta. Los factores son importantes en modelos estadísticos y se utilizan especialmente para modelar junto a funciones como _lm()_ y _glm()_.

El uso de factores con etíquetas es mejor que con enteros puesto que los factores són auto-descriptivos. Por ejemplo, si trabajamos con una variable que tiene los valores "Hombre" y "Mujer" es mejor que si lo hacemos con los valores _1_ y _2_.

Los objetos factor pueden ser creados con la función _factor()_.


```r
> x <- factor(c("yes", "yes", "no", "yes", "no"))
> x
```

```
[1] yes yes no  yes no 
Levels: no yes
```

```r
> table(x)
```

```
x
 no yes 
  2   3 
```

```r
> unclass(x)  ##vemos la representación interna del vector
```

```
[1] 2 2 1 2 1
attr(,"levels")
[1] "no"  "yes"
```

```r
> attr(x,"levels")
```

```
[1] "no"  "yes"
```

A menudo los factores serán creados por nosotros cuando importemos un conjunto de datos con funciones como _read.table()_. Este tipo de funciones crean factores por defecto cuando encuentran datos de tipo carácter o cadenas de carácteres ("_strings_").

El orden de los niveles de un factor puede ser establecido utilizando el argumento _levels_ de la función _factor()_. Esto puede ser importan en modelos liniales puesto que el primer nivel es utilizado como nivel base.


```r
> x <- factor(c("hombre", "hombre", "mujer", "hombre", "mujer"))
> x   ## los niveles son establecidos de forma alfabética
```

```
[1] hombre hombre mujer  hombre mujer 
Levels: hombre mujer
```

```r
> x <- factor(c("hombre", "hombre", "mujer", "hombre", "mujer"),levels = c("mujer", "hombre"))
> x
```

```
[1] hombre hombre mujer  hombre mujer 
Levels: mujer hombre
```


