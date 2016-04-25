# Uso de formato de texto y binario para almacenar datos

Existen numerosas modos de almacenamiento de datos, estos incluyen desde archivos CSV o delimitados por tabulador, a formatos mas complejos como el binario. Sin embargo, existe un formato intermedio que es textual, pero no tan simple como los mencionados anteriormente. Este tipo textual de formato es nativo en __R__ y de alguna manera es legible por su naturaleza textual.

Podemos crear una representación más descriptiva de nuestros objetos __R__ utilizando las funciones _dput()_ o _dump()_. Estas funciones son útiles porque el resultado del formato textual es editable, y en caso de corrupción, potencialmente recuperable. A diferencia de otros modos, _dump()_ y _dput()_ preservan los _metadatos_ (sacrificando algo de legibilidad). Por ejemplo, podríamos almacenar la clase de cada columna de una tabla o los niveles de una variable factor.

Los formatos textuales trabajan mucho mejor con sistemas de control de versiones como _subversion_ o _git_, los cuales únicamente pueden comprobar cambios significativos en archivos de texto. Además, los formatos en texto pueden ser mas duraderos; si existe una corrupción en algún sitio en el archivo, puede ser fácilmente arreglado abriendo un editor de texto (aunque esto probablemente sólo suceda en el peor de los casos).

Por último, cabe mencionar que también existen inconvenientes en el uso de este tipo de almacenamiento.El motivo es que este tipo de formato no es muy eficiente en cuanto a almacenamiento. Por otro lado, también es difícil su legibilidad. Así pues, en ocasiones es preferible tener datos almacenados en un archivo CSV y tener por otro lado un archivo de código que especifique los metadatos.

