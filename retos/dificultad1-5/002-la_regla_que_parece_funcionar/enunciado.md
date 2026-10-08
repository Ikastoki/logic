# Reto 002 — La regla que parece funcionar

- **Categoría:** CONTRAEJEMPLOS
- **Categorías secundarias:** LOGICA, CASOS_LIMITE
- **Formato:** CONTRAEJEMPLO
- **Dificultad:** 1/5
- **Tiempo estimado:** 15 minutos

## Objetivo

Entrenar la capacidad de cuestionar una regla aparentemente correcta, identificar los supuestos sobre los que se apoya y encontrar el caso más pequeño que demuestre que no siempre funciona.

## Reto

Un compañero ha creado una regla para determinar si una lista de números está ordenada de menor a mayor.

Su razonamiento es el siguiente:

> "Si el primer número es menor que el último, entonces la lista está ordenada de menor a mayor."

Por ejemplo:

```text
[2, 4, 7]
```

El primer número es menor que el último, así que considera que la lista está ordenada.

Ahora afirma:

> "Esta comprobación es suficiente para cualquier lista."

Tu tarea es determinar si esa afirmación es siempre cierta.

## Condiciones

* La lista puede contener cualquier cantidad de números.
* Los números pueden repetirse.
* No se puede asumir que los números están ordenados previamente.
* Una lista está ordenada de menor a mayor si cada elemento no es mayor que el siguiente.
* Debes considerar también listas muy pequeñas.

## Ejemplos

Estas listas pueden ayudarte a analizar la afirmación:

```text
[1, 2, 3]
[1, 3, 2]
[5, 5]
[4]
```

No todas tienen que utilizarse para responder.

## Tu misión

1. Decide si la regla propuesta siempre funciona.
2. Si crees que no funciona, encuentra el **contraejemplo más pequeño** que puedas.
3. Explica exactamente por qué ese caso rompe la regla.
4. Identifica qué supuesto incorrecto está haciendo el razonamiento de tu compañero.
5. Explica qué tendría que comprobar realmente para poder afirmar que una lista está ordenada.

No necesitas escribir código.

<details>
<summary>Pista</summary>

No te centres primero en listas grandes.

Busca la diferencia entre comprobar una relación entre **dos elementos concretos** y comprobar una propiedad que debe cumplirse en **toda la lista**.

</details>
