# Estructura de control de flujo

La estructura de control de flujo es una parte fundamental de cualquier lenguaje de programación. Permite controlar el
flujo de ejecución de un programa, lo que significa que se pueden tomar decisiones y realizar acciones basadas en
ciertas condiciones. En Java, hay varias estructuras de control de flujo que se utilizan para controlar el flujo de
ejecución de un programa. Algunas de las estructuras de control de flujo más comunes en Java son:

- **Estructuras de control de selección**: Permiten tomar decisiones basadas en ciertas condiciones. Algunas de las
  estructuras de control de selección más comunes en Java son `if`, `if-else`, `switch`.
- **Estructuras de control de repetición**: Permiten repetir un bloque de código varias veces. Algunas de las
  estructuras
  de control de repetición más comunes en Java son `for`, `while`, `do-while`.
- **Estructuras de control de transferencia**: Permiten transferir el control de un programa a una ubicación específica.
  Algunas de las estructuras de control de transferencia más comunes en Java son `break`, `continue`, `return`.

## Estructuras de Control de Selección

Las estructuras de control de selección permiten tomar decisiones basadas en ciertas condiciones. En Java, hay varias
estructuras de control de selección que se utilizan para tomar decisiones en un programa. Algunas de las estructuras de
control de selección más comunes en Java son:

- **if**: La estructura `if` se utiliza para ejecutar un bloque de código si una condición es verdadera.
- **if-else**: La estructura `if-else` se utiliza para ejecutar un bloque de código si una condición es verdadera y otro
  bloque de código si la condición es falsa.
- **if-else-if**: La estructura `if-else-if` se utiliza para ejecutar un bloque de código si una condición es verdadera,
  otro bloque de código si otra condición es verdadera, y así sucesivamente.
- **switch**: La estructura `switch` se utiliza para seleccionar uno de varios bloques de código para ejecutar, basado
  en
  el valor de una expresión.
- **Operador ternario**: El operador ternario (`?:`) se utiliza para asignar un valor a una variable basado en una
  condición.

### Ejemplo de Estructuras de Control de Selección

A continuación se muestra un ejemplo de cómo se utilizan las estructuras de control de selección en Java:

```java
int x = 10;
// Estructura if
if (x > 0) {
    System.out.println("x es positivo");
}
// Estructura if-else
if (x > 0) {
    System.out.println("x es positivo");
} else {
    System.out.println("x es negativo o cero");
}
// Estructura if-else-if
if (x > 0) {
    System.out.println("x es positivo");
} else if (x < 0) {
    System.out.println("x es negativo");
} else {
    System.out.println("x es cero");
}
// Estructura switch
switch (x) {
    case 1:
        System.out.println("x es 1");
        break;
    case 2:
        System.out.println("x es 2");
        break;
    default:
        System.out.println("x no es 1 ni 2");
}
// Estructura switch mejorada
switch (x) {
    case 1 -> System.out.println("x es 1");
    case 2 -> System.out.println("x es 2");
    default -> System.out.println("x no es 1 ni 2");
}
// Operador ternario
String mensaje = (x > 0) ? "x es positivo" : "x es negativo o cero";
System.out.println(mensaje);
```

En este ejemplo:

- Se declara una variable `x` con el valor `10`.
- Se utilizan las estructuras de control de selección `if`, `if-else`, `if-else-if`, `switch`, y el operador ternario
  para tomar decisiones basadas en el valor de la variable `x`.
- Se imprime un mensaje en la consola dependiendo de la condición evaluada.
- Se utiliza la estructura `switch` mejorada introducida en Java 12.
- Se asigna un mensaje a la variable `mensaje` basado en la condición evaluada.
- Se imprime el mensaje en la consola.

## Estructuras de Control de Repetición

Las estructuras de control de repetición permiten repetir un bloque de código varias veces. En Java, hay varias
estructuras de control de repetición que se utilizan para repetir un bloque de código en un programa. Algunas de las
estructuras de control de repetición más comunes en Java son:

- **for**: La estructura `for` se utiliza para repetir un bloque de código un número específico de veces.
- **while**: La estructura `while` se utiliza para repetir un bloque de código mientras una condición sea verdadera.
- **do-while**: La estructura `do-while` se utiliza para repetir un bloque de código al menos una vez y luego repetirlo
  mientras una condición sea verdadera.
- **for-each**: La estructura `for-each` se utiliza para iterar sobre una colección de elementos.
- **break**: La palabra clave `break` se utiliza para salir de un bucle.
- **continue**: La palabra clave `continue` se utiliza para saltar a la siguiente iteración de un bucle.

### Ejemplo de Estructuras de Control de Repetición

A continuación se muestra un ejemplo de cómo se utilizan las estructuras de control de repetición en Java:

```java
// Estructura for
for (int i = 0; i < 5; i++) {
    System.out.println("Iteración " + i);
}
// Estructura while
int j = 0;
while (j < 5) {
    System.out.println("Iteración " + j);
    j++;
}
// Estructura do-while
int k = 0;
do {
    System.out.println("Iteración " + k);
    k++;
} while (k < 5);
// Estructura for-each
int[] numeros = {1, 2, 3, 4, 5};
for (int numero : numeros) {
    System.out.println("Número: " + numero);
}
// Estructura break
for (int l = 0; l < 10; l++) {
    if (l == 5) {
        break;
    }
    System.out.println("Iteración " + l);
}
// Estructura continue
for (int m = 0; m < 5; m++) {
    if (m == 2) {
        continue;
    }
    System.out.println("Iteración " + m);
}
```

En este ejemplo:

- Se utilizan las estructuras de control de repetición `for`, `while`, `do-while`, `for-each`, y las palabras clave
  `break` y `continue` para repetir un bloque de código.
- Se imprime un mensaje en la consola en cada iteración del bucle.
- Se utiliza la estructura `for-each` para iterar sobre un array de números.
- Se utiliza la palabra clave `break` para salir de un bucle cuando se cumple una condición.
- Se utiliza la palabra clave `continue` para saltar a la siguiente iteración de un bucle cuando se cumple una
  condición.
- Se muestra cómo se utilizan las estructuras de control de repetición en Java.
turn**: La palabra clave `return` se utiliza para devolver un valor de un método y salir del método.