
# Creando vectores

La función _c()_ puede ser usada para crear objetos.


```r
> x <- c(0.5, 0.6)      ## numeric
> x <- c(TRUE, FALSE)   ## logical
> x <- c(T, F)          ##logical
> x <- c("a", "b", "c") ##character
> x <- 9:29             ##integer
> x <- c(1+0i, 2+4i)    ##complex
```

Obsérvese en el ejemplo anterior que _T_ y _F_ és lo mismo que _TRUE_ y _FALSE_ respectivamente. Sin embargo, deberíamos utilizar los valores _TRUE_ y _FALSE_ para indicar los valores lógicos, es considerado una buena práctica.

También podemos utilizar la función _vector()_ para inicializar vectores.


```r
> x <- vector("numeric", length = 10)
> x
```

```
 [1] 0 0 0 0 0 0 0 0 0 0
```

