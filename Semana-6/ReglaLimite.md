# Análisis de Complejidad Asintótica

## Parte 1: Comprobar si  
**\( f(n) = n^3 + 9n^2\log(n) \in O(g(n)) \)**  
con  
**\( g(n) = n^2 \log(n) \)**

### Evaluación del límite:
\[
\lim_{n \to \infty} \frac{f(n)}{g(n)} =
\frac{n^3 + 9n^2\log(n)}{n^2\log(n)} =
\frac{n^3}{n^2\log(n)} + \frac{9n^2\log(n)}{n^2\log(n)} =
\frac{n}{\log(n)} + 9
\]

### Conclusión:
\[
\lim_{n \to \infty} \left( \frac{n}{\log(n)} + 9 \right) = \infty \Rightarrow f(n) \notin O(g(n))
\]

---

## Parte 2: Comprobar si  
**\( f(n) \in O(n^2) \)**

### Evaluación:
\[
\lim_{n \to \infty} \frac{f(n)}{n^2} =
\frac{n^3 + 9n^2\log(n)}{n^2} =
n + 9\log(n)
\]

### Conclusión:
\[
\lim_{n \to \infty} (n + 9\log(n)) = \infty \Rightarrow f(n) \notin O(n^2)
\]

---

## Parte 3: Comparación entre funciones exponenciales

Sean:
- \( f(n) = 2^n \)
- \( g(n) = 2^{2n} = 4^n \)

### Verificar si \( f(n) \in O(g(n)) \):

\[
\frac{f(n)}{g(n)} = \frac{2^n}{4^n} = \frac{2^n}{(2^2)^n} = \frac{2^n}{2^{2n}} = 2^{-n}
\]

\[
\lim_{n \to \infty} 2^{-n} = 0 \Rightarrow f(n) \in O(g(n))
\]

---

### Verificar si \( g(n) \in O(f(n)) \):

\[
\frac{g(n)}{f(n)} = \frac{4^n}{2^n} = 2^n
\]

\[
\lim_{n \to \infty} 2^n = \infty \Rightarrow g(n) \notin O(f(n))
\]

---

## Resumen

| Relación                   | Resultado        | Justificación                                          |
|---------------------------|------------------|--------------------------------------------------------|
| \( f(n) \in O(g(n)) \)     | ❌ No             | \( f(n) \) crece más rápido que \( g(n) \)            |
| \( f(n) \in O(n^2) \)      | ❌ No             | Cociente tiende a infinito                             |
| \( 2^n \in O(4^n) \)       | ✅ Sí             | Cociente tiende a 0                                    |
| \( 4^n \in O(2^n) \)       | ❌ No             | Cociente tiende a infinito                             |

