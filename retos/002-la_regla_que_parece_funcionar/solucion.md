# Reto 002 — La regla que parece funcionar

## Solución

La regla «si el primer número es menor que el último, entonces la lista está ordenada» es incorrecta.

Un contraejemplo mínimo es:

`[1, 3, 2]`

El primer número (`1`) es menor que el último (`2`), pero la lista no está ordenada porque `3 > 2`.

El error de la regla es asumir que comparar únicamente los extremos permite conocer la relación entre todos los elementos intermedios. Una lista ordenada debe cumplir una propiedad local en **cada pareja de elementos consecutivos**:

`elemento[i] <= elemento[i + 1]`

Por tanto, no es necesario ordenar la lista. Basta con recorrerla y comprobar esas comparaciones.

### Estrategia

Para cada posición:

1. Comparar el elemento actual con el siguiente.
2. Si el actual es mayor que el siguiente, la lista no está ordenada.
3. Si ninguna comparación incumple la condición, la lista está ordenada.

### Complejidad

* **Tiempo:** O(n), porque en el peor caso se recorren los elementos una vez.
* **Espacio adicional:** O(1), si se realiza la comprobación directamente sobre la lista.

### Idea clave

Hay que distinguir entre:

* **Ordenar una lista:** modificarla para que cumpla una propiedad.
* **Comprobar si está ordenada:** verificar si ya cumple esa propiedad.

En este reto, ordenar sería trabajo innecesario. La solución correcta consiste en verificar directamente la propiedad que define el orden.
