¡Los _atributos_ y los _metodos_ son cosas distintas!

Veamos de a uno:

`abuela.edad()`

Es un envío de mensaje bien escrito, pero no existe el método `edad()` en la abuela. 

`abuela.edad` 

No es un envío de mensaje, porque le faltan los `()`. 
Y si lo que pretendías hacer es acceder a la variable de la abuela sin enviar un mensaje... ¡No se puede! Sólo podemos comunicarnos con un objeto enviándole mensajes.

`abuela edad` 

Esto no es nada. Si te animaste a probarlo, el error que te dio debe haber sido feo...  

Esto nos lleva a ver que las variables no se pueden acceder desde afuera del objeto, decimos que son **privadas**.

Si queremos preguntarle a la abuela cuantos años tiene, sí o sí tenemos que definir un método para ello. 

Vamos a denominar **encapsulamiento** a esta característica de un objeto de ser el único que puede manipular sus propios atributos. 

En otras palabras, retomando la idea de entender a los _objetos_ como _sujetos_, podemos decir que cada objeto mantiene oculta su _intimidad_ y los demás objetos lo respetan.

> Te animás a hacer un método para que la abuela pueda responder su edad? 
