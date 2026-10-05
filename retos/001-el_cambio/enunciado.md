# Reto 001 — El cambio

- **Categoría:** LÓGICA
- **Categorías secundarias:** DESCOMPOSICIÓN, CASOS_LIMITE
- **Formato:** PROBLEMA
- **Dificultad:** 1/5
- **Tiempo estimado:** 15 minutos

## Objetivo

Entrenar la capacidad de descomponer un problema y detectar qué información es realmente necesaria para resolverlo.

## Reto

Una máquina expendedora acepta monedas de 1 €, 2 € y 5 €.

Un producto cuesta 7 €.

Una persona introduce monedas hasta que la máquina tiene suficiente dinero para pagar el producto. En ese momento, la máquina debe devolver el cambio exacto utilizando las monedas que tiene disponibles.

La máquina empieza el día con:

* 3 monedas de 1 €
* 2 monedas de 2 €
* 1 moneda de 5 €

La persona introduce:

* una moneda de 5 €
* una moneda de 2 €

La máquina debe entregar el producto y devolver el cambio correspondiente.

### Tu misión

Determina:

1. ¿Cuánto cambio debe devolver la máquina?
2. ¿Qué monedas puede utilizar para devolverlo?
3. ¿Hay más de una forma válida de hacerlo?
4. ¿Qué ocurre con las monedas que quedan en la máquina después de la operación?

Después, intenta responder a esta pregunta:

> ¿Qué información adicional necesitarías si quisiéramos convertir este problema en un algoritmo que funcionase para cualquier precio, cualquier combinación de monedas y cualquier cantidad disponible?

No necesitas escribir código.

<details>
<summary>Pista</summary>

No pienses todavía en "qué algoritmo utilizar".

Primero intenta representar el estado de la máquina **antes y después** de la compra.

</details>
