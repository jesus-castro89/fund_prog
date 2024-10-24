# La clase Random

La clase `Random` de Java se encuentra en el paquete `java.util` y se utiliza para generar números aleatorios. Para
crear un objeto de la clase `Random`, se debe importar el paquete `java.util` y luego instanciar un objeto de la clase
`Random` de la siguiente manera:

```java
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        Random random = new Random();
    }
}
```

## Métodos de la clase `Random`

La clase `Random` tiene varios métodos que permiten generar números aleatorios de diferentes tipos. A continuación, se
presentan algunos de los métodos más comunes de la clase `Random`:

- `nextInt()`: Este método genera un número entero aleatorio.
- `nextDouble()`: Este método genera un número de punto flotante aleatorio entre 0.0 y 1.0.
- `nextBoolean()`: Este método genera un valor booleano aleatorio.
- `nextGaussian()`: Este método genera un número de punto flotante aleatorio con una distribución gaussiana.
- `nextInt(int bound)`: Este método genera un número entero aleatorio entre 0 (inclusive) y el límite especificado (
  exclusivo).
- `nextInt(int origin, int bound)`: Este método genera un número entero aleatorio entre el origen especificado (
  inclusive)
  y el límite especificado (exclusivo).
- `nextLong()`: Este método genera un número largo aleatorio.
- `nextFloat()`: Este método genera un número de punto flotante aleatorio entre 0.0 y 1.0.
- `nextBytes(byte[] bytes)`: Este método genera una secuencia de bytes aleatorios y los almacena en el arreglo
  especificado.
- `doubles()`: Este método genera una secuencia de números de punto flotante aleatorios en un rango específico.
- `ints()`: Este método genera una secuencia de números enteros aleatorios en un rango específico.
- `longs()`: Este método genera una secuencia de números largos aleatorios en un rango específico.

## Función para enteros aleatorios de un rango específico

Para generar un número entero aleatorio en un rango específico, se puede utilizar el método `nextInt(int origin, int
bound)` de la clase `Random`. A continuación, se muestra un ejemplo de cómo generar un número entero aleatorio entre 1 y
100:

```java
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        Random random = new Random();
        int numeroAleatorio = random.nextInt(100) + 1;
        System.out.println("Número aleatorio entre 1 y 100: " + numeroAleatorio);
    }
}
```

En este ejemplo, el método `nextInt(100)` genera un número entero aleatorio entre 0 y 99, y luego se le suma 1 para
obtener un número aleatorio entre 1 y 100.