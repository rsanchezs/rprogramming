
# Números

Los números en __R__ son tratados como objetos de tipo _numeric_ (números reales de doble precisión). Esto quiere decir que si vemos en __R__ números com "1" or "2" nos puede llevar a pensar que estamos tratando con números enteros pero, en realidad detrás de bastidores __R__ los representa como _numeric_ (algo como "1.00" or "2.00"). Esto no és importante en la mayoría de los casos... excepto cuando sí lo és.

Si necesitamos trabajar con enteros debemos especificarlo explícitamente con el sufijo _L_. Por lo tanto, introduciendo en __R__ _1_ te devuelve un objeto de tipo _numeric_; introduciendo _1L_ nos devolvera un objeto de tipo entero.

Existe un tipo especial de número _Inf_ que representa _infinito_. Esto nos permite representar entidades como _1/0_. Así pues, _Inf_ puede ser utilizado en cálculos de tipo: _1 / Inf_ que es igual a _0_.

El valor _NaN_ representa un valor indefinido ("not a number"); por ejemplo _0 / 0_; _NaN_ puede ser considerado como un valor no definido (lo veremos en próximos capítulos).
