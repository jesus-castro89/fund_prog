# La programación Módular

La programación modular es un enfoque de diseño de software que consiste en dividir un programa en módulos o unidades
funcionales independientes. Cada módulo se encarga de realizar una tarea específica y se comunica con otros módulos a
través de interfaces bien definidas.

## Ventajas de la Programación Modular

Algunas de las ventajas de la programación modular son:

* **Facilidad de Mantenimiento**: Al dividir un programa en módulos independientes, es más fácil realizar cambios y
  actualizaciones en el código sin afectar otras partes del programa.
* **Reutilización de Código**: Los módulos pueden ser reutilizados en diferentes programas o proyectos, lo que ahorra
  tiempo y esfuerzo en el desarrollo de software.
* **Facilidad de Depuración**: Al tener módulos independientes, es más sencillo identificar y corregir errores en el
  código.
* **Escalabilidad**: Los módulos pueden ser agregados o eliminados según sea necesario, lo que facilita la
  escalabilidad del programa.
* **Facilidad de Colaboración**: Varios programadores pueden trabajar en diferentes módulos de forma simultánea, lo que
  acelera el desarrollo del software.
* **Abstracción**: Los módulos permiten ocultar los detalles de implementación y exponer una interfaz clara y sencilla
  para interactuar con el resto del programa.

## Ejemplo de Programación Modular en Java

A continuación se muestra un ejemplo sencillo de programación modular en Java:

En este ejemplo tendremos el paquete `programacion` con dos módulos: `Calculadora` y `Main`. El módulo `Calculadora`
contiene la lógica para realizar operaciones matemáticas, mientras que el módulo `Main` se encarga de interactuar con
el usuario y llamar a los métodos de la calculadora.

### Estructura de Directorios

```
src
└── programacion
    ├── Calculadora.java
    └── Main.java
```

### Código Fuente

#### `Calculadora.java`

```java
package programacion;

public class Calculadora {
    public static int sumar(int a, int b) {
        return a + b;
    }

    public static int restar(int a, int b) {
        return a - b;
    }

    public static int multiplicar(int a, int b) {
        return a * b;
    }

    public static int dividir(int a, int b) {
        return a / b;
    }
}
```

#### `Main.java`

```java
package programacion;

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el primer número: ");
        int a = scanner.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int b = scanner.nextInt();

        System.out.println("Suma: " + Calculadora.sumar(a, b));
        System.out.println("Resta: " + Calculadora.restar(a, b));
        System.out.println("Multiplicación: " + Calculadora.multiplicar(a, b));
        System.out.println("División: " + Calculadora.dividir(a, b));
    }
}
```

En este ejemplo, el módulo `Calculadora` contiene los métodos para realizar operaciones matemáticas, mientras que el
módulo `Main` interactúa con el usuario para obtener los números de entrada y mostrar los resultados de las operaciones.

La programación modular es una técnica poderosa que facilita el diseño, desarrollo y mantenimiento de software. Al
dividir un programa en módulos independientes, se mejora la legibilidad, reutilización y escalabilidad del código,
permitiendo a los programadores trabajar de forma más eficiente y colaborativa.