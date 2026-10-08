# Reto 001 — Solución de referencia

## 1. Comprender el problema

Tenemos una máquina que:

* acepta monedas de 1 €, 2 € y 5 €;
* tiene una cantidad limitada de cada moneda;
* recibe monedas de un cliente;
* entrega un producto cuando se ha alcanzado su precio;
* debe devolver el cambio exacto cuando el cliente paga de más.

El punto importante es que **tener suficiente dinero no garantiza poder devolver el cambio**.

---

## 2. Información necesaria

Necesitamos conocer:

```text
precioProducto

monedasAceptadas

monedasDisponibles

dineroIntroducido
```

Por ejemplo:

```text
precioProducto = 7

monedasAceptadas = [1, 2, 5]

monedasDisponibles:
    1 € → 3
    2 € → 2
    5 € → 1

dineroIntroducido = 0
```

---

## 3. Recibir el dinero

Mientras el dinero introducido sea inferior al precio:

```text
recibir moneda

si la moneda no es válida:
    devolver moneda

si la moneda es válida:
    añadirla a las monedas de la máquina
    sumar su valor al dinero introducido
```

Cuando el cliente ha introducido suficiente dinero:

```text
cambio = dineroIntroducido - precioProducto
```

---

## 4. Si no hay cambio

Si:

```text
cambio = 0
```

entonces:

```text
entregar producto
```

No es necesario buscar ninguna moneda.

---

## 5. Si hay cambio

Si:

```text
cambio > 0
```

tenemos que encontrar una combinación de las monedas disponibles que sume exactamente el cambio.

Por ejemplo:

```text
cambio = 6 €

monedas disponibles:

5 € → 1
2 € → 3
1 € → 0
```

Una estrategia que parece intuitiva sería:

```text
coger la moneda más grande posible
```

Por tanto:

```text
6 - 5 = 1
```

Pero no tenemos monedas de 1 €.

La estrategia falla.

Sin embargo:

```text
2 + 2 + 2 = 6
```

sí funciona.

Por tanto, **no podemos asumir que elegir siempre la moneda más grande produce una solución válida**.

---

## 6. Buscar una combinación válida

El problema se puede separar en una función conceptual:

```text
buscarCambio(cambio, monedasDisponibles)
```

Esta función debe responder:

```text
¿Existe alguna combinación de las monedas disponibles
que sume exactamente "cambio"?
```

Si existe:

```text
devolver las monedas utilizadas
actualizar las monedas disponibles
entregar el producto
```

Si no existe:

```text
no completar la venta
```

o utilizar la estrategia que el sistema haya definido para ese caso.

---

## 7. Algoritmo general

Una primera versión de pseudocódigo sería:

```text
precioProducto = 7

monedasDisponibles:
    1 € → 3
    2 € → 2
    5 € → 1

dineroIntroducido = 0

MIENTRAS dineroIntroducido < precioProducto:

    recibir moneda

    SI moneda no está en monedasAceptadas:
        devolver moneda

    SI NO:
        añadir moneda a monedasDisponibles
        dineroIntroducido = dineroIntroducido + valor(moneda)


cambio = dineroIntroducido - precioProducto


SI cambio == 0:

    entregar producto


SI cambio > 0:

    combinacion = buscarCambio(cambio, monedasDisponibles)

    SI combinacion existe:

        retirar combinacion de monedasDisponibles
        entregar producto
        devolver combinacion al cliente

    SI NO:

        cancelar operación
        devolver dinero al cliente
```

---

## 8. Problemas que quedan por resolver

Este algoritmo todavía contiene una parte que no hemos definido:

```text
buscarCambio(...)
```

Y eso es deliberado.

Ese problema requiere decidir cómo buscar entre las diferentes combinaciones posibles.

También habría que decidir:

* si queremos minimizar el número de monedas;
* qué hacer si existen varias combinaciones;
* qué hacer si no existe ninguna;
* cuándo se considera que una venta puede cancelarse;
* qué ocurre con las monedas introducidas si no se puede devolver el cambio.

Por tanto, el problema original se puede descomponer en varios problemas más pequeños.

---

## 9. Aprendizajes principales

### 1. Caso concreto y solución general no son lo mismo

Para el caso concreto:

```text
producto = 7 €
cliente = 5 € + 2 €
```

la solución es trivial.

Pero una máquina que funcione para cualquier precio necesita bastante más lógica.

### 2. El valor total disponible no es suficiente

Una máquina puede tener suficiente dinero para devolver el cambio y aun así no poder formar la cantidad exacta.

### 3. Una estrategia aparentemente buena puede fallar

"Utilizar siempre la moneda más grande posible" no garantiza una solución.

### 4. Un problema grande puede dividirse

El problema de la máquina contiene, entre otros:

```text
validar moneda
↓
acumular dinero
↓
calcular cambio
↓
buscar combinación
↓
actualizar estado
```

La parte más compleja puede convertirse en otro problema independiente.

---

## 10. Lo que habría que mejorar

Esta solución todavía no es un algoritmo completamente definido.

La principal pieza pendiente es:

```text
buscarCambio()
```

Ahí está el siguiente problema algorítmico interesante.

También habría que definir claramente qué debe ocurrir cuando no existe una combinación válida.

La solución presentada es, por tanto, una **descomposición del problema**, no una implementación definitiva.
