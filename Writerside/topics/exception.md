# Excepciones

Una excepción es un error que ocurre durante la ejecución de un programa. Cuando se produce una excepción, el programa
se detiene y Java lanza una excepción.

Para manejar las excepciones, se utilizan bloques `try-catch`. En el bloque `try`, se coloca el código que puede
lanzar una excepción, y en el bloque `catch`, se captura la excepción y se maneja.

## Tipos de excepciones

Existen varios tipos de excepciones en Java, entre los que se encuentran:

- **Checked exceptions**: son excepciones que se comprueban en tiempo de compilación. El programador debe manejarlas
  utilizando bloques `try-catch` o lanzarlas con la palabra clave `throws`.
- **Unchecked exceptions**: son excepciones que no se comprueban en tiempo de compilación. El programador no está
  obligado a manejarlas, pero si no lo hace, el programa se detendrá.
- **Errores**: son excepciones que no se deben manejar, ya que indican problemas graves en el sistema.
- **Excepciones personalizadas**: son excepciones creadas por el programador para manejar situaciones específicas.

## Bloques `try-catch`

Los bloques `try-catch` se utilizan para manejar excepciones en Java. En el bloque `try`, se coloca el código que
puede lanzar una excepción, y en el bloque `catch`, se captura la excepción y se maneja.

```java
try {
    // Código que puede lanzar una excepción
} catch (Excepcion e) {
    // Manejo de la excepción
}
```

## Uso simple de excepciones

A continuación, se muestra un ejemplo de cómo manejar una excepción en Java:

```java
public class Main {
    public static void main(String[] args) {
        try {
            int resultado = dividir(10, 0);
            System.out.println("El resultado es: " + resultado);
        } catch (Exception e) {
            System.out.println("Error: división por cero");
        }
    }

    public static int dividir(int numerador, int denominador) {
        return numerador / denominador;
    }
}
```

En este ejemplo, se intenta dividir un número por cero, lo cual lanza una excepción de tipo `ArithmeticException` y
que nosotros manejamos en el bloque `catch` como una excepción genérica `Exception`.

## Usando excepciones para leer datos

Las excepciones también pueden ser útiles para leer datos de entrada del usuario y manejar posibles errores. Por
ejemplo, si se espera un número entero y el usuario ingresa un valor no numérico, se puede lanza una excepción y
manejarla en un bloque `catch`.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            System.out.print("Ingrese un número entero: ");
            int numero = scanner.nextInt();
            System.out.println("El número ingresado es: " + numero);
        } catch (Exception e) {
            System.out.println("Error: el valor ingresado no es un número entero");
        }
    }
}
```

En este ejemplo, se utiliza un objeto `Scanner` para leer un número entero del usuario. Si el usuario ingresa un valor
no numérico, se lanza una excepción y se maneja en el bloque `catch`.

## Conclusión

Las excepciones son una parte importante de la programación en Java, ya que permiten manejar errores de forma
estructurada y controlada. Al utilizar bloques `try-catch`, se pueden capturar y manejar excepciones de manera
adecuada, evitando que el programa se detenga de forma inesperada.