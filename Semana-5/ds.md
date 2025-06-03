Tema 3: Notación Asintótica
Introducción
En este capítulo, los autores introducen la notación asintótica como una herramienta fundamental para describir y analizar la eficiencia de los algoritmos, especialmente en términos de tiempo de ejecución y uso de recursos, en función del tamaño de la entrada.

Objetivo de la Notación Asintótica
El propósito principal de la notación asintótica es proporcionar una forma de expresar el comportamiento de un algoritmo cuando el tamaño de la entrada tiende a infinito, es decir, su comportamiento en el peor de los casos o en casos límite. Esto permite comparar algoritmos y seleccionar el más eficiente para un problema dado.

Tipos de Notación Asintótica
## Notación O (O grande): Cota superior

Representa una cota superior del tiempo de ejecución de un algoritmo. Formalmente, una función f(n) pertenece a O(g(n)) si existen constantes positivas c y n₀ tales que:

f(n) ≤ c * g(n)  para todo n ≥ n₀

Esto indica que, a partir de un cierto punto, el crecimiento de f(n) no supera a g(n) multiplicada por una constante.

## Notación Ω (Omega): Cota inferior

Representa una cota inferior del tiempo de ejecución. Formalmente, f(n) pertenece a Ω(g(n)) si existen constantes positivas c y n₀ tales que:

f(n) ≥ c * g(n)  para todo n ≥ n₀

Esto significa que, a partir de cierto tamaño de entrada, el algoritmo requiere al menos un tiempo proporcional a g(n).

## Notación Θ (Theta): Cota ajustada

Indica que f(n) está acotada tanto superior como inferiormente por g(n). Formalmente, f(n) pertenece a Θ(g(n)) si existen constantes positivas c₁, c₂ y n₀ tales que:

c₁ * g(n) ≤ f(n) ≤ c₂ * g(n)  para todo n ≥ n₀


Esto implica que f(n) y g(n) crecen al mismo ritmo asintótico.

Ejemplos de Clases de Complejidad
O(1): Tiempo constante. El tiempo de ejecución no depende del tamaño de la entrada.

O(log n): Tiempo logarítmico. Ejemplo: búsqueda binaria.

O(n): Tiempo lineal. Ejemplo: recorrido de una lista.

O(n log n): Tiempo casi lineal. Ejemplo: algoritmos de ordenamiento eficientes como mergesort.

O(n²): Tiempo cuadrático. Ejemplo: algoritmos de ordenamiento simples como bubble sort.

O(2ⁿ): Tiempo exponencial. Ejemplo: resolución de problemas NP-completos por fuerza bruta.

Propiedades de la Notación Asintótica
Transitividad: Si f(n) ∈ O(g(n)) y g(n) ∈ O(h(n)), entonces f(n) ∈ O(h(n)).

Suma: Si f₁(n) ∈ O(g₁(n)) y f₂(n) ∈ O(g₂(n)), entonces f₁(n) + f₂(n) ∈ O(max(g₁(n), g₂(n))).

Producto: Si f₁(n) ∈ O(g₁(n)) y f₂(n) ∈ O(g₂(n)), entonces f₁(n) * f₂(n) ∈ O(g₁(n) * g₂(n)).

Aplicación en el Análisis de Algoritmos
La notación asintótica se utiliza para:

- Evaluar la eficiencia de algoritmos sin depender de implementaciones específicas o hardware.

- Comparar algoritmos que resuelven el mismo problema, identificando cuál es más eficiente en términos de crecimiento del tiempo de ejecución.

- Clasificar problemas según la complejidad de los algoritmos que los resuelven.

**Conclusión:**

La notación asintótica es una herramienta esencial en la informática teórica y práctica, permitiendo un análisis riguroso y abstracto de la eficiencia algorítmica. Su comprensión es fundamental para el diseño y selección de algoritmos eficientes.
