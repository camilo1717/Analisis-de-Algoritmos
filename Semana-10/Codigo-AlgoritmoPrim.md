```java 
package ec.edu.utpl.carreras.computacion.proava.clases.s1;

import java.util.*;

public class ArbolRecubrimientoMinimo {

    public static void main(String[] args) {
        Grafo grafo = new Grafo(6); // nodos de 0 a 5 (equivale a 1 a 6)

        // Agrega las aristas con pesos correctos
        grafo.agregarArista(0, 1, 6);  // 1-2
        grafo.agregarArista(0, 2, 1);  // 1-3
        grafo.agregarArista(0, 3, 5);  // 1-4
        grafo.agregarArista(1, 2, 5);  // 2-3
        grafo.agregarArista(1, 4, 3);  // 2-5
        grafo.agregarArista(2, 3, 5);  // 3-4
        grafo.agregarArista(2, 5, 4);  // 3-6
        grafo.agregarArista(3, 5, 2);  // 4-6
        grafo.agregarArista(4, 5, 6);  // 5-6

        grafo.prim();
    }

    static class Arista implements Comparable<Arista> {
        int origen, destino, peso;

        Arista(int origen, int destino, int peso) {
            this.origen = origen;
            this.destino = destino;
            this.peso = peso;
        }

        @Override
        public int compareTo(Arista otra) {
            return Integer.compare(this.peso, otra.peso);
        }

        @Override
        public String toString() {
            return "(" + (origen + 1) + " - " + (destino + 1) + ") peso: " + peso;
        }
    }

    static class Grafo {
        int V;
        List<List<Arista>> ady;

        Grafo(int V) {
            this.V = V;
            ady = new ArrayList<>();
            for (int i = 0; i < V; i++) {
                ady.add(new ArrayList<>());
            }
        }

        void agregarArista(int u, int v, int peso) {
            ady.get(u).add(new Arista(u, v, peso));
            ady.get(v).add(new Arista(v, u, peso)); // grafo no dirigido
        }

        void prim() {
            boolean[] visitado = new boolean[V];
            PriorityQueue<Arista> cola = new PriorityQueue<>();
            List<Arista> mst = new ArrayList<>();

            visitado[0] = true; // nodo 1 (índice 0)
            cola.addAll(ady.get(0));

            while (!cola.isEmpty()) {
                Arista arista = cola.poll();

                if (visitado[arista.destino]) continue;

                mst.add(arista);
                visitado[arista.destino] = true;

                for (Arista siguiente : ady.get(arista.destino)) {
                    if (!visitado[siguiente.destino]) {
                        cola.add(siguiente);
                    }
                }
            }

            System.out.println("Árbol de recubrimiento mínimo (Prim):");
            int total = 0;
            for (Arista a : mst) {
                System.out.println(a);
                total += a.peso;
            }
            System.out.println("Peso total del árbol: " + total);
        }
    }
}
```
