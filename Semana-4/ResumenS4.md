## Tema 3: Characterizing Running Time

Cormet et al., 2022 – "Algorithms Unlocked" o textos similares

Este tema se centra en cómo medir y describir el tiempo de ejecución de un algoritmo de manera precisa y general, sin depender exclusivamente de implementaciones o plataformas específicas.

Puntos clave:

Tiempo real vs. modelo teórico: Aunque los algoritmos se ejecutan en computadoras físicas, el análisis de su tiempo de ejecución se realiza mediante modelos teóricos que abstraen detalles del hardware.

Input size (tamaño de entrada): El tiempo de ejecución se estudia en función del tamaño de la entrada, comúnmente representado como n. No se mide con entradas específicas, sino con la cantidad de datos.

Unidades de tiempo abstractas: Se usan operaciones básicas (comparaciones, asignaciones, etc.) como "unidades" en lugar de segundos. Esto permite comparar algoritmos en términos relativos, independientemente del lenguaje de programación o computadora.

Mediciones empíricas vs. análisis asintótico: Si bien se pueden hacer pruebas experimentales para medir el rendimiento, se prefiere el análisis asintótico para estimar el comportamiento general con entradas grandes.

Peor caso, mejor caso y caso promedio:

Peor caso (worst-case): Garantiza que el tiempo de ejecución nunca será peor que cierta función.

Mejor caso: Útil, pero menos relevante en la práctica.

Caso promedio: Estima el comportamiento esperado, aunque es más complejo de calcular.

Importancia del análisis independiente de la implementación: Esto permite evaluar la eficiencia y escalabilidad de algoritmos de forma general.

## Tema 3: Notación Asintótica

Brassard & Bratley, 2006 – "Fundamentals of Algorithmics"

Este tema introduce formalmente las herramientas matemáticas para describir el tiempo (y espacio) de ejecución de algoritmos mediante funciones que expresan su crecimiento.

Puntos clave:
Motivación: Se busca clasificar algoritmos según la velocidad con que crece su tiempo de ejecución en relación con el tamaño de la entrada.

Notación O (mayor orden de magnitud):

Describe una cota superior.

Si un algoritmo tiene tiempo O(n²), significa que su ejecución toma como máximo tiempo proporcional a n².

Notación Ω (cota inferior):

Describe el tiempo mínimo que el algoritmo requiere.

Ejemplo: Un algoritmo tiene tiempo Ω(n) si siempre toma al menos tiempo proporcional a n.

Notación Θ (cota ajustada):

Significa que el tiempo de ejecución está acotado superior e inferiormente por la misma función.

Si un algoritmo es Θ(n log n), ni puede ser más rápido ni más lento (asintóticamente) que eso.

Ejemplos comparativos:

O(1): Tiempo constante

O(log n): Logarítmico

O(n): Lineal

O(n²): Cuadrático

O(2ⁿ): Exponencial

O(n!): Factorial

Utilidad práctica: La notación asintótica permite seleccionar el algoritmo más eficiente según el problema, especialmente con entradas grandes, donde pequeñas diferencias se amplifican enormemente.

## Conclusión:
Ambos textos convergen en que el análisis de algoritmos no debe depender de pruebas empíricas aisladas, sino de modelos teóricos generales, donde el crecimiento del tiempo de ejecución en función del tamaño de entrada es el criterio central. La notación asintótica es una herramienta poderosa para expresar esto, y permite comparar algoritmos más allá de casos particulares.

Si quieres ver ejemplos con gráficos o pseudocódigo de distintos casos de notación O, puedo ayudarte con un resumen visual, o si prefieres, con ejercicios prácticos para afianzar la comprensión.
