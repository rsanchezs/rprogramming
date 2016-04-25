
# Lectura de lineas en archivos de texto

Los archivos de texto pueden ser leídos línea a línea mediante la función _readLines()_. Esta función es útil cuando nos encontramos ante archivos con datos sin estructura o que no son estandard.


```
con <- gzfile("words.gz")
x <- readLines(con, 19)

```

Cuando nos encontremos con archivos con datos estructurados como archivos CSV o separados por tabuladores, existen otras funciones como _read.csv()_ o read.table().

El ejemplo anterior usa _gzfile()_ para crear una conexión a un archivo comprimido con el algoritmo gzip. Esta estrategia nos permite leer el archivo sin tener que descomprimirlo con anterioridad, lo que nos ahorra espacio y  tiempo.

Existe una función complementaria _writeLines()_ que toma un vector de caracteres como argumento y escribe cada elemento del vector en una línea diferente cada vez en el archivo de texto
