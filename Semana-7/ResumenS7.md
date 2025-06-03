/**
 * Tema 3: Notación Asintótica - Brassard & Bratley (2006)
 * Resumen en formato SCSS para GitHub.
 */

// 1. Introducción
$introduccion: (
  descripcion: "La notación asintótica describe el comportamiento límite de funciones (como complejidad de algoritmos) cuando n → ∞.",
  detalles: (
    "Ignora factores constantes (ej. 2n² ≈ n²)",
    "Ignora términos de menor orden (ej. n² + n ≈ n²)"
  )
);

// 2. Notaciones Principales
$notaciones: (
  // a) O-grande (O) → Cota superior (peor caso)
  "O-grande": (
    definicion: "f(n) = O(g(n)) si ∃c > 0, n₀ ≥ 0 tal que 0 ≤ f(n) ≤ c·g(n) ∀n ≥ n₀",
    ejemplo: "3n² + 5n = O(n²)"
  ),

  // b) Ω-grande (Ω) → Cota inferior (mejor caso)
  "Ω-grande": (
    definicion: "f(n) = Ω(g(n)) si ∃c > 0, n₀ ≥ 0 tal que 0 ≤ c·g(n) ≤ f(n) ∀n ≥ n₀",
    ejemplo: "n³ = Ω(n²)"
  ),

  // c) Θ-grande (Θ) → Límite ajustado (caso promedio)
  "Θ-grande": (
    definicion: "f(n) = Θ(g(n)) si f(n) = O(g(n)) y f(n) = Ω(g(n))",
    ejemplo: "n(n-1)/2 = Θ(n²)"
  ),

  // d) o-pequeña (o) y ω-pequeña (ω) → Cotas no ajustadas
  "o-pequeña": (
    definicion: "f(n) = o(g(n)) si lim(n→∞) f(n)/g(n) = 0",
    ejemplo: "n = o(n²)"
  ),
  "ω-pequeña": (
    definicion: "f(n) = ω(g(n)) si lim(n→∞) f(n)/g(n) = ∞",
    ejemplo: "n² = ω(n)"
  )
);

// 3. Propiedades y Reglas
$propiedades: (
  "Transitividad": "Si f = O(g) y g = O(h), entonces f = O(h) (aplica para Ω, Θ, o, ω)",
  "Reflexividad": "f = O(f)",
  "Simetría": "f = Θ(g) ⇔ g = Θ(f)",
  "Regla del máximo": "Si f₁(n) = O(g₁(n)) y f₂(n) = O(g₂(n)), entonces f₁(n) + f₂(n) = O(max(g₁(n), g₂(n)))"
);

// 4. Aplicaciones en Análisis de Algoritmos
$aplicaciones: (
  "Tiempo de ejecución": "Se expresa con O, Ω o Θ. Ejemplo: Algoritmo con bucles anidados = O(n²)",
  "Comparación de algoritmos": "Ejemplo: O(n log n) es mejor que O(n²)"
);

// 5. Limitaciones
$limitaciones: (
  "No captura diferencias constantes": "Ejemplo: 2n vs. 100n",
  "Útil para n grande": "Puede no reflejar rendimiento en entradas pequeñas"
);

// Conclusión
$conclusion: "La notación asintótica es esencial para comparar algoritmos de manera abstracta, clasificándolos por eficiencia para problemas grandes.";
