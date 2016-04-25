
# Calculando los requerimientos de memoria

Debido a que __R__ almacena todos sus objetos en la memoria física, es importante conocer cuanta memoria está siendo usada por estos objetos en tu espacio de trabajo. Una situación importante en la que es importante conocer la cantidad de memoria necesaria es cuando leemos un conjunto de datos en __R__. 

Por ejemplo, supongamos que tenemos un _data frame_ con _1.500.000_ de filas y _120_ columnas, las cuales todas son numéricas. Bien, la mayoría de computadores de hoy en dia usan _64_ bits de memoria para [numeros en punto flotante doble precision](https://es.wikipedia.org/wiki/IEEE_coma_flotante). Conociendo esta información podemos hacer los siguientes cálculos:


> 1.500.000 * 120 * 8 bytes/numeric = 1.440.000 bytes
                                    = 1.440.000 / 2^20^ byte/MB
                                    = 1.373,29 MB
                                    = 1.34 GB
                                    

Por lo tanto el conjunto de datos requiere 1.34 GB de memoria. La mayoría de ordenadores de hoy en día tienen esta RAM. Sin embargo, tenemos que tener en cuenta:

+ otros programas que se esten ejecutando en nuestro sistema
+ otros objetos __R__ que están utilizando memoria en nuestro espacio de trabajo


> ![](C:/Users/Drube/Documents/workspace/rprogramming/images/icon_exclamation.png) Importar un conjunto de datos cuando no poseemos suficiente memoria es un modo muy fácil de bloquear nuestro sistema (o al menos nuestra sesión en __R__). Esto es una situación que debemos evitar y que requiere que finalicemos el proceso __R__, en el mejor de los escenarios, o reiniciar nuestra computadora, en el peor de los casos. Por lo tanto, recomiendo encarecidamente que se tengan en cuenta los requerimientos de memoria antes de leer un conjunto de datos. 
