# Cadenas con Formato y Bloques de texto

En Java, las cadenas de texto se pueden formatear de diferentes maneras para mostrar información de manera legible y
estructurada. En este artículo, veremos cómo utilizar cadenas con formato y bloques de texto en Java.

## Cadenas con Formato

Las cadenas con formato permiten combinar texto con valores de variables de una manera más legible y estructurada. En
Java, se pueden utilizar los métodos `String.format()` y `System.out.printf()` para formatear cadenas con valores
dinámicos. Por ejemplo:

```java
String nombre = "Juan";
int edad = 30;
double altura = 1.75;

String mensaje = String.format("Hola, %s. Tienes %d años y mides %.2f 
                metros.", nombre, edad, altura);
System.out.println(mensaje);
// Salida: Hola, Juan. Tienes 30 años y mides 1.75 metros.
// Equivalente a:
System.out.printf("Hola, %s. Tienes %d años y mides %.2f metros.\n", 
                nombre, edad, altura);
```

En este ejemplo, se ha utilizado el método `String.format()` para combinar el texto "Hola, %s. Tienes %d años y mides
%.2f metros." con los valores de las variables `nombre`, `edad` y `altura`. Luego, se imprime el mensaje formateado
utilizando `System.out.println()` o bien `System.out.printf()`.

## Los comodines de formato

Los comodines de formato son caracteres especiales que se utilizan en las cadenas con formato para indicar dónde se
deben insertar los valores de las variables. Los comodines de formato en Java son:

| Comodín | Tipo de Dato |
|---------|--------------|
| `%s`    | Cadena       |
| `%d`    | Entero       |
| `%f`    | Decimal      |
| `%c`    | Carácter     |
| `%b`    | Booleano     |

### Casos Especiales

Además de los comodines de formato básicos, Java también ofrece algunos casos especiales para formatear valores de
variables de manera más específica. Algunos de los casos especiales más comunes son:

| Comodín | Descripción                                                      |
|---------|------------------------------------------------------------------|
| `%10s`  | Justificar a la derecha en 10 espacios                           |
| `%-10s` | Justificar a la izquierda en 10 espacios                         |
| `%05d`  | Rellenar con ceros a la izquierda                                |
| `%,d`   | Separador de miles                                               |
| `%.xf`  | Número de decimales, siendo X la cantidad de decimales esperados |
| `%x`    | Formato hexadecimal                                              |
| `%o`    | Formato octal                                                    |

## Bloques de Texto

Los bloques de texto son una característica introducida en Java 13 que permite definir cadenas de texto multilínea de
manera más legible y sencilla. Para utilizar bloques de texto en Java, se utilizan las comillas triples (`"""`) para
encerrar el texto. Por ejemplo:

```java
String texto = """
    Este es un bloque de texto
    que puede contener múltiples líneas
    sin necesidad de utilizar caracteres de escape.
    """;
System.out.println(texto);
```

En este ejemplo, se ha definido un bloque de texto multilínea utilizando las comillas triples (`"""`). El texto puede
contener múltiples líneas y no es necesario utilizar caracteres de escape como `\n` para indicar saltos de línea.

Además de ellos puedes usar los bloques de texto para cadenas con formato, por ejemplo:

```java
String nombre = "Juan";
int edad = 30;
double altura = 1.75;
String mensaje = """
    Hola, %s. 
    Tienes %d años y mides %.2f metros.
    """.formatted(nombre, edad, altura);
System.out.println(mensaje);
```

En este caso, se ha utilizado el método `formatted()` para combinar el texto del bloque con los valores de las variables
`nombre`, `edad` y `altura`. Luego, se imprime el mensaje formateado utilizando `System.out.println()`.

## Conclusión

Las cadenas con formato y los bloques de texto son herramientas útiles para mostrar información de manera legible y
estructurada en Java. Al utilizar comodines de formato y bloques de texto, se puede mejorar la legibilidad y claridad
del código, así como facilitar la presentación de datos al usuario.