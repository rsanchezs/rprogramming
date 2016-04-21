
# Valores indefinidos

Los valores indefinidos son indicados en __R__ por _NA_ o _NaN_ para cualquier operación indefinida matematicamente.

+ _is.na()_ se utiliza para comprobar si los objetos son _NA_
+ _is.nan()_ se utiliza para comprobar si los objetos son _NaN_
+ _NA_ pertenecen a una clase, por lo tanto nos podemos encontrar con integer _NA_, character _NA_, etc.
+ Un valor _NaN_ es también un _NA_ pero lo contrario es falso.


```r
> ## Crea un vector con valore Na
> x <- c(1, 2, NA, 10, 3)
> ##Devuelve un vector lógico indicando que elementos son NA
> is.na(x)
```

```
[1] FALSE FALSE  TRUE FALSE FALSE
```

```r
> ##Devuelve un vector lógico indicando que elemetos son NaN
> is.nan(x)
```

```
[1] FALSE FALSE FALSE FALSE FALSE
```


```r
> ## Crea un vector con valores Na y NaN
> x <- c(1, 2, NA, NaN, 3)
> ##Devuelve un vector lógico indicando que elementos son NA
> is.na(x)
```

```
[1] FALSE FALSE  TRUE  TRUE FALSE
```

```r
> ##Devuelve un vector lógico indicando que elemetos son NaN
> is.nan(x)
```

```
[1] FALSE FALSE FALSE  TRUE FALSE
```

