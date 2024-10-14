# Arreglos (Arrays) y ArrayList

Los arreglos (arrays) y las listas (ArrayList) son estructuras de datos que permiten almacenar múltiples valores en una
sola variable. En este artículo, veremos cómo declarar, inicializar y utilizar arreglos y listas en Java.

## Arreglos (Arrays)

Un arreglo es una estructura de datos que permite almacenar múltiples valores del mismo tipo en una sola variable. Para
declarar un arreglo en Java, se utiliza la siguiente sintaxis:

```java
tipo[] nombreArreglo = new tipo[tamaño];
```

Por ejemplo, para declarar un arreglo de enteros con 5 elementos:

```java
int[] numeros1 = new int[5];
int[] numeros2 = {1, 2, 3, 4, 5};
```

En este caso, se ha declarado un arreglo `numeros1` de enteros con 5 elementos y se ha inicializado con valores nulos.
También se ha declarado un arreglo `numeros2` de enteros con 5 elementos y se ha inicializado con los valores `1`, `2`,
`3`, `4` y `5`.

Para acceder a un elemento de un arreglo, se utiliza el índice del elemento entre corchetes. Por ejemplo, para acceder
al segundo elemento del arreglo `numeros2`:

```java
int segundoElemento = numeros2[1];
```

En este caso, se ha accedido al segundo elemento del arreglo `numeros2` (índice `1`) y se ha almacenado en la variable
`segundoElemento`.

## Listas (ArrayList)

Un ArrayList es una implementación de la interfaz `List` en Java que permite almacenar múltiples valores en una sola
variable. Para declarar un ArrayList en Java, se utiliza la siguiente sintaxis:

```java
ArrayList<tipo> nombreLista = new ArrayList<>();
```

Por ejemplo, para declarar un ArrayList de cadenas:

```java
ArrayList<String> nombres = new ArrayList<>();
nombres.add("Juan");
nombres.add("María");
nombres.add("Pedro");
```

En este caso, se ha declarado un ArrayList `nombres` de cadenas y se han añadido los valores `Juan`, `María` y
`Pedro` a la lista.

Para acceder a un elemento de un ArrayList, se utiliza el método `get()` con el índice del elemento. Por ejemplo, para
acceder al segundo elemento del ArrayList `nombres`:

```java
String segundoNombre = nombres.get(1);
```

En este caso, se ha accedido al segundo elemento del ArrayList `nombres` (índice `1`) y se ha almacenado en la variable
`segundoNombre`.

### Funciones de ArrayList

| Función                   | Descripción                                        |
|---------------------------|----------------------------------------------------|
| `add(elemento)`           | Añade un elemento al final de la lista.            |
| `add(posición, elemento)` | Añade un elemento en la posición especificada.     |
| `get(posición)`           | Devuelve el elemento en la posición especificada.  |
| `set(posición, elemento)` | Reemplaza el elemento en la posición especificada. |
| `remove(posición)`        | Elimina el elemento en la posición especificada.   |
| `size()`                  | Devuelve el tamaño de la lista.                    |
| `clear()`                 | Elimina todos los elementos de la lista.           |

Estas son algunas de las funciones más comunes que se pueden utilizar con ArrayList en Java. Para más información sobre
las funciones disponibles, se recomienda consultar la [documentación oficial de Java](https://docs.oracle.com/en/java/).

## Conclusión

Los arreglos y las listas son estructuras de datos fundamentales en Java que permiten almacenar múltiples valores en una
sola variable. Los arreglos son más eficientes en términos de memoria y rendimiento, pero tienen un tamaño fijo,
mientras que los ArrayList son más flexibles y permiten añadir, eliminar y modificar elementos dinámicamente. Ambas
estructuras son útiles en diferentes situaciones y es importante conocer cómo utilizarlas correctamente en el desarrollo
de aplicaciones en Java.