# Tema 4: Divide and Conquer (Cormen et al., 2022)

## Introducción

El enfoque **Divide and Conquer (Dividir y Vencerás)** es una técnica fundamental en el diseño de algoritmos. Consiste en descomponer un problema en varios subproblemas más pequeños, resolverlos de manera recursiva y luego combinar esas soluciones para formar la solución del problema original.

Este paradigma es ampliamente utilizado en algoritmos eficientes y ha demostrado ser una herramienta poderosa para mejorar el rendimiento en diversos tipos de problemas.

## Estructura General

Un algoritmo basado en Divide and Conquer sigue tres pasos fundamentales:

1. **Dividir**: Se divide el problema en uno o más subproblemas más pequeños del mismo tipo.
2. **Conquistar**: Se resuelven recursivamente los subproblemas. Si el tamaño del subproblema es lo suficientemente pequeño, se resuelve directamente.
3. **Combinar**: Se combinan las soluciones de los subproblemas para obtener la solución del problema original.

## Ejemplos Clásicos

- **Merge Sort**: Divide el arreglo en mitades, ordena recursivamente cada mitad y luego las combina.
- **Quick Sort**: Selecciona un pivote, divide el arreglo en dos partes (menores y mayores que el pivote), y ordena recursivamente cada parte.
- **Binary Search**: Divide la búsqueda en mitades y continúa en la subparte correspondiente.
- **Strassen’s Matrix Multiplication**: Divide matrices grandes en submatrices más pequeñas y realiza multiplicaciones más eficientes.

## Análisis de Complejidad

La complejidad de un algoritmo Divide and Conquer suele representarse mediante una **relación de recurrencia**. Un caso típico es:

T(n) = a T(n/b) + f(n)


donde:
- `n` es el tamaño del problema,
- `a` es el número de subproblemas,
- `n/b` es el tamaño de cada subproblema,
- `f(n)` es el tiempo requerido para dividir y combinar.

El **Teorema Maestro (Master Theorem)** se utiliza para resolver estas recurrencias y analizar la eficiencia del algoritmo.

## Ventajas

- Favorece el paralelismo.
- Maneja grandes cantidades de datos de forma más eficiente.
- Simplifica la resolución de problemas complejos.

## Conclusión

Divide and Conquer es una estrategia potente que aparece en numerosos algoritmos eficientes. Comprender su estructura y cómo analizar su rendimiento es esencial para el diseño de algoritmos avanzados.

---

> **Referencia**:  
> Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2022). *Introduction to Algorithms* (4th ed.). MIT Press.
