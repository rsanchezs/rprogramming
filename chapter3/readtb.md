
# Leyendo archivos con read.table()

La función _read.table()_ es de las más utilizadas para la lectura de datos. Se recomienda encarecidamente la lectura del archivo de ayuda para _read.table()_ (ejecutar _?read.table_ en __R__).

A continuación se muestran los argumentos de la función:

+ _file_, el  nombre del archivo o conexión
+ _header_, de tipo lógico indicando si el archivo contiene una línia de cabecera
+ _sep_, una cadena indicando como están separadas las columnas
+ _colClasses_, un vector de carácteres indicando la clase de cada columna en el conjunto de datos
+ _nrows_, el número de filas en el conjunto de datos. Por defecto _read.table)_ lee el archivo entero
+ _comment.char_, una cadena indicanto el tipo de character utilizado en los comentarios. Por defecto es "__#__". Se recomienda que si no existen líneas comentadas, pasar como argumento la cadena vacía (__""__).
+ _skip_, el número de líneas para salter desde el principio
+ _stringAsFactors_, para codificar las variables de tipo carácter como factores

Para conjunto de un tamaño pequeño o moderado, podemos utilizar la función _read.table()_ sin especificar ningún argumento.

```{}
data <- read.table("foo.txt")

```

En este caso, R automáticamente realizará lo siguiente:

+ saltará las líneas que empiezen con _#_
+ calculará cuántas línias tiene el archivo (y cuánta memoria necesita)
+ calculará que tipo de variable almacena cada columna

Es importante mencionar que si pasamos los argumentos anteriormente mencionados a la función _read.table_ haremos que trabaje más eficazmente y mucho más rápido.

La función __read.csv()__ es idéntica a la función que hemos visto anteriormente excepto en algunos argumentos por defecto (ej. como el argumento _sep_)











