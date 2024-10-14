# La clase Math

La clase `Math` es una clase estática que proporciona métodos y constantes para realizar operaciones matemáticas en
Java. Esta clase se encuentra en el paquete `java.lang` y no es necesario importarla para utilizarla en un programa
Java.

## Métodos de la Clase Math

La clase `Math` proporciona una serie de métodos estáticos para realizar operaciones matemáticas comunes, como
cálculos de raíces cuadradas, exponenciales, logaritmos, funciones trigonométricas, entre otros. Algunos de los métodos
más utilizados son:

| Método                | Descripción                                    |
|-----------------------|------------------------------------------------|
| `abs(valor)`          | Devuelve el valor absoluto de un número.       |
| `sqrt(valor)`         | Devuelve la raíz cuadrada de un número.        |
| `pow(base, exp)`      | Devuelve la potencia de un número.             |
| `log(valor)`          | Devuelve el logaritmo natural de un número.    |
| `sin(angulo)`         | Devuelve el seno de un ángulo en radianes.     |
| `cos(angulo)`         | Devuelve el coseno de un ángulo en radianes.   |
| `tan(angulo)`         | Devuelve la tangente de un ángulo en radianes. |
| `toRadians(grados)`   | Convierte grados a radianes.                   |
| `toDegrees(radianes)` | Convierte radianes a grados.                   |
| `random()`            | Devuelve un número aleatorio entre 0 y 1.      |

Estos son solo algunos de los métodos que proporciona la clase `Math`. Para ver la lista completa de métodos y
constantes, se puede consultar
la [documentación oficial de Java](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html).

## Valor aleatorio de un rango

Para obtener un valor aleatorio dentro de un rango específico, se puede utilizar el método `random()` de la clase
`Math` junto con la siguiente fórmula
matemática: $$\text{Math.random()} \times (\text{max} - \text{min} + 1) + \text{min}$$

Donde `max` es el valor máximo del rango y `min` es el valor mínimo del rango. Por ejemplo, para obtener un número
aleatorio entre 1 y 10:

```java
int numeroAleatorio = (int) (Math.random() * (10 - 1 + 1) + 1);
// Que es equivalente a:
// int numeroAleatorio = (int) (Math.random() * 10) + 1;
```

En este caso, se ha multiplicado el resultado de `Math.random()` por el rango deseado y se ha sumado el valor mínimo
para obtener un número aleatorio dentro del rango especificado.

## Conclusión

La clase `Math` en Java proporciona una serie de métodos estáticos para realizar operaciones matemáticas comunes. Estos
métodos son útiles para realizar cálculos matemáticos en un programa Java de forma sencilla y eficiente.