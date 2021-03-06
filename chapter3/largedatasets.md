
# Leyendo grandes conjuntos de datos

Ver el video de esta sección:

{%youtube%}BJYYIJO3UFI{%endyoutube%}


Cuándo trabajemos con grandes volúmenes de datos, podemos hacer una serie de cosas que harán nuestra vida más fácil y prevendrán que __R__ se ahogue.

+ Leer la página de ayuda de la función _read.table_, la cual contiene muchas pistas.
+ Realizar un cálculo aproximado de la cantidad necesaria de memoria que necesitan nuestro conjunto de datos (véase la siguiente sección para un ejemplo).
+ Poner _comment.char = ""_ si no existen líneas de comentario en nuestro archivo.
+ Usar el argumento _colClasses_. 

Una manera de comprobar la clase de cada columna es la siguiente:


```r
> initial <- read.table("datatable.txt", nrows = 100) ## ponemos nrows para un mejor uso de memoria
> classes <- sapply(initial, class)
> tabAll <- read.table("datatable.txt", colClasses = classes)
```

En general, cuándo utilizamos __R__ con grandes volúmenes de datos, es útil conocer una serie de cosas sobre nuestro ordenador.

+ La cantidad de memoria.
+ Otras aplicaciones que estén en uso. En la medida de lo posible intentar cerrar las que podamos.
+ En sistemas multiusuarios, tener en cuenta la cantidad de usuarias conectados.
+ El sistema operativo que utilizamos.
