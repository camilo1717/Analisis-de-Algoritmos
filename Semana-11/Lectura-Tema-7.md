# Tema 7: Divide y Vencerás (Brassard & Bratley, 2006)

## Introducción

**Divide y Vencerás** es una estrategia algorítmica que consiste en **dividir** un problema en subproblemas más pequeños, resolver cada uno de ellos de manera independiente (generalmente de forma recursiva) y luego **combinar** sus soluciones para formar una solución al problema completo.

Brassard y Bratley destacan que esta técnica se basa en la idea de que es más fácil resolver muchos problemas simples que uno complejo. Esta filosofía permite reducir la complejidad del problema original y aplicar soluciones elegantes y eficientes.

## Estructura de la Técnica

1. **Dividir**: El problema se fragmenta en subproblemas más pequeños del mismo tipo.
2. **Resolver (Conquistar)**: Si los subproblemas son triviales, se resuelven directamente. Si no, se aplica recursivamente el mismo enfoque.
3. **Combinar**: Se reúnen las soluciones de los subproblemas para construir la solución completa.

## Ejemplos de Aplicación

- **Ordenamiento por mezcla (Merge Sort)**: Se divide el arreglo en mitades, se ordenan recursivamente y se combinan.
- **Ordenamiento rápido (Quick Sort)**: El arreglo se divide en función de un pivote, y se ordenan ambas partes por separado.
- **Multiplicación de matrices grandes**: Dividir matrices en bloques más pequeños para una multiplicación más eficiente.
- **Algoritmos geométricos**: Como la búsqueda del par de puntos más cercanos en un plano.

## Análisis del Tiempo de Ejecución

El tiempo de ejecución de un algoritmo de Divide y Vencerás puede describirse mediante relaciones de recurrencia. Por ejemplo:

T(n) = 2T(n/2) + cn


En este caso, el costo total de dividir y combinar es lineal, y se puede resolver la recurrencia usando técnicas estándar o el Teorema Maestro, llegando a una complejidad de **O(n log n)**, como en el caso de Merge Sort.

## Consideraciones

- **Eficiencia**: Esta técnica mejora notablemente el rendimiento comparado con métodos iterativos o de fuerza bruta.
- **Simplicidad estructural**: Facilita la expresión recursiva de la solución.
- **Versatilidad**: Puede aplicarse a una gran variedad de problemas computacionales.

## Conclusión

Divide y Vencerás es una técnica clásica y poderosa en la construcción de algoritmos. Su simplicidad, eficiencia y aplicabilidad a diversos dominios hacen que sea una herramienta esencial en el repertorio de diseño algorítmico.

---

> **Referencia**:  
> Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.

