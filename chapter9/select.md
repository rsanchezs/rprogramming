
# select()

Para los ejemplos en este capítulo utilizaremos un conjunto de datos relacionados con los vuelos en el año 2013 en la ciudad de Chicago.


```
## Installing package into 'C:/Users/Ruben/Documents/R/win-library/3.3'
## (as 'lib' is unspecified)
```

```
## package 'devtools' successfully unpacked and MD5 sums checked
```

```
## Warning: cannot remove prior installation of package 'devtools'
```

```
## 
## The downloaded binary packages are in
## 	C:\Users\Ruben\AppData\Local\Temp\RtmpOAIc5F\downloaded_packages
```

```
## Downloading GitHub repo rstudio/EDAWR@master
## from URL https://api.github.com/repos/rstudio/EDAWR/zipball/master
```

```
## Installing EDAWR
```

```
## Installing 17 packages: babynames, colorspace, dichromat, forecast, fracdiff, ggplot2, gtable, labeling, munsell, quadprog, RColorBrewer, RcppArmadillo, reshape2, scales, timeDate, tseries, zoo
```

```
## Installing packages into 'C:/Users/Ruben/Documents/R/win-library/3.3'
## (as 'lib' is unspecified)
```

```
## package 'babynames' successfully unpacked and MD5 sums checked
## package 'colorspace' successfully unpacked and MD5 sums checked
## package 'dichromat' successfully unpacked and MD5 sums checked
## package 'forecast' successfully unpacked and MD5 sums checked
## package 'fracdiff' successfully unpacked and MD5 sums checked
## package 'ggplot2' successfully unpacked and MD5 sums checked
## package 'gtable' successfully unpacked and MD5 sums checked
## package 'labeling' successfully unpacked and MD5 sums checked
## package 'munsell' successfully unpacked and MD5 sums checked
## package 'quadprog' successfully unpacked and MD5 sums checked
## package 'RColorBrewer' successfully unpacked and MD5 sums checked
## package 'RcppArmadillo' successfully unpacked and MD5 sums checked
## package 'reshape2' successfully unpacked and MD5 sums checked
## package 'scales' successfully unpacked and MD5 sums checked
## package 'timeDate' successfully unpacked and MD5 sums checked
## package 'tseries' successfully unpacked and MD5 sums checked
## package 'zoo' successfully unpacked and MD5 sums checked
## 
## The downloaded binary packages are in
## 	C:\Users\Ruben\AppData\Local\Temp\RtmpOAIc5F\downloaded_packages
```

```
## "C:/PROGRA~1/R/R-33~1.0/bin/x64/R" --no-site-file --no-environ --no-save  \
##   --no-restore --quiet CMD INSTALL  \
##   "C:/Users/Ruben/AppData/Local/Temp/RtmpOAIc5F/devtools139c1f617d03/rstudio-EDAWR-2652ea6"  \
##   --library="C:/Users/Ruben/Documents/R/win-library/3.3" --install-tests
```

```
## 
```

Para importar el conjunto de datos del paquete __nycflights13__ en __R__:


```r
library(nycflights13) ##Cargamos la libreria
```

```
## Error in library(nycflights13): there is no package called 'nycflights13'
```

```r
data(package = "nycflights13") ##Importamos los datos en R
```

```
## Error in find.package(package, lib.loc, verbose = verbose): there is no package called 'nycflights13'
```

Si queremos trabajar con un conjunto de datos del paquete tendremos que cargarlo en el entorno __R__. Por ejemplo, si queremos trabajar con el data frame __planes__:


```r
data("planes")
```

```
## Warning in data("planes"): data set 'planes' not found
```
A continuación podemos realizar un examen preliminar del data frame:


```r
str(planes) ##Muestra la estrutura del data frame
```

```
## Classes 'tbl_df', 'tbl' and 'data.frame':	3322 obs. of  9 variables:
##  $ tailnum     : chr  "N10156" "N102UW" "N103US" "N104UW" ...
##  $ year        : int  2004 1998 1999 1999 2002 1999 1999 1999 1999 1999 ...
##  $ type        : chr  "Fixed wing multi engine" "Fixed wing multi engine" "Fixed wing multi engine" "Fixed wing multi engine" ...
##  $ manufacturer: chr  "EMBRAER" "AIRBUS INDUSTRIE" "AIRBUS INDUSTRIE" "AIRBUS INDUSTRIE" ...
##  $ model       : chr  "EMB-145XR" "A320-214" "A320-214" "A320-214" ...
##  $ engines     : int  2 2 2 2 2 2 2 2 2 2 ...
##  $ seats       : int  55 182 182 182 55 182 182 182 182 182 ...
##  $ speed       : int  NA NA NA NA NA NA NA NA NA NA ...
##  $ engine      : chr  "Turbo-fan" "Turbo-fan" "Turbo-fan" "Turbo-fan" ...
```

```r
dim(planes) ## n x m
```

```
## [1] 3322    9
```

```r
names(planes) ##nombre de las variables
```

```
## [1] "tailnum"      "year"         "type"         "manufacturer"
## [5] "model"        "engines"      "seats"        "speed"       
## [9] "engine"
```

```r
?planes ##documentación del data frame
```

```
## Warning in read.dcf(file.path(p, "DESCRIPTION"), c("Package", "Version")):
## cannot open compressed file 'C:/Users/Ruben/Documents/R/win-library/3.3/
## devtools/DESCRIPTION', probable reason 'No such file or directory'
```

```
## Warning in find.package(if (is.null(package)) loadedNamespaces() else
## package, : there is no package called 'devtools'
```

```
## No documentation for 'planes' in specified packages and libraries:
## you could try '??planes'
```

La función ___select()___ sirve para seleccionar una o varias columnas del data frame.


```r
select(planes, tailnum, year,type)
```

```
## Error in eval(expr, envir, enclos): could not find function "select"
```

Podemos utilizar la notación __:__ para seleccionar un rango de columnas:


```r
select(planes, tailnum:type)
```

```
## Error in eval(expr, envir, enclos): could not find function "select"
```
Podemos excluir una o varias columnas en nuestra selección del siguiente modo:


```r
select(planes, -tailnum)
```

```
## Error in eval(expr, envir, enclos): could not find function "select"
```

```r
select(planes, -(tailnum:type))
```

```
## Error in eval(expr, envir, enclos): could not find function "select"
```

La función __select()__ nos permite seleccionar un conjunto de columnas/variables según un patrón con la siguiente sintaxis:


```r
select(planes, starts_with("m"))
```

```
## Error in eval(expr, envir, enclos): could not find function "select"
```

```r
select(planes, ends_with("e"))
```

```
## Error in eval(expr, envir, enclos): could not find function "select"
```

A continuación mostramos un conjunto de funciones para __select__ que nos serán muy útiles:


+ __-__ : Selecciona todas las variables excepto
+ __:__ : Selecciona un rango
+ __contains()__ : Selecciona variables cuyo nombre contiene la cadena de texto
+ __ends_with()__: Selecciona variables cuyo nombre termina con la cadena de caracteres
+ __everything()__ : Selecciona todas las columnas
+ __matches()__: Selecciona las variables cuyos nombres coinciden con una expresión regular
+ __num_range()__: Selecciona las variables por posición
+ __one_of()__: Selecciona variables cuyos nombres están en un grupo de nombres
+ __start_with()__: Selecciona variables cuyos nombres empiezan con la cadena de caracteres.









