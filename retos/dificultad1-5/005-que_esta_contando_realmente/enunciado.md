# Reto 005 — ¿Qué está contando realmente?

* **Categoría:** LECTURA_DE_CODIGO
* **Categorías secundarias:** LOGICA, DATOS_Y_ESTADO
* **Formato:** LECTURA_CODIGO
* **Dificultad:** 1/5
* **Tiempo estimado:** 10–15 min

## Objetivo

Practicar la lectura de código siguiendo los cambios de una variable y distinguiendo entre lo que parece hacer un programa y lo que realmente hace.

## Reto

Observa el siguiente pseudocódigo:

```text
numeros = [2, 4, 6]
contador = 0

PARA CADA numero EN numeros:
    contador = contador + 1

MOSTRAR contador
```

Una compañera afirma que el programa muestra la suma de todos los números de la lista.

¿Tiene razón?

## Condiciones

* El pseudocódigo es independiente de cualquier lenguaje de programación.
* `PARA CADA` recorre los elementos de la lista uno por uno.
* `contador` empieza con el valor `0`.
* Cada instrucción se ejecuta en el orden en que aparece.
* No supongas que una variable cambia de valor si no hay una instrucción que lo haga.

## Ejemplos

La lista contiene estos elementos:

```text
[2, 4, 6]
```

No se proporciona el resultado de la ejecución. Debes deducirlo siguiendo las instrucciones.

## Misión

Sin ejecutar el programa ni escribir código nuevo:

1. Explica qué ocurre en cada iteración del bucle.
2. Indica qué valor tiene `numero` en cada iteración.
3. Indica cómo cambia `contador` en cada iteración.
4. Determina qué muestra finalmente el programa.
5. Explica por qué la afirmación de tu compañera es correcta o incorrecta.

## Pista

<details>
<summary>Mostrar pista</summary>

Distingue entre la variable `numero`, que recibe el elemento actual de la lista, y la variable `contador`, que se incrementa en cada vuelta.

Sigue los valores de ambas variables paso a paso, sin adelantar el resultado.

</details>
