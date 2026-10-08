# Reto 003 — La condición que falta

**Categoría:** DESCOMPOSICION
**Secundarias:** LOGICA, CASOS_LIMITE
**Formato:** PROBLEMA
**Dificultad:** 1/5
**Tiempo estimado:** 10–15 min

## Objetivo

Aprender a identificar qué información y condiciones son necesarias antes de intentar resolver un problema.

## Reto

Un compañero dice:

> «Para saber si una persona puede entrar en una sala, basta con comprobar si tiene una entrada.»

¿Estás de acuerdo con esta afirmación?

Antes de pensar en una solución, analiza qué tendría que cumplirse realmente para que una persona pueda entrar.

## Condiciones

Para este problema, considera que para poder entrar deben cumplirse estas condiciones:

1. La entrada corresponde a la obra correcta.
2. La fecha y hora son correctas.
3. La persona cumple la edad mínima.
4. La entrada es válida y no ha sido utilizada.

No añadas nuevas condiciones que no estén definidas en el problema. El objetivo es razonar sobre las condiciones establecidas.

## Ejemplos

```text
Persona A → tiene entrada
Persona B → no tiene entrada
```

Estos ejemplos por sí solos no proporcionan toda la información necesaria para decidir si una persona puede entrar.

## Misión

Sin escribir código:

1. Decide si la afirmación inicial es siempre cierta.
2. Si no lo es, encuentra un contraejemplo.
3. Identifica qué información falta para poder tomar la decisión.
4. Reformula la regla de manera que tenga en cuenta todas las condiciones establecidas.
5. Explica por qué es importante definir previamente las condiciones del problema.

**Importante:** no se trata de buscar infinitas excepciones inventando nuevas reglas. Una vez definidas las condiciones del problema, el razonamiento debe mantenerse dentro de ellas.

<details>
<summary>Pista</summary>

No te centres únicamente en si la persona tiene una entrada. Pregúntate qué propiedades debe tener esa entrada y qué condiciones debe cumplir la persona para que esa entrada permita realmente el acceso.

</details>
