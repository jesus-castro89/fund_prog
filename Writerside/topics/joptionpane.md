# Ventanas emergentes con JOptionPane

En Java, la clase `JOptionPane` proporciona métodos estáticos para mostrar ventanas emergentes con mensajes, preguntas y
opciones para interactuar con el usuario. Estas ventanas emergentes son útiles para mostrar información, solicitar datos
al usuario y confirmar acciones en aplicaciones de escritorio.

En este artículo, se explicará cómo utilizar la clase `JOptionPane` para mostrar diferentes tipos de ventanas emergentes
en Java.

## Personalización de Ventanas Emergentes

Antes de conocer los métodos específicos de `JOptionPane`, es importante mencionar que se pueden personalizar las
ventanas con la clase `UIManager`. Esta clase permite personalizar varios aspectos de una ventana pero veremos en
específico como cambiar la fuente de mensajes de `JOptionPane`, botones y otros componentes.

Para cambiar la fuente de los mensajes de `JOptionPane`, se puede utilizar el siguiente código:

```java
UIManager.put("OptionPane.messageFont", new Font("Arial", Font.PLAIN, 14));
```

En este caso, se ha cambiado la fuente de los mensajes de `JOptionPane` a `Arial` con un tamaño de `14`. De esta forma,
todos los mensajes que se muestren con `JOptionPane` utilizarán esta fuente.

Para cambiar la fuente de los botones de `JOptionPane`, se puede utilizar el siguiente código:

```java
UIManager.put("OptionPane.buttonFont", new Font("Arial", Font.PLAIN, 14));
```

En este caso, se ha cambiado la fuente de los botones de `JOptionPane` a `Arial` con un tamaño de `14`. De esta forma,
todos los botones que se muestren en los cuadros de diálogo de `JOptionPane` utilizarán esta fuente.

Para cambiar la fuente de las entradas de texto de `JOptionPane`, se puede utilizar el siguiente código:

```java
UIManager.put("TextField.font", new Font("Arial", Font.PLAIN, 14));
```

En este caso, se ha cambiado la fuente de las entradas de texto de `JOptionPane` a `Arial` con un tamaño de `14`. De
esta forma, todas las entradas de texto que se muestren en los cuadros de diálogo de `JOptionPane` utilizarán esta
fuente.

Estos son solo algunos ejemplos de cómo personalizar las ventanas emergentes de `JOptionPane` en Java. Es posible
personalizar otros aspectos de las ventanas emergentes utilizando la clase `UIManager` según las necesidades de la
aplicación.

## Mensajes Informativos

Para mostrar un mensaje informativo con `JOptionPane` en Java, se puede utilizar el método `showMessageDialog()`. Por
ejemplo:

```java
JOptionPane.showMessageDialog(null, "Este es un mensaje informativo", "Información", JOptionPane.INFORMATION_MESSAGE);
```

En este ejemplo, se muestra un cuadro de diálogo con el mensaje "Este es un mensaje informativo" y el título "
Información", dónde:

* El primer parámetro (`null`) indica que el cuadro de diálogo se mostrará en el centro de la pantalla.
* El segundo parámetro es el mensaje que se mostrará en el cuadro de diálogo.
* El tercer parámetro es el título del cuadro de diálogo.
* El cuarto parámetro (`JOptionPane.INFORMATION_MESSAGE`) indica el tipo de mensaje a mostrar (en este caso, un mensaje
  informativo).

### Tipos de Mensajes

`JOptionPane` proporciona diferentes tipos de mensajes que se pueden mostrar en los cuadros de diálogo, como:

| Constante                         | Descripción               |
|-----------------------------------|---------------------------|
| `JOptionPane.ERROR_MESSAGE`       | Mensaje de error          |
| `JOptionPane.INFORMATION_MESSAGE` | Mensaje informativo       |
| `JOptionPane.WARNING_MESSAGE`     | Mensaje de advertencia    |
| `JOptionPane.QUESTION_MESSAGE`    | Mensaje de pregunta       |
| `JOptionPane.PLAIN_MESSAGE`       | Mensaje simple(Sin icono) |

Estos tipos de mensajes permiten personalizar la apariencia de los cuadros de diálogo según el propósito del mensaje.

## Entrada de Datos

Para solicitar datos al usuario con `JOptionPane` en Java, se puede utilizar el método `showInputDialog()`. Por ejemplo:

```java
String nombre = JOptionPane.showInputDialog(null, "Ingrese su nombre", "Entrada de Datos", JOptionPane.QUESTION_MESSAGE);
```

Existen diversos constructores para el método `showInputDialog()`, que permiten personalizar el cuadro de diálogo según
las necesidades de la aplicación, a saber:

* `showInputDialog(Component parentComponent, Object message)`: Muestra un cuadro de diálogo con un campo de entrada de
  texto y un mensaje.
* `showInputDialog(Component parentComponent, Object message, Object initialSelectionValue)`: Muestra un cuadro de
  diálogo con un campo de entrada de texto, un mensaje y un valor inicial.
* `showInputDialog(Component parentComponent, Object message, String title, int messageType)`: Muestra un cuadro de
  diálogo con un campo de entrada de texto, un mensaje, un título y un tipo de mensaje.
* `showInputDialog(Component parentComponent, Object message, String title, int messageType, Icon icon, Object[]
  selectionValues, Object initialSelectionValue)`: Muestra un cuadro de diálogo con un campo de entrada de texto, un
  mensaje, un título, un tipo de mensaje, un icono, valores de selección y un valor inicial.
* `showInputDialog(Object message)`: Muestra un cuadro de diálogo con un campo de entrada de texto y un mensaje.

En este ejemplo, se muestra un cuadro de diálogo con un campo de entrada de texto para que el usuario ingrese su nombre.
El valor ingresado por el usuario se almacena en la variable `nombre`.

El valor que devuelve `showInputDialog()` es de tipo `Object`, por lo que es necesario convertirlo al tipo de dato
correspondiente. Por ejemplo:

```java
int edad = Integer.parseInt(JOptionPane.showInputDialog("Ingrese su edad"));
double altura = Double.parseDouble(JOptionPane.showInputDialog("Ingrese su altura"));
float peso = Float.parseFloat(JOptionPane.showInputDialog("Ingrese su peso"));
```

En este caso, se solicita al usuario que ingrese su edad, altura y peso, y se convierten los valores ingresados a los
tipos de datos `int`, `double` y `float`, respectivamente.

## Confirmación de Acciones

Para confirmar una acción con `JOptionPane` en Java, se puede utilizar el método `showConfirmDialog()`. Por ejemplo:

```java
int confirmacion = JOptionPane.showConfirmDialog(null, "¿Está seguro de eliminar este archivo?", "Confirmación",
        JOptionPane.YES_NO_OPTION, JOptionPane.QUESTION_MESSAGE);

if (confirmacion == JOptionPane.YES_OPTION) {

    // Eliminar el archivo
    System.out.println("Archivo eliminado");

} else {

    // Cancelar la eliminación
    System.out.println("Eliminación cancelada");

}
```

En este ejemplo, se muestra un cuadro de diálogo con la pregunta "¿Está seguro de eliminar este archivo?" y dos botones
(`Sí` y `No`). Dependiendo de la opción seleccionada por el usuario, se imprime un mensaje en la consola.

El método `showConfirmDialog()` permite personalizar el cuadro de diálogo con diferentes opciones, como:

* `JOptionPane.DEFAULT_OPTION`: Botones predeterminados (`Aceptar` y `Cancelar`).
* `JOptionPane.YES_NO_OPTION`: Botones `Sí` y `No`.
* `JOptionPane.YES_NO_CANCEL_OPTION`: Botones `Sí`, `No` y `Cancelar`.
* `JOptionPane.OK_CANCEL_OPTION`: Botones `Aceptar` y `Cancelar`.

Estas opciones permiten adaptar el cuadro de diálogo a las necesidades específicas de la aplicación.

Y al igual que en el caso anterior, `showConfirmDialog()` tiene diversos constructores que permiten personalizar el
cuadro de diálogo según las necesidades de la aplicación, a saber:

* `showConfirmDialog(Component parentComponent, Object message)`: Muestra un cuadro de diálogo con un mensaje y botones
  predeterminados.
* `showConfirmDialog(Component parentComponent, Object message, String title, int optionType)`: Muestra un cuadro de
  diálogo con un mensaje, un título y un tipo de opción.
* `showConfirmDialog(Component parentComponent, Object message, String title, int optionType, int messageType)`: Muestra
  un cuadro de diálogo con un mensaje, un título, un tipo de opción y un tipo de mensaje.
* `showConfirmDialog(Component parentComponent, Object message, String title, int optionType, int messageType, Icon
  icon)`: Muestra un cuadro de diálogo con un mensaje, un título, un tipo de opción, un tipo de mensaje y un icono.
* `showConfirmDialog(Object message)`: Muestra un cuadro de diálogo con un mensaje y botones predeterminados.

## Conclusión

Las ventanas emergentes con `JOptionPane` son una forma sencilla y efectiva de interactuar con el usuario en
aplicaciones de escritorio en Java. Al utilizar los métodos `showMessageDialog()`, `showInputDialog()` y
`showConfirmDialog()`, es posible mostrar mensajes informativos, solicitar datos al usuario y confirmar acciones de
manera intuitiva y amigable.