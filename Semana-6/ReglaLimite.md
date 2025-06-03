# Análisis de Complejidad Asintótica

---

Dado: $f(n) = n^3 + 9n^2\log(n))$ y $g(n) = n^2\log(n)$
* Comprobar $f(n) \in O(g(n))$
* Comprobar $f(n) \notin O(n^2)$
  
## Parte 1: Comprobar si `f(n) ∈ O(g(n))`

### Dados:
- `f(n) = n³ + 9n² log(n)`
- `g(n) = n² log(n)`

### Límite:


Como `lim n→∞ (n / log(n)) = ∞`, entonces:

❌ **f(n) ∉ O(g(n))**

---

## ❌ Parte 2: Comprobar si `f(n) ∈ O(n²)`

### Límite:


📈 Como `lim n→∞ (n + 9 log(n)) = ∞`, entonces:

❌ **f(n) ∉ O(n²)**

---

## Parte 3: Comparación entre funciones exponenciales

### Sean:
- `f(n) = 2ⁿ`
- `g(n) = 4ⁿ = 2²ⁿ`

---

### Verificar si `f(n) ∈ O(g(n))`

Como el límite tiende a 0, **f(n) ∈ O(g(n))**

---

### Verificar si `g(n) ∈ O(f(n))`

❌ Como el límite tiende a ∞, **g(n) ∉ O(f(n))**

---

## Resumen

| Relación                        | Resultado | Justificación                            |
|--------------------------------|-----------|------------------------------------------|
| `f(n) ∈ O(g(n))`               | ❌ No     | f(n) crece más rápido que g(n)           |
| `f(n) ∈ O(n²)`                 | ❌ No     | El cociente tiende a infinito            |
| `2ⁿ ∈ O(4ⁿ)`                   | ✅ Sí     | El cociente tiende a 0                   |
| `4ⁿ ∈ O(2ⁿ)`                   | ❌ No     | El cociente tiende a infinito            |

---

📘 **Nota**: Big O (`O(g(n))`) representa una cota superior del crecimiento de una función. Si `f(n) ∈ O(g(n))`, entonces `f(n)` no crece más rápido que `g(n)` hasta una constante multiplicativa.



