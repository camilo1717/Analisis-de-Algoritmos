# Tema 10: Algoritmos Probabilistas

## Introducción

Los **algoritmos probabilistas** (o aleatorizados) son algoritmos que hacen uso de **números aleatorios** en el proceso de toma de decisiones. A diferencia de los algoritmos deterministas, que producen siempre la misma salida para una entrada dada, los probabilistas pueden producir diferentes resultados en ejecuciones distintas.

Este enfoque se ha vuelto importante en teoría de algoritmos y práctica computacional, especialmente en problemas donde los algoritmos deterministas son ineficientes o desconocidos.

## Características Generales

- Incorporan **generadores de números aleatorios** o fuentes de aleatoriedad.
- El comportamiento del algoritmo depende, al menos parcialmente, de estos valores aleatorios.
- Su análisis se basa en **probabilidades**, no solo en peor caso o casos promedio.

## Tipos de Algoritmos Probabilistas

Brassard y Bratley clasifican los algoritmos probabilistas en dos grandes categorías:

### 1. **Algoritmos de Monte Carlo**
- Tienen un tiempo de ejecución **determinista o limitado**.
- El resultado puede ser **incorrecto con cierta probabilidad**.
- La probabilidad de error puede reducirse aumentando el número de ejecuciones o muestras.
- Ejemplo típico: pruebas de primalidad como **Miller-Rabin**, donde se puede garantizar una baja probabilidad de error sin confirmar con certeza si un número es primo.

### 2. **Algoritmos de Las Vegas**
- Siempre devuelven un resultado **correcto**.
- Su tiempo de ejecución es **variable** y depende de la aleatoriedad.
- Son más seguros en cuanto a la precisión, pero su rendimiento puede ser menos predecible.
- Ejemplo típico: el algoritmo aleatorizado de **QuickSort**, donde la elección aleatoria del pivote afecta el tiempo de ejecución pero siempre produce un resultado correcto.

## Ejemplos de Aplicación

- **Pruebas de primalidad** (Monte Carlo)
- **QuickSort aleatorizado** (Las Vegas)
- **Algoritmos para el corte mínimo en grafos**
- **Algoritmos para juegos y simulaciones**
- **Algoritmos de hashing universal**

## Ventajas

- Suelen ser **más simples y eficientes** que sus equivalentes deterministas.
- Permiten **resolver problemas complejos** para los cuales no se conoce un buen algoritmo determinista.
- Son útiles para trabajar con grandes volúmenes de datos o entradas impredecibles.

## Desventajas

- Pueden ser **no deterministas** en el resultado o tiempo de ejecución.
- Requieren **análisis probabilístico**, lo cual puede ser más complejo.
- La aleatoriedad puede ser costosa si se necesita alta precisión o garantía de resultado.

## Conclusión

Los algoritmos probabilistas representan una poderosa herramienta en el diseño algorítmico moderno. Su capacidad de ofrecer soluciones eficientes a problemas difíciles, especialmente en contextos donde no existen métodos deterministas eficaces, los hace esenciales en muchas áreas de la informática. Comprender su naturaleza y cómo controlar el riesgo asociado es clave para su uso correcto.

---

> **Referencia**:  
> Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.
