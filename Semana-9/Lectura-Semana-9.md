# Tema 6: Algoritmos Voraces (Greedy Algorithms)

## Introducción

Los **algoritmos voraces** constituyen una técnica de diseño algorítmico que consiste en tomar, en cada etapa del proceso de resolución de un problema, la decisión que **parezca ser la mejor en ese momento**. Es decir, el algoritmo realiza una serie de elecciones locales óptimas con la esperanza de que estas decisiones conduzcan a una **solución global óptima**.

Esta estrategia es apreciada por su **simplicidad y eficiencia**, ya que no explora todo el espacio de soluciones posibles como lo haría, por ejemplo, una técnica de programación dinámica o de fuerza bruta. Sin embargo, su aplicabilidad depende de ciertas propiedades específicas del problema.

## Principios Fundamentales

Para que un algoritmo voraz sea correcto (es decir, devuelva una solución óptima), el problema debe cumplir con las siguientes propiedades:

### 1. Subestructura óptima
Un problema tiene **subestructura óptima** si una solución óptima del problema puede construirse a partir de soluciones óptimas de sus subproblemas. Esta característica también está presente en problemas que se resuelven con programación dinámica.

### 2. Propiedad de elección voraz
La **elección voraz** implica que siempre existe una opción localmente óptima que forma parte de alguna solución global óptima. Esta propiedad es exclusiva de los problemas que se pueden resolver correctamente con un algoritmo voraz.

Si un problema no cumple con esta propiedad, el algoritmo voraz podría devolver una solución incorrecta o subóptima.

## Funcionamiento General de un Algoritmo Voraz

Un algoritmo voraz suele seguir los siguientes pasos:

1. **Inicialización**: Se parte de una solución vacía o parcial.
2. **Selección**: Se elige la mejor opción local entre las disponibles según un criterio específico.
3. **Factibilidad**: Se verifica que la elección sea válida dentro del contexto del problema.
4. **Incorporación**: Se añade la elección a la solución.
5. **Repetición**: Se repite el proceso hasta completar la solución.

## Ejemplos Clásicos

Existen varios problemas clásicos en los que los algoritmos voraces funcionan de manera eficiente y garantizan una solución óptima. Algunos de ellos son:

### - Árbol de expansión mínima
Algoritmos como **Kruskal** y **Prim** construyen un árbol de expansión mínima conectando todos los nodos de un grafo con el costo total más bajo. Ambos se basan en seleccionar la arista más barata disponible que no forme ciclos.

### - Codificación de Huffman
Utilizado en compresión de datos. Este algoritmo genera un árbol binario óptimo asignando códigos más cortos a los símbolos más frecuentes, minimizando así la longitud total del mensaje codificado.

### - Selección de actividades
Se trata de seleccionar el mayor número posible de actividades compatibles (que no se traslapen en el tiempo). El algoritmo voraz elige siempre la actividad que termina más temprano.

### - Problema del cambio de monedas
Consiste en dar cambio con la menor cantidad de monedas. El enfoque voraz funciona correctamente solo si las denominaciones de monedas están diseñadas de forma compatible (por ejemplo, en sistemas como el estadounidense o el europeo). En otros casos, puede fallar.

## Limitaciones

No todos los problemas se prestan para ser resueltos mediante algoritmos voraces. Por ejemplo:

- **Problema de la mochila (0/1 Knapsack Problem)**: La solución óptima no puede ser garantizada por un enfoque voraz, ya que tomar el objeto de mayor valor por unidad de peso puede no conducir a la mejor combinación global.

Es crucial analizar cuidadosamente si el problema cumple con la **subestructura óptima** y la **propiedad de elección voraz** antes de aplicar esta estrategia.

## Ventajas

- Generalmente son más simples de implementar.
- Requieren menos recursos computacionales.
- Son rápidos y eficientes para problemas donde son aplicables.

## Conclusión

Los algoritmos voraces representan una herramienta poderosa en el diseño de algoritmos, pero su eficacia depende estrictamente de las propiedades del problema a resolver. Identificar correctamente si un problema puede ser resuelto de forma voraz es tan importante como el algoritmo en sí.

---

> **Referencia:**  
> Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.
