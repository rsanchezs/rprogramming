
# Lectura de conexiones URL

Con la combinación de las funciones _readLines()_ y _url()_ podremos ser capaces de leer líneas de páginas web almacenadas en un servidor remoto.


```r
> ##Abrimos una conexión URL
> con <- url("http://www.uoc.edu", "r")
> 
> ## Leemos la página web
> x <- readLines(con)
```

```
Warning in readLines(con): incomplete final line found on 'http://
www.uoc.edu'
```

```r
> ## Mostramos unas pocas líneas
> head(x)
```

```
[1] ""                                                                                                                             
[2] "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">"
[3] "<html xmlns=\"http://www.w3.org/1999/xhtml\" lang=\"ca\">\t"                                                                   
[4] "<head>"                                                                                                                       
[5] "\t<meta http-equiv=\"Content-Type\" content=\"text/html;charset=ISO-8859-1\" />"                                               
[6] "\t<meta name=\"robots\" \t\t\t\t\tcontent=\"all\" />"                                                                               
```

La estrategia que hemos utilizado en el ejemplo anterior podemos utilizarla para leer archivos de datos que esten almacenados en servidores web.

El uso de conexiones URL es útil para producir análisis reproducibles, ya que nuestro código estará documentando de dónde provienen los datos y como fueron obtenidos. Esta estrategia es preferible a la descarga del archivo desde un navegador web. Sin embargo, corremos el riesgo que el código que hemos escrito no funcione en un futuro si las cosas han cambiado en el lado del servidor.
