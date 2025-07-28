# Subtema 6.4: Grafos – Caminos Mínimos

## Introducción

El problema de los **caminos mínimos** en grafos consiste en encontrar la ruta más corta entre dos vértices, o desde un vértice origen a todos los demás. Este es un problema clásico en teoría de grafos con múltiples aplicaciones prácticas como redes de transporte, enrutamiento en redes informáticas, análisis de mapas, y más.

En este contexto, el uso de **algoritmos voraces** es especialmente eficaz cuando se trata de grafos ponderados, es decir, grafos donde las aristas tienen un costo o peso asociado.

## Definición del Problema

Dado un grafo dirigido o no dirigido con pesos no negativos en sus aristas, el objetivo es encontrar el camino de costo mínimo desde un vértice fuente a los demás vértices del grafo. Se trata de minimizar la suma de los pesos de las aristas a lo largo del recorrido.

## Algoritmo de Dijkstra

El algoritmo más representativo para resolver el problema de caminos mínimos en este contexto es el **algoritmo de Dijkstra**, un enfoque clásico de tipo voraz. Este algoritmo asume que **todos los pesos son no negativos** y funciona eficientemente en grafos densos o dispersos.

### Funcionamiento general:

1. Se inicializa una tabla de distancias con infinito para todos los vértices excepto el nodo origen, que se establece en cero.
2. Se mantiene un conjunto de vértices **no procesados**.
3. En cada paso, se selecciona el vértice no procesado con la **menor distancia temporal** (elección voraz).
4. Se actualizan las distancias a los vecinos si se encuentra un camino más corto a través del vértice seleccionado.
5. El vértice se marca como procesado.
6. El proceso se repite hasta procesar todos los vértices.

### Propiedades:

- **Subestructura óptima**: El camino más corto desde el origen hasta cualquier vértice pasa por caminos más cortos intermedios.
- **Elección voraz**: Seleccionar siempre el nodo con la menor distancia provisional lleva a una solución global óptima.

El algoritmo tiene una complejidad de **O(n²)** con matrices de adyacencia, y puede optimizarse a **O((n + m) log n)** usando colas de prioridad con montículos (heaps), donde `n` es el número de vértices y `m` el número de aristas.

## Comparación con Otros Algoritmos

- **Bellman-Ford** también encuentra caminos mínimos desde un solo origen y puede manejar pesos negativos, pero no es voraz y es menos eficiente que Dijkstra cuando los pesos son todos positivos.
- **Floyd-Warshall** resuelve el problema de caminos mínimos entre **todos los pares de vértices**, pero no es un algoritmo voraz.

## Aplicaciones

- Sistemas de navegación GPS.
- Redes de telecomunicaciones (optimización de rutas).
- Planeamiento de trayectorias en videojuegos y robótica.
- Análisis de grafos urbanos y de redes sociales.

## Limitaciones

El algoritmo de Dijkstra **no funciona correctamente si el grafo contiene aristas con pesos negativos**, ya que puede pasar por alto rutas más baratas que solo se vuelven evidentes tras revisar aristas negativas.

## Conclusión

El subtema de caminos mínimos dentro de los algoritmos voraces demuestra cómo, en presencia de ciertas condiciones (pesos no negativos y estructura adecuada), las decisiones locales óptimas pueden conducir a soluciones globalmente óptimas. El **algoritmo de Dijkstra** es un ejemplo paradigmático del éxito del enfoque voraz en el dominio de los grafos, siendo eficiente, confiable y ampliamente utilizado.

---

> **Referencia:**  
> Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.

