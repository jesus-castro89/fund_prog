# Menús de interacción y excepciones

## Introducción

Los menús de interacción son una forma común de presentar opciones al usuario y permitirle seleccionar una acción
específica. Estos menús pueden ser utilizados en diferentes tipos de aplicaciones, como programas de consola,
aplicaciones de escritorio o aplicaciones web.

Por otro lado, las excepciones son errores que pueden ocurrir durante la ejecución de un programa y que deben ser
manejados adecuadamente para evitar que el programa se detenga de forma inesperada. En Java, las excepciones se manejan
utilizando bloques `try-catch` que permiten capturar y manejar los errores de forma controlada.

En este artículo, exploraremos cómo crear menús de interacción en Java y cómo manejar excepciones para garantizar un
funcionamiento correcto y robusto de nuestras aplicaciones Java.

## Creación de menús de interacción

Los menús de interacción son una forma efectiva de presentar opciones al usuario y permitirle seleccionar una acción
específica. En Java, los menús de interacción se pueden implementar utilizando estructuras de control como `if-else` o
`switch-case`, combinados con la entrada de datos del usuario a través de la consola o en nuestro caso, ventanas
emergentes.

A continuación, se muestra un ejemplo:

```java
import javax.swing.JOptionPane;

public class MenuInteractivo {
    public static void main(String[] args) {
        int opcion = 0;

        do {
            opcion = Integer.parseInt(JOptionPane.showInputDialog("Menú de opciones\n1. Opción 1\n2. Opción 2\n3. Salir"));

            switch (opcion) {
                case 1:
                    JOptionPane.showMessageDialog(null, "Ha seleccionado la opción 1");
                    break;
                case 2:
                    JOptionPane.showMessageDialog(null, "Ha seleccionado la opción 2");
                    break;
                case 3:
                    JOptionPane.showMessageDialog(null, "Saliendo del programa");
                    break;
                default:
                    JOptionPane.showMessageDialog(null, "Opción inválida");
            }
        } while (opcion != 3);
    }
}
```

En este ejemplo, se utiliza un bucle `do-while` para mostrar un menú de opciones al usuario y permitirle seleccionar
una acción. Dependiendo de la opción seleccionada, se muestra un mensaje correspondiente utilizando la clase
`JOptionPane` de Java.

## Manejo de excepciones

Como ya se ha mencionado en otros apartados, es posible que ocurran errores durante la ejecución de un programa, como
la selección de un dato incorrecto en un menú de interacción o la inserción de un valor no numérico donde se espera un
número. Esta es una situación común en la programación y es importante manejar estas excepciones de forma adecuada para
evitar que el programa se detenga de forma inesperada.

Tomando entonces el ejemplo anterior, podemos agregar un bloque `try-catch` para manejar posibles excepciones al
convertir la entrada del usuario a un número entero:

```java
import javax.swing.JOptionPane;

public class MenuInteractivo {
    public static void main(String[] args) {
        int opcion = 0;

        do {
            try {
                opcion = Integer.parseInt(JOptionPane.showInputDialog("Menú de opciones\n1. Opción 1\n2. Opción 2\n3. Salir"));
            } catch (NumberFormatException e) {
                JOptionPane.showMessageDialog(null, "Error: ingrese un número válido");
                continue;
            }

            switch (opcion) {
                case 1:
                    JOptionPane.showMessageDialog(null, "Ha seleccionado la opción 1");
                    break;
                case 2:
                    JOptionPane.showMessageDialog(null, "Ha seleccionado la opción 2");
                    break;
                case 3:
                    JOptionPane.showMessageDialog(null, "Saliendo del programa");
                    break;
                default:
                    JOptionPane.showMessageDialog(null, "Opción inválida");
            }
        } while (opcion != 3);
    }
}
```

En este caso, se utiliza un bloque `try-catch` para capturar la excepción `NumberFormatException` que se lanza cuando
la entrada del usuario no puede ser convertida a un número entero. Si se produce esta excepción, se muestra un mensaje
de error y se continúa con la ejecución del programa.

## Conclusión

Los menús de interacción y el manejo de excepciones son elementos importantes en el desarrollo de aplicaciones Java,
ya que permiten interactuar con el usuario de forma efectiva y manejar posibles errores de forma controlada. Al
utilizar estructuras de control como `if-else` o `switch-case` para crear menús de interacción y bloques `try-catch`
para manejar excepciones, podemos garantizar un funcionamiento correcto y robusto de nuestras aplicaciones Java.

En resumen, los menús de interacción y el manejo de excepciones son herramientas fundamentales para crear aplicaciones
Java que sean fáciles de usar y que ofrezcan una experiencia de usuario satisfactoria.