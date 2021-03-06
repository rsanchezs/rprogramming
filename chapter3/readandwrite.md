
# Lectura y escritura de datos

Existen las siguientes funciones para la lectura de datos en __R__.

+ _read.table, read.csv_, para la lectura de datos de forma o estructura de tabla
+ _readLines_, para la lectura de líneas en archivos de texto
+ _source_, para la lectura en archivos __R__ (_inverso de dump_)
+ _dget_, para la lectura en archivos __R__ (_inverso de dput_)
+ _load_, para la lectura de espacios de trabajo previamente guardados
+ _unserialize_, para la lectura de un único objeto __R__ en formato binario

Existen desde luego, gran cantidad de paquetes en __R__ para la lectura de todo tipo de conjunto de datos, y en ocasiones nos veremos obligados a recurrir a alguno de estos paquetes si estamos trabajando en area específica.

Las funciones análogas para la escritura de datos a archivos son las siguientes.

+ _write.table_, para la escritura de datos en forma de tabla en archivos de texto (ej. _CSV_) o "_connection_"
+ _writeLines_, para la escritura de datos tipo carácter línia a línia en un archivo o _connection_
+ _dump_, para el volcado de representaciones textuales de varios objetos __R__
+ _dput_, para la salida de una representación textual de un objeto __R__
+ _save_, para el almaciento de un número arbitrario de objetos __R__ en formato binario (posiblemente comprimidos) a un archivo
+ _serialize_, para convertir un objeto __R__ a formato binario para la salida a una _connection_ (o archivo)
