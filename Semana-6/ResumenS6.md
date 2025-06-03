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


En esta sección, los autores abordan cómo analizar el tiempo de ejecución de algoritmos a través del estudio de las estructuras de control fundamentales: secuencias, condicionales y bucles. El análisis se basa principalmente en determinar la complejidad temporal, es decir, cómo crece el tiempo de ejecución en función del tamaño de entrada.

1. Secuencias:
Cuando un algoritmo ejecuta instrucciones una tras otra, la complejidad total es simplemente la suma de los tiempos de cada instrucción. Por ejemplo, si hay tres operaciones con complejidades 
𝑇
1
(
𝑛
)
,
𝑇
2
(
𝑛
)
,
𝑇
3
(
𝑛
)
T 
1
​
 (n),T 
2
​
 (n),T 
3
​
 (n), la complejidad total es 
𝑇
(
𝑛
)
=
𝑇
1
(
𝑛
)
+
𝑇
2
(
𝑛
)
+
𝑇
3
(
𝑛
)
T(n)=T 
1
​
 (n)+T 
2
​
 (n)+T 
3
​
 (n). En notación asintótica, se conserva solo el término dominante.

2. Condicionales (if-else):
Para estructuras de decisión, el tiempo de ejecución depende de la rama que se tome. Se analiza cada posible camino y se determina cuál tiene el mayor costo, especialmente en el análisis del peor caso. Si las ramas tienen diferentes complejidades, se elige la más costosa:
𝑇
(
𝑛
)
=
max
⁡
{
𝑇
true
(
𝑛
)
,
𝑇
false
(
𝑛
)
}
T(n)=max{T 
true
​
 (n),T 
false
​
 (n)}
En algunos casos también se analiza el caso promedio, considerando la probabilidad de cada camino.

3. Bucles:
Los bucles son más complejos de analizar, ya que implican múltiples repeticiones. Se debe considerar:

El número de iteraciones del bucle.

El costo de las operaciones dentro del bucle.

Por ejemplo, un bucle que ejecuta una operación de complejidad 
𝑂
(
1
)
O(1) 
𝑛
n veces, tiene complejidad 
𝑂
(
𝑛
)
O(n). Si el bucle contiene otro bucle anidado, la complejidad puede crecer a 
𝑂
(
𝑛
2
)
O(n 
2
 ) o más.

4. Bucles anidados:
Son casos donde uno o más bucles están dentro de otros. Se calcula el producto de las iteraciones. Por ejemplo, dos bucles anidados que cada uno itera 
𝑛
n veces dan una complejidad de 
𝑂
(
𝑛
⋅
𝑛
)
=
𝑂
(
𝑛
2
)
O(n⋅n)=O(n 
2
 ).

5. Relevancia de la notación asintótica:
El análisis de estructuras de control utiliza la notación asintótica (como O, Ω, Θ) para describir el comportamiento del algoritmo a gran escala. Esto permite comparar algoritmos y prever su desempeño cuando se enfrentan a entradas grandes.

En resumen, esta sección proporciona las bases para estimar la eficiencia algorítmica desde su estructura lógica. Entender cómo cada estructura de control afecta la complejidad es clave para diseñar soluciones eficientes.
