### Algortimos Voraces
Los algoritmos voraces son una estrategia de diseño algorítmico que construye una solución óptima eligiendo de forma iterativa la opción más favorable en cada paso, sin reconsiderar decisiones pasadas. Se basan en tomar decisiones locales óptimas con la esperanza de que lleven a una solución global óptima.

Para que un algoritmo voraz funcione correctamente y garantice una solución óptima, el problema debe cumplir con dos propiedades fundamentales:

Subestructura óptima: Una solución óptima al problema completo contiene soluciones óptimas a sus subproblemas.

Propiedad de elección voraz: Una elección localmente óptima puede conducir a una solución globalmente óptima.

Los algoritmos voraces suelen ser más eficientes en términos de complejidad temporal que otras técnicas como la programación dinámica, pero no siempre garantizan la mejor solución para todos los problemas.

Algunos problemas clásicos que se resuelven correctamente con métodos voraces son:

Cambio de monedas (cuando las denominaciones lo permiten)

Árboles de expansión mínima, usando algoritmos como Prim y Kruskal

Codificación de Huffman, que genera un árbol binario óptimo para compresión

Problema del conjunto de actividades (selección de actividades compatibles en el tiempo)

Sin embargo, no todos los problemas pueden resolverse con esta técnica. Por ejemplo, el problema de la mochila (knapsack problem) en su versión entera no puede ser resuelto óptimamente con un enfoque voraz.

El capítulo enfatiza que antes de aplicar un algoritmo voraz, es fundamental comprobar que el problema cumple las propiedades necesarias, especialmente la de elección voraz, ya que su ausencia puede llevar a soluciones incorrectas.
