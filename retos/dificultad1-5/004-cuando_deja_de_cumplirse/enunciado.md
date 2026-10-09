# Reto 004 — ¿Cuándo deja de cumplirse?

* **Categoría:** LOGICA
* **Categorías secundarias:** CONTRAEJEMPLOS, CASOS_LIMITE
* **Formato:** CONTRAEJEMPLO
* **Dificultad:** 1/5
* **Tiempo estimado:** 10 minutos

## Objetivo

Practicar la comprobación de una regla mediante ejemplos y aprender a identificar los casos que merecen una atención especial.

## Reto

Un compañero propone la siguiente regla para determinar si una persona es mayor de edad:

> Si la edad es mayor o igual que 18, la persona es mayor de edad. En caso contrario, es menor de edad.

Afirma que la regla funciona para cualquier edad permitida por las condiciones del problema.

¿Estás de acuerdo con su afirmación?

## Condiciones

* La edad se expresa en años cumplidos.
* La edad es un número entero no negativo.
* Se considera que una persona alcanza la mayoría de edad al cumplir los 18 años.
* No hay otras condiciones que debas tener en cuenta.

## Ejemplos

| Edad | Resultado esperado |
| ---: | ------------------ |
|   16 | Menor de edad      |
|   17 | Menor de edad      |
|   18 | Mayor de edad      |
|   19 | Mayor de edad      |

## Misión

Sin escribir código:

1. Explica con tus palabras qué establece la regla.
2. Comprueba si funciona con los ejemplos proporcionados.
3. Identifica qué valor merece una comprobación especial y explica por qué.
4. Determina si existe algún caso permitido por las condiciones en el que la regla falle.
5. Explica qué podemos concluir después de comprobar varios ejemplos y qué no podemos asegurar únicamente con esas pruebas.

## Pista

<details>
<summary>Mostrar pista</summary>

Presta especial atención al valor que separa las dos categorías. Comprueba qué sucede justo antes, justo en ese valor y justo después.

No inventes condiciones nuevas: trabaja únicamente con las establecidas en el enunciado.

</details>
