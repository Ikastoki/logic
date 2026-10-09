# Reto 004 — ¿Cuándo deja de cumplirse?

## Solución

La regla propuesta es correcta según las condiciones del problema:

* Si la edad es mayor o igual que 18, la persona es mayor de edad.
* Si la edad es menor que 18, la persona es menor de edad.

Como la edad es un número entero no negativo, todos los valores permitidos quedan cubiertos por una de las dos condiciones.

## Comprobación de los ejemplos

| Edad | Regla aplicada       | Resultado     |
| ---: | -------------------- | ------------- |
|   16 | Menor que 18         | Menor de edad |
|   17 | Menor que 18         | Menor de edad |
|   18 | Mayor o igual que 18 | Mayor de edad |
|   19 | Mayor o igual que 18 | Mayor de edad |

Todos los resultados coinciden con lo establecido en el enunciado.

## El caso límite

La edad de 18 años es el caso más importante porque marca el límite entre las dos categorías.

Conviene comprobar tres valores:

* **17:** justo por debajo del límite.
* **18:** exactamente en el límite.
* **19:** justo por encima del límite.

Si solo probáramos 16, 17, 19 y 20, no habríamos comprobado directamente qué sucede en el valor donde cambia la clasificación.

## ¿Basta con probar ejemplos?

No. Que una regla funcione con varios ejemplos no demuestra, por sí solo, que funcione con todos los valores permitidos.

En este caso, podemos justificar que funciona porque las condiciones están claramente definidas y las dos posibilidades cubren todas las edades permitidas:

* Edad menor que 18.
* Edad mayor o igual que 18.

No queda ningún valor permitido fuera de esas categorías.

## Aprendizaje

Para comprobar una regla:

1. Entender las condiciones que debe cumplir.
2. Probar ejemplos representativos.
3. Comprobar especialmente los valores límite.
4. Verificar que todos los casos permitidos quedan cubiertos.

**Idea clave:** definir bien las condiciones reduce la ambigüedad, y elegir buenas pruebas ayuda a detectar errores que los ejemplos habituales podrían ocultar.
