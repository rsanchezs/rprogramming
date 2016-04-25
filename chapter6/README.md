# Selección de objetos

Existen tres operadores que pueden ser utilizados para extraer subconjuntos de elementos en objetos __R__.

+ El operador __[__ siempre devuelve un objeto de la misma clase al original. Puede ser utilizado para seleccionar múltiples elementos en un objeto.
+ El operador __[[__ es usado para extraer elementos en una __lista__ o __data frame__. Sólo puede extraer un sólo elemento y la clase del objeto retornado no tiene que ser necesariamente de tipo lista o data frame.
+ El operador __$__ es usado para extraer elementos de una lista o data frame __por su nombre__ literal. La __semántica es similar a [[__.
