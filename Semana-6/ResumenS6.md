## 4.2 Análisis de las estructuras de control

Este apartado se centra en el impacto de las estructuras de control (como condicionales, bucles y bloques secuenciales) sobre la eficiencia computacional de los algoritmos. Se analiza cómo el comportamiento temporal de un algoritmo está influenciado directamente por estas estructuras, y se establece una base para evaluar su complejidad en el peor caso, caso promedio y mejor caso.

El capítulo descompone el análisis en componentes básicos:

**Secuencias:**

La complejidad es la suma de las operaciones individuales.

**Condicionales (if-else):**

Se evalúan distintas ramas según su probabilidad y su costo.

**Bucles (for, while):** 

Se consideran el número de iteraciones y el costo de cada una. En bucles anidados, la complejidad se multiplica según los niveles de anidamiento.

El análisis se complementa con ejemplos que muestran cómo pequeñas diferencias en la estructura de control pueden cambiar drásticamente la eficiencia. También se introduce la notación asintótica como herramienta clave para expresar estos análisis, destacando la importancia del crecimiento del tiempo de ejecución respecto al tamaño del problema.
