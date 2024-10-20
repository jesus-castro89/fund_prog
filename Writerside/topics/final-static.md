# Los modificadores `final` y `static`

En Java, los modificadores `final` y `static` se utilizan para definir constantes y métodos estáticos, respectivamente.
Estos modificadores tienen diferentes usos y propósitos en la programación en Java.

## Modificador `final`

El modificador `final` se utiliza para declarar constantes, métodos finales y clases finales en Java. Al utilizar el
modificador `final`, se índica que el valor de una variable, el comportamiento de un método o la estructura de una clase
no pueden ser modificados una vez que han sido definidos.

### Constantes

En Java, una constante es una variable cuyo valor no puede ser modificado una vez que ha sido asignado. Para declarar
una constante con el modificador `final`, se utiliza la siguiente sintaxis:

```java
final tipo NOMBRE_CONSTANTE = valor;
```

Por ejemplo, para declarar una constante entera con el valor `10`:

```java
final int NUMERO_MAXIMO = 10;
```

En este caso, la constante `NUMERO_MAXIMO` tiene un valor de `10` y no puede ser modificado en ningún otro lugar del
programa.

> **Nota:** Por convención, los nombres de las constantes en Java se escriben en mayúsculas y separados por guiones
> bajos (`_`). Esto facilita la identificación de las constantes en el código.

> **Nota:** Las constantes en Java también pueden ser declaradas como `static`, lo que permite acceder a ellas sin
> necesidad de crear una instancia de la clase que las contiene.

> **Nota:** Dentro de los tipos enumerados (`enum`) en Java, las constantes son implícitamente `final` y `static`.

## Modificador `static`

El modificador `static` se utiliza para definir métodos y variables estáticas en Java. Una variable estática pertenece a
la clase en lugar de a una instancia específica de la clase, lo que significa que su valor es compartido por todas las
instancias de la clase. Un método estático puede ser invocado sin necesidad de crear una instancia de la clase que lo
contiene.

### Variables Estáticas

Para declarar una variable estática en Java, se utiliza la siguiente sintaxis:

```java
static tipo NOMBRE_VARIABLE = valor;
```

Por ejemplo, para declarar una variable estática entera con el valor `0`:

```java
static int contador = 0;
```

En este caso, la variable `contador` es compartida por todas las instancias de la clase y su valor puede ser accedido y
modificado por cualquier instancia de la clase.

> **Nota:** Las variables estáticas en Java se inicializan una sola vez, cuando la clase es cargada por el cargador de
> clases.

### Métodos Estáticos

Para declarar un método estático en Java, se utiliza la siguiente sintaxis:

```java
static tipoRetorno nombreMetodo(parametros) {
    // Código del método
}
```

Por ejemplo, para declarar un método estático que imprime un mensaje en la consola:

```java
static void imprimirMensaje(String mensaje) {
    System.out.println(mensaje);
}
```

En este caso, el método `imprimirMensaje` es estático y puede ser invocado sin necesidad de crear una instancia de la
clase que lo contiene.

> **Nota:** Los métodos estáticos en Java no pueden acceder a variables de instancia ni a métodos no estáticos de la
> clase.

> **Nota:** Los métodos estáticos en Java son útiles para definir funciones de utilidad que no dependen del estado de
> una instancia específica de la clase.

> **Nota:** Los métodos estáticos en Java pueden ser invocados a través del nombre de la clase, sin necesidad de crear
> una instancia de la clase.

## Conclusión

En resumen, los modificadores `final` y `static` son herramientas poderosas en Java que permiten definir constantes,
métodos estáticos y variables estáticas en las clases. Al utilizar estos modificadores de forma adecuada, es posible
mejorar la claridad y la eficiencia del código, así como facilitar la reutilización de funciones y valores en
diferentes partes de un programa Java.