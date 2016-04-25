
# Conexiones con archivos

Las conexiones con archivos de texto pueden ser creadas con la función _file()_.


```r
> str(file)
```

```
function (description = "", open = "", blocking = TRUE, encoding = getOption("encoding"), 
    raw = FALSE)  
```

La función _file()_ tiene una serie de argumentos que son comunes a la mayoría de las demás funciones de conexión.

+ _description_ es el nombre del archivo
+ _open_ es un código indicando el modo en que el archivo tiene que ser abierto

Las diferentes opciones del argumento _open_ son:

+ "r" abre el archivo en modo lectura
+ "w" abre el archivo en modo escritura (crea un nuevo archivo)
+ "a" abre un archivo para escribir en el final
+ "rb", "wb", "ab" escritura, lectura, concatenación en modo binario (Windows)

En la practica, nosotros no trataremos con la interface conexión directamente, ya que la mayoría de las funciones lo hacen por nosotros en segundo plano.

Por ejemplo, si lo hiciéramos de forma explícita, una manera de leer un archivo CSV podría ser como mostramos a continuación:

```
## Crea un conexión a "foo.txt"
con <- file("foo.txt")

##Abre la conexión en "foo.txt" en modo lectura
open(con, "r")

##Lee los datos de la conexión
data <- read.csv(con)

##Cierra la conexión
close(con)

```
siendo lo mismo

```
data <- read.csv("foo.txt")

```
como mencionábamos anteriormente entre bastidores la función _open.csv()_ abre una conexión con el archivo _foo.txt_ y la cierra cuando ha terminado.












