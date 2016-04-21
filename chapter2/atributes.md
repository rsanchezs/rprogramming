
# Atributos

Los objetos en __R__ pueden tener atributos, estos són como metadatos para el objeto. Estos metadatos pueden ser muy útiles ya que nos proporcionan información del objeto. Por ejemplo, los nombres de columna en un _data frame_ nos proporcionan información de lo que contiene cada columna. Algunos ejemplos de atributos en objetos __R__ son:

+ names, dimnames
+ dimensions (en matrices, arrays)
+ class (e.g. integer, numeric)
+ length
+ otros atributos/metadatos definidos por el usuario

A los atributos de un objeto si los hay, se puede acceder mediante la función _attributes()_. No todos los objetos contienen atributos, en este caso la función  _attributes()_ devolverá _NULL_.
