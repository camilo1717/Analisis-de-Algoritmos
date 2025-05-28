## Código Fibonacci

```Java
public class Fibonacci {

    // Método recursivo para calcular Fibonacci
    public static int fibonacci(int n) {
        if (n <= 1) return n;
        return fibonacci(n - 1) + fibonacci(n - 2);
    }

    // Prueba del método
    public static void main(String[] args) {
        int n = 10; 
        for (int i = 0; i <= n; i++) {
            System.out.print(fibonacci(i) + " ");
        }
    }
}
```
## Identificar las Recurrencias:

La recurrencia del algoritmo de Fibonacci es:

**T(n) = T(n−1) + T(n−2) + O(1)**
                             
esto es debido a que, por cada llamada a fibonacci(n) realiza dos llamadas recursivas: fibonacci(n-1) y fibonacci(n-2)

## Obtener la Ecuación General y Comprobar:

![WhatsApp Image 2025-05-27 at 23 36 01](https://github.com/user-attachments/assets/e5c8f8f2-2ef1-4647-8840-646726a24a57)

