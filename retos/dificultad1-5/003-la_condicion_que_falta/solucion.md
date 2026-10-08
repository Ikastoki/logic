# Reto 003 — La condición que falta

## Solución

La afirmación:

> «Para saber si una persona puede entrar en una sala, basta con comprobar si tiene una entrada.»

no es siempre cierta.

Tener una entrada es solo una de las condiciones posibles. La entrada puede corresponder a otra obra, a otra fecha u hora, la persona puede no cumplir la edad mínima o la entrada puede no ser válida o haber sido utilizada anteriormente.

Por tanto, necesitamos conocer **qué condiciones definen que una persona pueda entrar**.

En el contexto de este reto, establecemos estos requisitos:

1. La entrada corresponde a la obra correcta.
2. La fecha y hora son correctas.
3. La persona cumple la edad mínima.
4. La entrada es válida y no ha sido utilizada.

La regla puede reformularse entonces como:

> Una persona puede entrar si tiene una entrada válida y cumple todos los requisitos establecidos para esa entrada.

### Una cuestión importante

No debemos seguir añadiendo requisitos indefinidamente.

Por ejemplo, podríamos inventar que también es obligatorio vestir de una determinada manera, estar en una puerta concreta o cumplir cualquier otra condición. Pero si esas condiciones no forman parte del problema, no debemos utilizarlas para demostrar que nuestra solución es incorrecta.

Esto muestra una idea fundamental:

**Antes de comprobar si una solución es correcta, hay que definir claramente las condiciones y el alcance del problema.**

Una solución solo debe evaluarse respecto a las reglas que realmente forman parte del enunciado.

### Aprendizaje

El reto entrena una habilidad básica de resolución de problemas:

**identificar las condiciones necesarias antes de intentar construir una solución.**

También enseña a distinguir entre:

* un caso límite válido que está contemplado por el problema;
* y una condición inventada que nunca fue establecida.

Si las reglas del problema están mal definidas, podemos discutir indefinidamente sobre posibles excepciones sin acercarnos a una solución.
