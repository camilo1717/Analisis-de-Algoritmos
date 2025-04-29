```java
public static void main(String[] args) {
        int[] arreglo = { 12, 7, 9, 3, 15, 8 };

        System.out.println("Antes del merge:");
        imprimirArreglo(arreglo);

        // merge de la primera mitad [0..2] y segunda mitad [3..5]
        merge(arreglo, 0, 2, 5);

        System.out.println("Después del merge:");
        imprimirArreglo(arreglo);
    }

    // Método auxiliar para imprimir el arreglo
    public static void imprimirArreglo(int[] arr) {
        for (int valor : arr) {
            System.out.print(valor + " ");
        }
        System.out.println();
    }
}
public class MergeExample {

    // Método merge
    public static void merge(int[] a, int p, int q, int r) {
        int i = p;
        int j = q + 1;
        int k = 0;
        int[] b = new int[r - p + 1]; // arreglo temporal

        while (i <= q && j <= r) {
            if (a[i] <= a[j]) {
                b[k++] = a[i++];
            } else {
                b[k++] = a[j++];
            }
        }

        while (i <= q) {
            b[k++] = a[i++];
        }

        while (j <= r) {
            b[k++] = a[j++];
        }

        for (i = p, k = 0; i <= r; i++, k++) {
            a[i] = b[k];
        }
    }
```
