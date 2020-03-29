El motivo por el cual Caperucita sabe responder a algunos mensajes y otros no, es porque cuando declaramos el objeto que la representa, indicamos qué y cómo responder.

Un objeto se define con un nombre y una serie de porciones de código que se denominan *métodos*, que indican qué mensajes puede responder y describen la manera en que lo hacen.

Por ejemplo, para que `caperucita` pueda responder a las preguntas anteriores, tiene que estar definido lo siguiente:

```wollok
object caperucita {
  method vasACasaDeTuAbuelita() {
    return true
  }
  method cuantoPesas() {
    return 80 
  }
  method comoEstas() {
    return "contenta de venir a una clase de programación"
  }
  method deQueColorEsLoQueLlevasEnLaCanasta() {
    return "rojo" 
  }
}
```

Como podemos ver, en primer lugar está declarado el objeto `caperucita` y luego cada uno de los métodos para responder a las preguntas que le hicimos.

Tomá nota :memo: de los elementos sintácticos que utilizamos:

* la palabra `object` delante del nombre del objeto.
* `{}` para encerrar lo que estamos definiendo de ese objeto; en este ejemplo, todo el código.
* la palabra `method` delante del nombre de cada método del objeto.
* `()` al final del nombre, tal cual como lo usamos al enviar el mensaje.
* nuevamente `{}` para encerrar todo lo que abarca el método.
* la palabra `return` para indicar cuál es la respuesta que se debe retornar en cada caso.
* Como detalle, a las cadenas de caracteres las encerramos entre `""`, los valores de verdad se son `true` y `false` y los numeros tal cual son.
 
___

Si queremos que funcione el mensaje que anteriormente daba error podemos declarar un nuevo método al objeto `caperucita`. 

Sería sencillo, pero pensándolo mejor no tiene mucho sentido que sea Caperucita quien responda, sino otro personaje...  

> Declará un objeto para representar al espejo mágico, que sepa decir quién es la mas bella del reino y, tal como sucede al inicio del cuento, nos responda que es la "reina malvada".
