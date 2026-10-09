# Reto 005 — ¿Qué está contando realmente?

## Solución

La afirmación de que el programa suma todos los números de la lista es incorrecta.

El código es:

```text
numeros = [2, 4, 6]
contador = 0

PARA CADA numero EN numeros:
    contador = contador + 1

MOSTRAR contador
```

El bucle recorre los tres elementos de la lista, pero la instrucción del cuerpo no utiliza el valor de `numero`. En cada iteración incrementa `contador` en una unidad.

## Seguimiento de las variables

| Iteración | `numero` | `contador` antes | `contador` después |
| --------: | -------: | ---------------: | -----------------: |
|         1 |        2 |                0 |                  1 |
|         2 |        4 |                1 |                  2 |
|         3 |        6 |                2 |                  3 |

Al terminar, el programa muestra `3`, que es la cantidad de elementos recorridos.

## ¿Cómo sumar los valores?

Para acumular los valores de la lista, hay que sumar el elemento actual al acumulador:

```text
numeros = [2, 4, 6]
contador = 0

PARA CADA numero EN numeros:
    contador = contador + numero

MOSTRAR contador
```

El resultado sería `12`.

La expresión `contador += numero` es una abreviatura equivalente en los lenguajes que admiten esa sintaxis.

## Aprendizaje

Un bucle puede recorrer una colección sin utilizar sus valores para realizar cálculos.

Para comprender qué hace un programa, hay que distinguir entre:

* **Recorrer elementos:** visitar cada elemento de una colección.
* **Contar elementos:** incrementar un contador en cada iteración.
* **Acumular valores:** sumar el valor de cada elemento a un acumulador.

La clave de la lectura de código es seguir las instrucciones reales y el estado de las variables, sin asumir que el programa hace algo que el código no indica.
