Ahora, queremos que la abuela cumpla años :birthday:
Si lo que buscamos es que la edad de la abuela aumente de a auno, por ejemplo pase a ser 100 a partir de saber que tiene 99, podríamos definirlo así:

``` wolok
object abuela {
  var edad = 99
  method cumplirAnios(){
    edad = edad + 1
  }
}
```

¿Pero cómo hacemos si queremos que cumpla de a varios años juntos? De alguna manera, cuando enviamos el mensaje, tenemos que indicarle cuantos años adicionales va a cumplir

Lo hacemos con un nuevo mensajes, en el que indicamos el valor en particular entre los paréntesis, 5 en este ejemplo: 
* `ム abuela.cumplirVariosAnios(5)`

Para que la abuela entienda el mensaje, le definimos un nuevo método.

``` wolok
  method cumplirVariosAnios(anios){
    edad = edad + anios
  }
```

Fijate que la definición del método también tiene ahora un elemento nuevo entre los paréntesis: `anios`. Le vamos a llamar **parámetro**. Se trata de una referencia al valor que se pasa cuando se envía el mensaje, o desde el punto de vista del objeto receptor, al valor que el método recibe. Es una variable, porque cada vez que se envía el mensaje, se lo puede hace con un valor diferente: en este primer ejemplo es 5, pero en otro contexto podría ser cualquier otro número. 

Pasar parámetros en un mensaje es una práctica muy común. Esos paréntesis que tenían los mensajes, que parecían molestos, ahora cobran sentido: sirven para agrupar los parámetros. Cuando son varios, se los separa con `,`

******************

Retomando el ejercicio anterior, algo que a veces estamos tentados de hacer es pretender modificar directamente desde afuera los atributos de un objeto, sin enviar mensajes.

Por ejemplo, si queremos que la edad de la abuela pase a valer 100, no podemos hacer esto:

* `ム abuela edad = 100`
* `ム abuela.edad = 100`
* `ム abuela.edad() = 100`

La solución es enviarle un mensaje con 100 como parámetro. 
* `ム abuela.edad(100)`

Y en otro momento podríamos hacer también.
* `ム abuela.edad(15)`

> A ver si lo podés hacer solo
> Definí el método necesario para que la abuela entienda los mensajes anteriores. Lo que queremos lograr es que la edad de la abuela quede en el valor en que nosotros querramos, sin importar su valor previo, y que lo podamos modificar cuantas veces como se nos de la gana.




