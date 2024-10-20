# Menú de opciones con JOptionPane en Java

En Java, la clase `JOptionPane` proporciona una forma sencilla de mostrar cuadros de diálogo con diferentes tipos de
mensajes y opciones. Uno de los usos más comunes de `JOptionPane` es la creación de un menú de opciones para que el
usuario seleccione una de ellas.

## Creación de un Menú de Opciones

Para crear un menú de opciones con `JOptionPane` en Java, se pueden utilizar los métodos `showInputDialog()` y
`showOptionDialog()`. Por ejemplo, para mostrar un menú de opciones con tres botones (`Sí`, `No` y `Cancelar`):

```java
int opcion = JOptionPane.showOptionDialog(null, "¿Desea continuar?", "Confirmación",
        JOptionPane.YES_NO_CANCEL_OPTION, JOptionPane.QUESTION_MESSAGE, null,
        new String[]{"Sí", "No", "Cancelar"}, "Sí");

switch (opcion) {
    case JOptionPane.YES_OPTION:
        System.out.println("Ha seleccionado Sí");
        break;
    case JOptionPane.NO_OPTION:
        System.out.println("Ha seleccionado No");
        break;
    case JOptionPane.CANCEL_OPTION:
        System.out.println("Ha seleccionado Cancelar");
        break;
    default:
        System.out.println("Ha cerrado el cuadro de diálogo");
        break;
}
```

En este ejemplo, se muestra un cuadro de diálogo con la pregunta "¿Desea continuar?" y tres botones (`Sí`, `No` y
`Cancelar`). Dependiendo de la opción seleccionada por el usuario, se imprime un mensaje en la consola.

## Opciones Personalizadas

Además de los botones predefinidos (`Sí`, `No` y `Cancelar`), es posible personalizar las opciones del menú de
opciones con `showOptionDialog()`. Por ejemplo, para mostrar un menú de opciones con dos botones personalizados:

```java
int opcion = JOptionPane.showOptionDialog(null, "Seleccione una opción", "Menú de Opciones",
        JOptionPane.DEFAULT_OPTION, JOptionPane.QUESTION_MESSAGE, null,
        new String[]{"Opción 1", "Opción 2"}, "Opción 1");

switch (opcion) {
    case 0:
        System.out.println("Ha seleccionado Opción 1");
        break;
    case 1:
        System.out.println("Ha seleccionado Opción 2");
        break;
    default:
        System.out.println("Ha cerrado el cuadro de diálogo");
        break;
}
```

En este caso, se muestra un cuadro de diálogo con la pregunta "Seleccione una opción" y dos botones personalizados
(`Opción 1` y `Opción 2`). Dependiendo de la opción seleccionada por el usuario, se imprime un mensaje en la consola.

## Menú con multiples opciones

Para mostrar un menú de opciones y solo un elemento de entrada, se puede utilizar `showInputDialog()`. Por ejemplo, para
mostrar un menú de opciones con tres opciones y un campo de texto para ingresar un valor:

```java
String[] opciones = {"Opción 1", "Opción 2", "Opción 3"};
String opcionSeleccionada = (String) JOptionPane.showInputDialog(null, "Seleccione una opción", "Menú de Opciones",
        JOptionPane.QUESTION_MESSAGE, null, opciones, opciones[0]);

if (opcionSeleccionada != null) {
    System.out.println("Ha seleccionado: " + opcionSeleccionada);
    switch (opcionSeleccionada) {
        case "Opción 1":
            // Acción para la opción 1
            break;
        case "Opción 2":
            // Acción para la opción 2
            break;
        case "Opción 3":
            // Acción para la opción 3
            break;
    }
} else {
    System.out.println("Ha cerrado el cuadro de diálogo");
}
```

En este ejemplo, se muestra un menú de opciones con tres opciones (`Opción 1`, `Opción 2` y `Opción 3`) y un campo de
texto para ingresar un valor. Dependiendo de la opción seleccionada por el usuario, se imprime un mensaje en la consola
y se ejecuta una acción específica para cada opción.

## Conclusión

Los cuadros de diálogo con menús de opciones son una forma útil de interactuar con el usuario en aplicaciones Java. La
clase `JOptionPane` proporciona métodos simples y flexibles para crear menús de opciones personalizados y manejar las
respuestas del usuario de manera efectiva.