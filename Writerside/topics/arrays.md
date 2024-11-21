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

### Funciones de Arreglos

| Función                        | Descripción                                               |
|--------------------------------|-----------------------------------------------------------|
| `length`                       | Devuelve la longitud del arreglo.                         |
| `clone()`                      | Crea una copia superficial del arreglo.                   |
| `copyOf(arreglo, tamaño)`      | Crea una copia del arreglo con el tamaño especificado.    |
| `fill(arreglo, valor)`         | Rellena el arreglo con el valor especificado.             |
| `sort(arreglo)`                | Ordena el arreglo en orden ascendente.                    |
| `binarySearch(arreglo, valor)` | Busca un valor en el arreglo utilizando búsqueda binaria. |

Estas son algunas de las funciones más comunes que se pueden utilizar con arreglos en Java. Para más información sobre
las funciones disponibles, se recomienda consultar la [documentación oficial de Java](https://docs.oracle.com/en/java/).

### Ejemplo de Uso de Arreglos y Funciones

```java
import java.util.Arrays;

class Main {
    public static void main(String[] args) {
        int[] numeros = {5, 3, 8, 1, 2, 4, 7, 6};

        // Imprimir el arreglo original
        System.out.println("Arreglo original: " + Arrays.toString(numeros));

        // Ordenar el arreglo
        Arrays.sort(numeros);
        System.out.println("Arreglo ordenado: " + Arrays.toString(numeros));

        // Buscar un valor en el arreglo
        int indice = Arrays.binarySearch(numeros, 4);
        System.out.println("El valor 4 se encuentra en el índice: " + indice);
    }
}
```

En este ejemplo, se declara un arreglo `numeros` de enteros con valores desordenados. Se utiliza la función
`Arrays.sort()` para ordenar el arreglo en orden ascendente y la función `Arrays.binarySearch()` para buscar el valor
`4` en el arreglo. Finalmente, se imprime el arreglo original, el arreglo ordenado y el índice donde se encuentra el
valor `4`.

## Arrays Multidimensionales

Los arreglos multidimensionales son arreglos que contienen otros arreglos como elementos. En Java, se pueden declarar
arreglos bidimensionales, tridimensionales o de mayor dimensión. Para declarar un arreglo bidimensional en Java, se
utiliza la siguiente sintaxis:

```java
tipo[][] nombreArreglo = new tipo[fila][columna];
```

Por ejemplo, para declarar un arreglo bidimensional de enteros con 3 filas y 2 columnas:

```java
int[][] matriz = new int[3][2];
```

Para acceder a un elemento de un arreglo bidimensional, se utiliza el índice de la fila y el índice de la columna. Por
ejemplo, para acceder al elemento en la segunda fila y la primera columna de la matriz:

```java
int elemento = matriz[1][0];
```

En este caso, se ha accedido al elemento en la segunda fila y la primera columna de la matriz y se ha almacenado en la
variable `elemento`.

### Funciones de Arrays Multidimensionales

| Función                        | Descripción                                               |
|--------------------------------|-----------------------------------------------------------|
| `length`                       | Devuelve la longitud de la primera dimensión del arreglo. |
| `length` (segunda dimensión)   | Devuelve la longitud de la segunda dimensión del arreglo. |
| `clone()`                      | Crea una copia superficial del arreglo.                   |
| `copyOf(arreglo, tamaño)`      | Crea una copia del arreglo con el tamaño especificado.    |
| `fill(arreglo, valor)`         | Rellena el arreglo con el valor especificado.             |
| `sort(arreglo)`                | Ordena el arreglo en orden ascendente.                    |
| `binarySearch(arreglo, valor)` | Busca un valor en el arreglo utilizando búsqueda binaria. |

Estas son algunas de las funciones más comunes que se pueden utilizar con arreglos multidimensionales en Java. Para más
información sobre las funciones disponibles, se recomienda consultar
la [documentación oficial de Java](https://docs.oracle.com/en/java/).

### Ejemplo de Uso de Arrays Multidimensionales

```java
import java.util.Arrays;

class Main {
    public static void main(String[] args) {
        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Imprimir la matriz original
        for (int[] fila : matriz) {
            System.out.println(Arrays.toString(fila));
        }

        // Ordenar la primera fila de la matriz
        Arrays.sort(matriz[0]);
        System.out.println("Primera fila ordenada: " + Arrays.toString(matriz[0]));

        // Buscar un valor en la matriz
        int indice = Arrays.binarySearch(matriz[1], 5);
        System.out.println("El valor 5 se encuentra en el índice: " + indice);
    }
}
```

En este ejemplo, se declara una matriz `matriz` bidimensional de enteros con 3 filas y 3 columnas. Se utiliza un bucle
`for` para imprimir la matriz original, la función `Arrays.sort()` para ordenar la primera fila de la matriz y la
función `Arrays.binarySearch()` para buscar el valor `5` en la segunda fila de la matriz. Finalmente, se imprime la
primera fila ordenada y el índice donde se encuentra el valor `5`.

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

| Función                   | Descripción                                               |
|---------------------------|-----------------------------------------------------------|
| `add(elemento)`           | Añade un elemento al final de la lista.                   |
| `add(posición, elemento)` | Añade un elemento en la posición especificada.            |
| `get(posición)`           | Devuelve el elemento en la posición especificada.         |
| `set(posición, elemento)` | Reemplaza el elemento en la posición especificada.        |
| `remove(posición)`        | Elimina el elemento en la posición especificada.          |
| `size()`                  | Devuelve el tamaño de la lista.                           |
| `clear()`                 | Elimina todos los elementos de la lista.                  |
| `removeFirst()`           | Elimina el primer elemento de la lista.                   |
| `removeLast()`            | Elimina el último elemento de la lista.                   |
| `indexOf(elemento)`       | Devuelve el índice de la primera ocurrencia del elemento. |
| `lastIndexOf(elemento)`   | Devuelve el índice de la última ocurrencia del elemento.  |
| `contains(elemento)`      | Comprueba si la lista contiene el elemento especificado.  |
| `addFirst(elemento)`      | Añade un elemento al principio de la lista.               |
| `addLast(elemento)`       | Añade un elemento al final de la lista.                   |
| `removeIf(condición)`     | Elimina los elementos que cumplen la condición.           |
| `sort(comparador)`        | Ordena la lista utilizando un comparador.                 |

Estas son algunas de las funciones más comunes que se pueden utilizar con ArrayList en Java. Para más información sobre
las funciones disponibles, se recomienda consultar la [documentación oficial de Java](https://docs.oracle.com/en/java/).

## Ordenamiento y Búsqueda en Listas

Para ordenar un ArrayList en Java, se puede utilizar el método `sort()` de la clase `Collections`. Por ejemplo, para
ordenar un ArrayList de enteros:

```java
ArrayList<Integer> numeros = new ArrayList<>();
numeros.add(5);
numeros.add(3);
numeros.add(8);
numeros.add(1);
numeros.add(2);

numeros.sort(null);
```

En este caso, se ha ordenado el ArrayList `numeros` de enteros en orden ascendente utilizando el método `sort()`.
También es posible utilizar un comparador personalizado para ordenar la lista de acuerdo a un criterio específico. Por
ejemplo, para ordenar un ArrayList de cadenas en orden descendente:

```java
ArrayList<String> nombres = new ArrayList<>();
nombres.add("Juan");
nombres.add("María");
nombres.add("Pedro");

nombres.sort(Collections.reverseOrder());
```

Para buscar un elemento en un ArrayList en Java, se puede utilizar el método `indexOf()` para obtener el índice de la
primera ocurrencia del elemento. Por ejemplo, para buscar el índice del valor `María` en el ArrayList `nombres`:

```java
int indice = nombres.indexOf("María");
```

### Ejemplo de Uso de ArrayList y Funciones

```java
import java.util.ArrayList;

class Main {
    public static void main(String[] args) {
        ArrayList<Integer> numeros = new ArrayList<>();
        numeros.add(5);
        numeros.add(3);
        numeros.add(8);
        numeros.add(1);
        numeros.add(2);
        numeros.add(4);
        numeros.add(7);
        numeros.add(6);

        // Imprimir la lista original
        System.out.println("Lista original: " + numeros);

        // Ordenar la lista
        numeros.sort(null);
        System.out.println("Lista ordenada: " + numeros);

        // Buscar un valor en la lista
        int indice = numeros.indexOf(4);
        System.out.println("El valor 4 se encuentra en el índice: " + indice);
    }
}
```

## Conclusión

Los arreglos y las listas son estructuras de datos fundamentales en Java que permiten almacenar múltiples valores en una
sola variable. Los arreglos son más eficientes en términos de memoria y rendimiento, pero tienen un tamaño fijo,
mientras que los ArrayList son más flexibles y permiten añadir, eliminar y modificar elementos dinámicamente. Ambas
estructuras son útiles en diferentes situaciones y es importante conocer cómo utilizarlas correctamente en el desarrollo
de aplicaciones en Java.