```java
package ec.edu.utpl.carreras.computacion.proava.clases.s1;

import java.util.*;

public class AlgoritmoDijkstra {

    public static void main(String[] args) {
        // Construcción del grafo dirigido con pesos
        agregarArista(1, 2, 10);
        agregarArista(1, 4, 30);
        agregarArista(1, 5, 100);
        agregarArista(2, 3, 50);
        agregarArista(3, 5, 10);
        agregarArista(4, 3, 20);
        agregarArista(4, 5, 60);

        int inicio = 1;
        int destino = 5;

        ejecutarDijkstra(inicio);
        System.out.println("Camino seguido: " + obtenerCamino(destino));
        System.out.println("Distancia mínima de " + inicio + " a " + destino + ": " + distancia.get(destino));
    }

    // Clase que representa una arista en el grafo
    static class Arista {
        int destino, peso;
        public Arista(int destino, int peso) {
            this.destino = destino;
            this.peso = peso;
        }
    }

    // Clase para los nodos en la cola de prioridad
    static class Nodo implements Comparable<Nodo> {
        int id, distancia;
        public Nodo(int id, int distancia) {
            this.id = id;
            this.distancia = distancia;
        }

        public int compareTo(Nodo otro) {
            return Integer.compare(this.distancia, otro.distancia);
        }
    }

    // Estructuras del grafo
    static Map<Integer, List<Arista>> grafo = new HashMap<>();
    static Map<Integer, Integer> distancia = new HashMap<>();
    static Map<Integer, Integer> anterior = new HashMap<>();

    // Función para agregar aristas dirigidas al grafo
    public static void agregarArista(int desde, int hasta, int peso) {
        grafo.computeIfAbsent(desde, clave -> new ArrayList<>()).add(new Arista(hasta, peso));
    }

    // Función que ejecuta el algoritmo de Dijkstra
    public static void ejecutarDijkstra(int origen) {
        PriorityQueue<Nodo> cola = new PriorityQueue<>();

        for (Integer nodo : grafo.keySet()) {
            distancia.put(nodo, Integer.MAX_VALUE);
            anterior.put(nodo, null);
        }

        distancia.put(origen, 0);
        cola.add(new Nodo(origen, 0));

        while (!cola.isEmpty()) {
            Nodo actual = cola.poll();
            if (!grafo.containsKey(actual.id)) continue;

            for (Arista arista : grafo.get(actual.id)) {
                int nuevaDistancia = distancia.get(actual.id) + arista.peso;
                if (nuevaDistancia < distancia.getOrDefault(arista.destino, Integer.MAX_VALUE)) {
                    distancia.put(arista.destino, nuevaDistancia);
                    anterior.put(arista.destino, actual.id);
                    cola.add(new Nodo(arista.destino, nuevaDistancia));
                }
            }
        }
    }

    // Función para reconstruir el camino mínimo desde el nodo origen
    public static List<Integer> obtenerCamino(int destino) {
        List<Integer> camino = new ArrayList<>();
        Integer actual = destino;
        while (actual != null) {
            camino.add(actual);
            actual = anterior.get(actual);
        }
        Collections.reverse(camino);
        return camino;
    }

```
