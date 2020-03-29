Efectivamente, ahora vemos que el lobo está en la casa de la abuela :house_with_garden:, lo que confirma que había realizado correctamente lo que le pedimos con el mensaje `andaALaCasaDeLaAbuela()`.

Algo hizo el lobo en reacción a dicho mensaje, que provocó que una misma pregunta respondiera cosas diferentes antes y después de haberlo enviado. De alguna manera, se las ingenió para _recordar_ su ubicacion en cada momento y permitir que vaya cambiando.

Vamos a ampliar lo que veníamos diciendo de los mensajes:

* Como ya habiamos visto, si el mensaje es una pregunta, nos responde.
* Lo que agregamos ahora, es que si el mensaje es una indicación, una orden, hace lo que le decimos y no nos responde nada. Decimos que es un mensaje con **efecto**.

Para que todo esto fuera posible, el Lobo Feroz está definido de esta manera:

```wollok
object lobo {
   var ubicacion = "bosque"
   method dondeEstas() {
      return ubicacion
   }
   method andaALaCasaDeLaAbuela() {
      ubicacion = "casa de la abuela"
   }
  }
```

Para recordar en todo momento el lugar donde está, el lobo tiene un **atributo**. Se trata en particular de un atributo _variable_ denominada `ubicacion`. Su valor inicial es `"bosque"`, pero con el método `andaALaCasaDeLaAbuela()` su valor se modifica. 


Como el método `dondeEstas()` en vez de un valor puntual devuelve `ubicacion`, lo que obtenemos como respuesta es el valor al que se hace **referencia** con dicho atributo en el momento en que le preguntemos.

Las _variables_ se llaman así porque en un momento hacen referencia a un valor y en otro momento pueden hacer referencia a otro. La manera en que una variable cambia el valor al que refiere es mediante una **asignación**.

Tomá nota :memo: de la sintaxis:

- con `var` declaramos una variable
- el `=` indica una asignación; a su izquierda va la referencia y a su derecha lo que queremos asignar en ella.
- al declarar una variable le podemos asignar un valor inicial
- para indicar que el método no retorna nada no hacemos nada especial, simplemente no aparece el `return`.

> Ahora te toca hacerlo a vos
>
> Definí un objeto que represente al espejo mágico, pero que ahora la respuesta de quien es la más bella del reino no sea siempre la misma. 
> El `espejoMagico` debe entender los siguientes mensajes:

> * `quienEsLaMasBellaDelReino()` Al igual que el ejercicio anterior, inicialmente responde que es la reina malvada.
> * `pasoElTiempo()` Representa que pasaron los años y mientras tanto Blancanieves creció. Causa el efecto necesario para que luego, la pregunta anterior tenga por respuesta "Blancanieves".

  
  
